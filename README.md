# 杂记

## Swagger

### 简介：请求数据接口(APi) 

 Swagger 可视化 : https://localhost:port/swager-ui.html 

 《API接口管理Swagger2实战教程》
 https://blog.csdn.net/guolianggsta/article/details/117827089

 《springBoot使用swagger-ui实现接口可视化调用》
 https://blog.csdn.net/qq_28483283/article/details/113888664

### 依赖

```
		<dependency>
            <groupId>io.springfox</groupId>
            <artifactId>springfox-swagger2</artifactId>
            <version>2.6.1</version>
        </dependency>

        <dependency>
            <groupId>io.springfox</groupId>
            <artifactId>springfox-swagger-ui</artifactId>
            <version>2.6.1</version>
        </dependency>
```

### 涉及到的注解

```
//控制器
@Api(value = "XXXController", description = "XXX信息接口"--接口描述) 
```
```
//控制器方法
@ApiOperation(value = "列表(精确查询+分页)"--接口描述, httpMethod = "POST"--请求类型) 

@PostMapping(value = "listProjectStartByPage"--请求值, produces = {"application/json;charset=UTF-8"}--指定返回格式)

@ResponseBody
public String funnction_name(@RequestBody(required=true) 操作对象类型 操作对象, HttpServletRequest request) throws Exception {};

```

## FastJsonUtils 工具类

### 简介：Json 返回处理

>包含：状态码(code)、数据(data)、消息(message)、时间(time)


### 依赖

```
	<dependency>
			<groupId>com.alibaba</groupId>
			<artifactId>fastjson</artifactId>
			<version>1.2.83</version>
	</dependency>
```

## SpringBoot 注解

>@Resource  &  @AutoWired : @Autowired注入的时候要确保只有一个实现类 



# SQL 小芝士


## XML文件查询条件

> Mapper 方法 ： 

	返回类型  方法名 (@Param("model") 类型 对象名 );

:star2: 单对象属性判断( 使用 model 代替变量对象)

```
	<if test="model.属性名 条件">
	and 表字段名 = #{model.属性}
	</if>
```


:star2: 对象集合属性判断( 使用 model 代替变量对象)

```
<if test="model.对象集合名 条件 ">

	and 表字段名 in

	<foreach collection="model.集合" item="属性" index="index" separator="," open="(" close=")">``

    #{属性}

    </foreach>

</if>
```


## 模板SQL操作

>导入依赖

```
<!-- mybatis 依赖 -->
        <dependency>
            <groupId>org.mybatis.spring.boot</groupId>
            <artifactId>mybatis-spring-boot-starter</artifactId>
            <version>2.1.1</version>
        </dependency>

<!-- TKmybatis 依赖 -->
        <dependency>
            <groupId>tk.mybatis</groupId>
            <artifactId>mapper-spring-boot-starter</artifactId>
            <version>1.1.0</version>
        </dependency>

```

>Mapper接口(绑定SQL模板)

```
	public interface SQLMapper<T>{

		@Options(keyProperty = "主键",keyColumn = "数据库字段名")

		//绑定SQL模板
		@InsertProvider( type = 模板.class, method = "dynamicSQL")

		//方法
		int batchInsert(List<T> list);

	}

```

>SQL模板

```
	public class BatchSQLProvider extends MapperTemplate {

		//实现接口
		public BatchSQLProvider(Class<?> mapperClass, MapperHelper mapperHelper) {

        super(mapperClass, mapperHelper);
    	}

    	//SQL操作
    	//思路：利用 StringBuilder 拼写SQL

    	public String batchInsert(MappedStatement statement){

        //获取实体类对应的Class对象
        Class entityClass = getEntityClass(statement);

        //开始拼sql
        StringBuilder sql = new StringBuilder();

        //INSERT INTO 表名
        sql.append(SqlHelper.insertIntoTable(entityClass, tableName(entityClass)));
        
        //(所有列，以逗号隔开)
        sql.append(SqlHelper.insertColumns(entityClass, false, false, false));
        sql.append(" VALUES ");
        
        //遍历实体集合
        sql.append("<foreach collection=\"list\" item=\"record\" separator=\",\" >");
        sql.append("<trim prefix=\"(\" suffix=\")\" suffixOverrides=\",\">");
        
        //获取全部列
        Set<EntityColumn> columnList = EntityHelper.getColumns(entityClass);
        
        //遍历实体所有字段
        for (EntityColumn column : columnList) {

            if (column.isInsertable()) {

                //出现类型com.microsoft.sqlserver.jdbc.SQLServerException: 操作数类型冲突: varbinary
                if(column.getJavaType() == Double.class){

                    //返回格式如:#{record.id,javaType=java.lang.String}
                    String record = column.getColumnHolder("record");
                    record = record.substring(0,record.length()-1)+",jdbcType=DECIMAL"+"}";

                    sql.append(record+ ",");

                }else {

                    sql.append(column.getColumnHolder("record") + ",");

                }

            }
        }

        sql.append("</trim>");
        sql.append("</foreach>");

        //logger.info("{}", sql.toString());
        return sql.toString();
    }

 }


```

## SQL连接

<img src="https://www.runoob.com/wp-content/uploads/2019/01/sql-join.png" style="width: 800px;height: 600px">


# 咖啡 小芝士

## List 集合操作

>将目标List集合分组

```
List<类型> applyTypeList = list.stream().map(实体类 :: 条件).distinct().collect(Collectors.toList());
```

>从List集合中去除元素

```
BoList.removeIf(e -> Strings.isNullOrEmpty(e.getProjectCode()));
```
 
>List集合元素排序

```
//根据 ProjectCode 逆序（需生成新的List）

List<PlanAppraiseBo> sortList = value.stream().sorted(Comparator.comparing(PlanAppraiseBo::getProjectCode).reversed()).collect(Collectors.toList());
```

>List集合过滤

```
  private List<Integer> integers = Lists.list(30, 40, 10, 20);

  Set<Integer> collect = integers.stream().filter(i -> i > 20).collect(Collectors.toSet());

  assertEquals(Sets.newTreeSet(30, 40), collect);

```

## Map集合操作

>将List分组转化为Map

```
Map<类型, List<类型>> map1 = List1.stream().collect(Collectors.groupingBy(实体类 :: 条件属性));
```
 
>Map集合遍历

```
   for (Map.Entry<类1, List<类2>> entry : map集合.entrySet()) {

     List<类2> value = entry.getValue();

   }
```


## String 字符串

>字符串截取

```
String S1 = S2.substring(S2.length() - 保留位数);
```
 
>数字补位

```
// 0 - 补充数； 3 - 补充位数； d - 实数；
String.format("%03d",num)     
```
 
## 实体类

>BO类 ： 业务类   进行业务设计，extends 实体类

>VO类 ： 视图类   显示属性包含的类

## 线程

>多线程塞入流程相关数据

```
	    List<Future> futureList = new ArrayList<>();

        for (DesignAppraiseBo designAppraiseBo : designAppraiseBoList) {

            designAppraiseBo.setLoginName(record.getLoginName());

            Future<String> future = designAppraiseAsyncService.addFlowData(designAppraiseBo);
            futureList.add(future);
        }

        try {

            // 监听线程是否全部结束
            while (true){

            	// 当线程容器中没有任何线程的时候 说明线程已经全部结束
                if (futureList.size() < 1) { 
                    logger.info("线程已全部结束");
                    break;
                }

                for (int i = 0; i < futureList.size(); i++) {
                    Future<String> future = futureList.get(i);
                    future.get();

                    // 线程结束 则将其从线程容器中移除
                    if (future.isDone()){
                        futureList.remove(i);
                        break;
                    }
                }
            }
        }catch (Exception e){
            throw new SystemRuntimeException(e.getMessage());
        }



```