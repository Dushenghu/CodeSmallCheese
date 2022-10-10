# :pushpin:杂记

##  :closed_book:学习资料

> 他人总结的杂七杂八 ： https://www.cnblogs.com/cao-lei/

##  :gun:  easyTools工具包
### 简介
> 自己搞的小工具包 

### 仓库
> [jar包仓库](https://github.com/Dushenghu/easyTools.git)  :  github ==> easyTools ==> jar(package) 



## :dart:Swagger

### 简介：请求数据接口(APi) 

 Swagger 可视化 : https://localhost:项目端口号/swager-ui.html 

 《API接口管理Swagger2实战教程》
 https://blog.csdn.net/guolianggsta/article/details/117827089

 《springBoot使用swagger-ui实现接口可视化调用》
 https://blog.csdn.net/qq_28483283/article/details/113888664

### 依赖

```java
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

```java
//控制器
@Api(value = "XXXController", description = "XXX信息接口"--接口描述) 
```
```java
//控制器方法
@ApiOperation(value = "列表(精确查询+分页)"--接口描述, httpMethod = "POST"--请求类型) 

@PostMapping(value = "listProjectStartByPage"--请求值, produces = {"application/json;charset=UTF-8"}--指定返回格式)

@ResponseBody
public String funnction_name(@RequestBody(required=true) 操作对象类型 操作对象, HttpServletRequest request) throws Exception {};

```

## :gift:Apache Commons 工具包

### 简介

> 官方地址 ： http://jakarta.apache.org/commons/index.html
>
> 工具简介：
>
> **BeanUtils**
> Commons-BeanUtils 提供对 Java 反射和自省API的包装
>
> **Betwixt**
> Betwixt提供将 JavaBean 映射至 XML 文档，以及相反映射的服务.
>
> **Chain**
> Chain 提供实现组织复杂的处理流程的“责任链模式”.
>
> **CLI**
> CLI 提供针对命令行参数，选项，选项组，强制选项等的简单API.
>
> **Codec**
> Codec 包含一些通用的编码解码算法。包括一些语音编码器， Hex, Base64, 以及URL encoder.
>
> **Collections**
> Commons-Collections 提供一个类包来扩展和增加标准的 Java Collection框架
>
> **Configuration**
> Commons-Configuration 工具对各种各式的配置和参考文件提供读取帮助.
>
> **Daemon**
> 一种 unix-daemon-like java 代码的替代机制
>
> **DBCP**
> Commons-DBCP 提供数据库连接池服务
>
> **DbUtils**
> DbUtils 是一个 JDBC helper 类库，完成数据库任务的简单的资源清除代码.
>
> **Digester**
> Commons-Digester 是一个 XML-Java对象的映射工具，用于解析 XML配置文件.
>
> **Discovery**
> Commons-Discovery 提供工具来定位资源 (包括类) ，通过使用各种模式来映射服务/引用名称和资源名称。.
>
> **EL**
> Commons-EL 提供在JSP2.0规范中定义的EL表达式的解释器.
>
> **FileUpload**
> FileUpload 使得在你可以在应用和Servlet中容易的加入强大和高性能的文件上传能力
>
> **HttpClient**
> Commons-HttpClient 提供了可以工作于HTTP协议客户端的一个框架.
>
> **IO**
> IO 是一个 I/O 工具集
>
> **Jelly**
> Jelly是一个基于 XML 的脚本和处理引擎。 Jelly 借鉴了 JSP 定指标签，Velocity, Cocoon和Xdoclet中的脚本引擎的许多优点。Jelly 可以用在命令行， Ant 或者 Servlet之中。
>
> **Jexl**
> Jexl是一个表达式语言，通过借鉴来自于Velocity的经验扩展了JSTL定义的表达式语言。.
>
> **JXPath**
> Commons-JXPath 提供了使用Xpath语法操纵符合Java类命名规范的 JavaBeans的工具。也支持 maps, DOM 和其他对象模型。.
>
> **Lang**
> Commons-Lang 提供了许多许多通用的工具类集，提供了一些java.lang中类的扩展功能
>
> **Latka**
> Commons-Latka 是一个HTTP 功能测试包，用于自动化的QA,验收和衰减测试.
>
> **Launcher**
> Launcher 组件是一个交叉平台的Java 应用载入器。 Commons-launcher 消除了需要批处理或者Shell脚本来载入Java 类。.原始的 Java 类来自于Jakarta Tomcat 4.0 项目
>
> **Logging**
> Commons-Logging 是一个各种 logging API实现的包裹类.
>
> **Math**
> Math 是一个轻量的，自包含的数学和统计组件，解决了许多非常通用但没有及时出现在Java标准语言中的实践问题.
>
> **Modeler**
> Commons-Modeler 提供了建模兼容JMX规范的 Mbean的机制.
>
> **Net**
> Net 是一个网络工具集，基于 NetComponents 代码，包括 FTP 客户端等等。
>
> **Pool**
> Commons-Pool 提供了通用对象池接口，一个用于创建模块化对象池的工具包，以及通常的对象池实现.
>
> **Primitives**
> Commons-Primitives提供了一个更小，更快和更易使用的对Java基本类型的支持。当前主要是针对基本类型的 collection。.
>
> **Validator**
> The commons-validator提供了一个简单的，可扩展的框架来在一个XML文件中定义校验器 (校验方法)和校验规则。支持校验规则的和错误消息的国际化。

### 依赖

```java
        <dependency>
            <groupId>commons-net</groupId>
            <artifactId>commons-net</artifactId>
            <version>3.4</version>
        </dependency>
            
        <dependency>
            <groupId>org.apache.commons</groupId>
            <artifactId>commons-lang3</artifactId>
        </dependency>
            
        <dependency>
            <groupId>commons-codec</groupId>
            <artifactId>commons-codec</artifactId>
        </dependency>
            
        <dependency>
            <groupId>commons-digester</groupId>
            <artifactId>commons-digester</artifactId>
            <version>2.1</version>
        </dependency>
            
        <dependency>
            <groupId>commons-beanutils</groupId>
            <artifactId>commons-beanutils</artifactId>
            <version>1.9.4</version>
        </dependency>
            
        <dependency>
            <groupId>commons-fileupload</groupId>
            <artifactId>commons-fileupload</artifactId>
            <version>1.3.1</version>
        </dependency>
            
        <dependency>
            <groupId>commons-io</groupId>
            <artifactId>commons-io</artifactId>
            <version>2.4</version>
        </dependency>
            
        <dependency>
            <groupId>commons-logging</groupId>
            <artifactId>commons-logging</artifactId>
            <version>1.2</version>
        </dependency>
```

### 使用

> 基于commons-codec 实现UUID 生成工具类

```java
public class UuidUtil {
    
    //Id因子
    private static String[] chars = new String[] { "a", "b", "c", "d", "e", "f", "g", "h", "i", "j", "k", "l", "m", "n","o", "p", "q", "r", "s", "t", "u", "v", "w", "x", "y", "z", "0", "1", "2", "3", "4", "5", "6", "7", "8","9", "A", "B", "C", "D", "E", "F", "G", "H", "I", "J", "K", "L", "M", "N", "O", "P", "Q", "R", "S", "T","U", "V", "W", "X", "Y", "Z"
    };
    
    /**
	 * 获取uuid
	 * @return
	 */
	public static String get32UUID() {
		String uuid = UUID.randomUUID().toString().replaceAll("-", "");
		return uuid;
	}
	
	/**
	 * 基于8位的uuid,生成12位uuid
	 * @return
	 */
	public static String generateUuidF12c() {
		StringBuffer shortBuffer = new StringBuffer();
		String uuid = UUID.randomUUID().toString().replace("-", "");
		for (int i = 0; i < 8; i++) {
			String str = uuid.substring(i * 4, i * 4 + 4);
			int x = Integer.parseInt(str, 16);
			shortBuffer.append(chars[x % 0x3E]);
		}
		shortBuffer.append(shortBuffer.toString().substring(4));
		return shortBuffer.toString();
	}
	
	/**
	 * 获取数据表主键用的UUID(22位)
	 * @return String
	 */
	public static String getPkUuid() {
		String tempUuid = compressedUuid();
		if(tempUuid.indexOf("--") != -1){
			tempUuid = compressedUuid();
		}
		return tempUuid;
	}
	
    private static String compressedUuid() {
        UUID uuid = UUID.randomUUID();
        return compressedUUID(uuid);
    }
 
    private static String compressedUUID(UUID uuid) {
        byte[] byUuid = new byte[16];
        long least = uuid.getLeastSignificantBits();
        long most = uuid.getMostSignificantBits();
        long2bytes(most, byUuid, 0);
        long2bytes(least, byUuid, 8);
        String compressUUID = Base64.encodeBase64URLSafeString(byUuid);
        return compressUUID;
    }
 
    private static void long2bytes(long value, byte[] bytes, int offset) {
        for (int i = 7; i > -1; i--) {
            bytes[offset++] = (byte) ((value >> 8 * i) & 0xFF);
        }
    }
    
}

	//调用生成UUID
	for(int i = 1;i <= 20(个数);i++){
            System.out.println(UuidUtil.getPkUuid());
    }

```



## :bookmark_tabs:日志打印工具

### 简介

> SLF4J代表*Simple Logging Facade for Java*。它提供了Java中所有日志框架的简单抽象。因此，它使用户能够使用单个依赖项处理任何日志框架，例如：[Log4j](http://www.yiibai.com/log4j/)，Logback和JUL(`java.util.logging`)。可以在运行时/部署时迁移到所需的日志记录框架。

### 依赖

```xml
<dependency>
            <groupId>org.slf4j</groupId>
            <artifactId>slf4j-api</artifactId>
            <version>1.7.28</version>
</dependency>
```

### 使用

```java
//Controller层通用异常信息处理类
public class BaseController {
	
	protected final Logger logger = LoggerFactory.getLogger(this.getClass());
	@Autowired
	protected CommonUtil commonUtil;
	
	/**
	 * Controller层通用异常信息处理
	 * @param e
	 * @return String
	 */
	protected String doSimpleEXC(Exception e) {
		String errMsg = null;
	
	    errMsg = e.getMessage();
		
		logger.error("通用异常: " + errMsg, e);
        
		if (StringUtil.isNotBlank(errMsg)) {
			return "请求异常:" + errMsg + " & " + e.toString();
		} else {
			return "请求异常:" + e.toString();
		}
	}
	
}

//Controller层调用
public class XXXXController extends BaseController {
    public void xxx (Object x){
        logger.info("控制台日志打印信息:参数[{}]",x);
    }
}

```



## :gift:FastJsonUtils 工具类

### 简介：Json 返回处理

>包含：状态码(code)、数据(data)、消息(message)、时间(time)


### 依赖

```java
	<dependency>
			<groupId>com.alibaba</groupId>
			<artifactId>fastjson</artifactId>
			<version>1.2.83</version>
	</dependency>
```

## :leaves:SpringBoot 

### 注解

>@Resource  &  @AutoWired : @Autowired注入的时候要确保只有一个实现类 

### 父子项目搭建

> 父POM

``` xml
<?xml version="1.0" encoding="UTF-8"?>
<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
         xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 https://maven.apache.org/xsd/maven-4.0.0.xsd">
    <modelVersion>4.0.0</modelVersion>
    
    <!-- spring boot 依赖 -->
    <parent>
        <groupId>org.springframework.boot</groupId>
        <artifactId>spring-boot-starter-parent</artifactId>
        <version>2.2.6.RELEASE</version>
        <relativePath/> <!-- lookup parent from repository -->
    </parent>
    
    <!-- 父项目信息  -->
    <groupId>com.du.parent</groupId>
    <artifactId>com-du-parent-test</artifactId>
    <version>1.0.0</version>
    <name>com-du-parent-test</name>
    <description>XXXXXXXXX</description>
 
    <packaging>pom</packaging>
 	
    <!-- 子modules -->
    <modules>
        <module>spring-boot-child1</module>
        <module>spring-boot-child2</module>
        <module>spring-boot-child3</module>
    </modules>
 
    <!-- 版本控制 -->
    <properties>
        <java.version>1.8</java.version>
    </properties>
 	
    <!-- 依赖 -->
    <dependencies>
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter</artifactId>
        </dependency>
 
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter-test</artifactId>
            <scope>test</scope>
            <exclusions>
                <exclusion>
                    <groupId>org.junit.vintage</groupId>
                    <artifactId>junit-vintage-engine</artifactId>
                </exclusion>
            </exclusions>
        </dependency>
    </dependencies>
 
    <!-- 打包 -->
    <build>
        <plugins>
            <plugin>
                <groupId>org.springframework.boot</groupId>
                <artifactId>spring-boot-maven-plugin</artifactId>
            </plugin>
        </plugins>
    </build>
 
</project>
```

> 子POM

```xml
<?xml version="1.0" encoding="UTF-8"?>
<project xmlns="http://maven.apache.org/POM/4.0.0"
         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
         xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
    
    <!-- 父项目信息 -->
    <parent>
     	<groupId>com.du.parent</groupId>
    	<artifactId>com-du-parent-test</artifactId>
    	<version>1.0.0</version>
    </parent>
    
    <!-- 项目信息 -->
    <modelVersion>4.0.0</modelVersion>
    <artifactId>spring-boot-child1</artifactId>
    <name>spring-boot-child1</name>
	
    <!-- 版本控制 -->
    <properties>
        <project.build.sourceEncoding>UTF-8</project.build.sourceEncoding>
        <java.version>1.8</java.version>
    </properties>
	
    <!-- 依赖 -->
    <dependencies>
        <dependency>
            <groupId>org.springframework.boot</groupId>
            <artifactId>spring-boot-starter</artifactId>
        </dependency>
    </dependencies>
	
    <!-- 打包 -->
    <build>
        <plugins>
            <plugin>
                <groupId>org.springframework.boot</groupId>
                <artifactId>spring-boot-maven-plugin</artifactId>
                <configuration>
                    <fork>true</fork>
                    <layout>ZIP</layout>
                    <excludeGroupIds>

                    </excludeGroupIds>
                </configuration>
            </plugin>
        </plugins>
    </build>

</project>
```

### 项目打包

>  POM依赖加载

```xml
<build>
		<plugins>
			<!-- 打包的时候跳过测试junit -->
			<plugin>
				<groupId>org.apache.maven.plugins</groupId>
				<artifactId>maven-surefire-plugin</artifactId>
				<version>2.17</version>
				<configuration>
					<skip>true</skip>
				</configuration>
			</plugin>
			<!-- 打包的时候加入源码 -->
			<plugin>
				<groupId>org.apache.maven.plugins</groupId>
				<artifactId>maven-source-plugin</artifactId>
				<executions>
					<execution>
						<id>attach-sources</id>
						<goals>
							<goal>jar</goal>
						</goals>
					</execution>
				</executions>
			</plugin>
		</plugins>
</build>
```

> 打包操作

<img src="https://i.loli.net/2020/09/06/M1owGP85ADXZiaN.png" style="width: 800px;height: 700px">

> 修改打包类型

``` xml
<!-- 在POM文件中表头部分修改 -->
<groupId>com.dudu</groupId>
<artifactId>build-test</artifactId>
<name>build-test</name>
<version>1.0.0</version>
<packaging>jar</packaging>

<!--默认为jar方式-->
<packaging>jar</packaging>

<!--改为war方式-->
<packaging>war</packaging>
```



##  :leaves:SpringCloud 微服务

> 学习网站（CSDN） https://blog.csdn.net/weixin_38007185/article/details/108186254



## :page_with_curl:PageHelper(分页插件)

>官方说明文档：https://pagehelper.github.io/

### 依赖
```xml
<!-- pagehelper -->
<dependency>
	<groupId>com.github.pagehelper</groupId>
	<artifactId>pagehelper-spring-boot-starter</artifactId>
	<version>1.2.13</version>
</dependency>
```
### 调用

```java
PageInfo<实体类> pageInfo = XXXService.findPage方法(对象);

findPage方法(对象){
    int page = record.getPage();
    int rows = record.getRows();

    PageHelper.startPage(page,rows);
    List<实体类> 查询对象集合 = XXXMapper.查询方法(对象);
    return new PageInfo<>(查询对象集合);
}
```

## :gift:HuTool(Java工具包)

>官方文档  https://hutool.cn/

## :lock:Kaptcha (验证码生成)

### 依赖

```java
<!-- kaptcha验证码 -->
<dependency>
    <groupId>com.github.penggle</groupId>
    <artifactId>kaptcha</artifactId>
    <version>2.3.2</version>j
</dependency>
```

### KaptchaConfig配置类

```java
@Configuration
public class KaptchaConfig {
    @Bean
    public DefaultKaptcha getDefaultKaptcha(){
        DefaultKaptcha captchaProducer = new DefaultKaptcha();
        Properties properties = new Properties();
        properties.setProperty("kaptcha.border", "yes");
        properties.setProperty("kaptcha.border.color", "105,179,90");
        properties.setProperty("kaptcha.textproducer.font.color", "blue");
        properties.setProperty("kaptcha.image.width", "110");
        properties.setProperty("kaptcha.image.height", "40");
        properties.setProperty("kaptcha.textproducer.font.size", "30");
        properties.setProperty("kaptcha.session.key", "code");
        properties.setProperty("kaptcha.textproducer.char.length", "4");
        properties.setProperty("kaptcha.textproducer.font.names", "宋体,楷体,微软雅黑");
        Config config = new Config(properties);
        captchaProducer.setConfig(config);
        return captchaProducer;

    }
}
```

### 生成验证码
``` java
@Controller
public class CodeController {
    @Autowired
    private Producer captchaProducer ;

    @RequestMapping("/kaptcha")
    public void getKaptchaImage(HttpServletRequest request, HttpServletResponse response) throws Exception {
        HttpSession session = request.getSession();
        response.setDateHeader("Expires", 0);
        response.setHeader("Cache-Control", "no-store, no-cache, must-revalidate");
        response.addHeader("Cache-Control", "post-check=0, pre-check=0");
        response.setHeader("Pragma", "no-cache");
        response.setContentType("image/jpeg");
        //生成验证码
        String capText = captchaProducer.createText();
        session.setAttribute(Constants.KAPTCHA_SESSION_KEY, capText);
        //向客户端写出
        BufferedImage bi = captchaProducer.createImage(capText);
        ServletOutputStream out = response.getOutputStream();
        ImageIO.write(bi, "jpg", out);
        try {
            out.flush();
        } finally {
            out.close();
        }
    }
}
```

### 前端调用
```html
 <img src="/kaptcha" title="看不清，点击换一张！"onclick="this.src='/kaptcha?d='+new Date().getTime()" id="img">
```

## :chart_with_upwards_trend:基于POI的文件导出

## Excel

### 依赖    	

```java
		<dependency>
            <groupId>org.apache.poi</groupId>
            <artifactId>poi</artifactId>
            <version>3.17</version>
        </dependency>
```

### ExcelUtuls 工具类

```java
Public class ExcelUtils {
    
    //公共调用方法
    public static void exportCommon(HttpServletRequest request, HttpServletResponse response,List<Object[]> data)throws IOException{
            //封装对象属性
    //        List<Map<String, Object>> list = createExcelRecord(projects, keys);
            ByteArrayOutputStream os = new ByteArrayOutputStream();
            try {
                //将转换成的Workbook对象通过流形式下载
                createCommonWorkBook(data).write(os);
            } catch (IOException e) {
    //            e.printStackTrace();
                throw e;
            }
        	//下载Excel请求
            exportExcel(request,response,os);
    }
    
    //创建工作簿方法
    private static Workbook createCommonWorkBook(List<Object[]> data) {
        // 创建excel工作簿 xls格式
        //Workbook wb = new HSSFWorkbook();
        //创建excel工作簿 xlsx格式
        Workbook wb = new XSSFWorkbook();

        //时间格式化
        SimpleDateFormat sdf= new SimpleDateFormat("yyyy-MM-dd");

        // 创建第一个sheet（页），并命名
        Sheet sheet = wb.createSheet("Sheet1");

        Object[] columnNames = data.get(0);

        // 手动设置列宽。第一个参数表示要为第几列设；，第二个参数表示列的宽度，n为列高的像素数。
        for (int i = 0; i < columnNames.length; i++) {
            if(i==0){
                sheet.setColumnWidth((short) i, (short) (20 * 150));
            }else{
                sheet.setColumnWidth((short) i, (short) (40 * 150));
            }
        }

        // 创建第一行
        Row row = sheet.createRow((short) 0);

        // 创建两种单元格格式
        CellStyle columnCellStyle = wb.createCellStyle();
        CellStyle dataCellStyle = wb.createCellStyle();

        // 创建两种字体
        Font columnFont = wb.createFont();
        Font dataFont = wb.createFont();

        // 创建第一种字体样式（用于列名）
        columnFont.setFontHeightInPoints((short) 12);
        columnFont.setColor(IndexedColors.BLACK.getIndex());
        columnFont.setBold(true);
        columnFont.setFontName("宋体");

        // 设置第一种单元格的样式（用于列名）
        columnCellStyle.setFont(columnFont);
        columnCellStyle.setBorderLeft(BorderStyle.THIN);
        columnCellStyle.setBorderRight(BorderStyle.THIN);
        columnCellStyle.setBorderTop(BorderStyle.THIN);
        columnCellStyle.setBorderBottom(BorderStyle.THIN);
        columnCellStyle.setAlignment(HorizontalAlignment.CENTER);
        columnCellStyle.setVerticalAlignment(VerticalAlignment.CENTER);
        columnCellStyle.setWrapText(true);

        // 创建第二种字体样式（用于值）
        dataFont.setFontHeightInPoints((short) 10);
        dataFont.setColor(IndexedColors.BLACK.getIndex());
        dataFont.setFontName("宋体");

        // 设置第二种单元格的样式（用于值）
        dataCellStyle.setFont(dataFont);
        dataCellStyle.setBorderLeft(BorderStyle.THIN);
        dataCellStyle.setBorderRight(BorderStyle.THIN);
        dataCellStyle.setBorderTop(BorderStyle.THIN);
        dataCellStyle.setBorderBottom(BorderStyle.THIN);
        dataCellStyle.setAlignment(HorizontalAlignment.CENTER);
        dataCellStyle.setVerticalAlignment(VerticalAlignment.CENTER);
        dataCellStyle.setWrapText(true);
        
        //设置列名
        for (int i = 0; i < columnNames.length; i++) {
            Cell cell = row.createCell(i);
            cell.setCellValue(columnNames[i].toString());
            cell.setCellStyle(columnCellStyle);
        }

        //设置每行每列的值
        for (short i = 1; i < data.size(); i++) {
            // Row 行,Cell 方格 , Row 和 Cell 都是从0开始计数的
            // 创建一行，在页sheet上
            Row dataRow = sheet.createRow((short) i);
            dataRow.setHeight((short) 600);

            Object[] objArray = data.get(i);

            // 在row行上创建一个方格
            for (short j = 0; j < objArray.length; j++) {

                Cell cell = dataRow.createCell(j);
                cell.setCellStyle(dataCellStyle);

                if (objArray[j] == null) {
                    cell.setCellValue("");
                }else{
                    cell.setCellValue(objArray[j].toString());
                }
            }
        }
        return wb;
    }
    
    //下载Excel请求
    public static void exportExcel(HttpServletRequest request, HttpServletResponse response, ByteArrayOutputStream os) throws IOException {

        byte[] content = os.toByteArray();
        InputStream is = new ByteArrayInputStream(content);

        // 设置response参数，可以打开下载页面
        response.reset();
        response.setContentType("application/vnd.ms-excel;charset=utf-8");
//      response.setHeader("Content-Disposition", "attachment;filename=" + encodeFileName(fileName, request));
        ServletOutputStream out = response.getOutputStream();
        BufferedInputStream bis = null;
        BufferedOutputStream bos = null;
        try {
            bis = new BufferedInputStream(is);
            bos = new BufferedOutputStream(out);
            byte[] buff = new byte[2048];
            int bytesRead;
            while (-1 != (bytesRead = bis.read(buff, 0, buff.length))) {
                bos.write(buff, 0, bytesRead);
            }
        } catch (final IOException e) {
            throw e;
        } finally {
            if (bis != null){
                bis.close();
            }
            if (bos != null){
                bos.close();
            }
        }
    }
    
}   
```

### 业务操作

```java
private void exportExcel (List<类型> 数据List,HttpServletRequest request, HttpServletResponse response){
    
    //用来存储列表数据
    List<Object[]> dataList = new ArrayList<>();
    
    //设置列名
    dataList.add(new Object[]{
        "列名1",
        "列名2",
        .......
    });
    
    //设置内容
    for(实体类 变量 : 数据List){
     dataList.add(new Object[]{
       // "序号",
       i++,
       变量.属性,
       ......
    }
    
   	//调用导出
    ExcelUtils.exportCommon(request,response,dataList);
    
}
```

## Word

### 根据Word模板导出

>  查看 Github ==> easyTools工具包 

## PDF

> 基于 itextpdf 导出

### 依赖

```xml
  <dependency>
      <groupId>com.itextpdf</groupId>
      <artifactId>itextpdf</artifactId>
      <version>5.5.13.3</version>
  </dependency>
      
  <dependency>
      <groupId>com.itextpdf</groupId>
      <artifactId>itext-asian</artifactId>
      <version>5.2.0</version>
  </dependency>
```

### 使用介绍

> 官方文档： https://kb.itextpdf.com/home/it7kb/ebooks

> 别人的说明：https://www.cnblogs.com/ssslinppp/p/4976922.html







# :floppy_disk:SQL 小芝士

## 查询字段的使用
> 通过Java操作字段，完成对XML查询条件的限制

   1.当实体对象使用 @Table(name="数据库表名") 绑定时，使用 @Transient 忽略字段

2. 设置  noBageRange 字段、orderField 字段、orderType字段（举例）；

3. 对 noBageRange、orderType  进行操作：如 ，noBageRange = “ 3”；orderField = " ISNULL(限制条件),限制条件"; orderType =" desc";

4. XML文件使用字段进行查询限制：

   ```sql
   <if test="model.noBageRange != null and !''.equals(model.noBageRange)">
                   and range < #{model.noBageRange}
   </if>
   
   <if test="model.orderField != null and !''.equals(model.orderField)">
               ${model.orderField} ${model.orderType},
   </if>
   ```

   


## XML文件查询条件

> Mapper 方法 ： 

	返回类型  方法名 (@Param("model") 类型 对象名 );

:star2: 单对象属性判断( 使用 model 代替变量对象)

```xml
	<if test="model.属性名 条件">
	and 表字段名 = #{model.属性}
	</if>
```


:star2: 对象集合属性判断( 使用 model 代替变量对象)

```xml
<if test="model.对象集合名 条件 ">

	and 表字段名 in

	<foreach collection="model.集合" item="属性" index="index" separator="," open="(" close=")">``

    #{属性}

    </foreach>

</if>
```


## 模板SQL操作

>导入依赖

```java
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

```java
	public interface SQLMapper<T>{

		@Options(keyProperty = "主键",keyColumn = "数据库字段名")

		//绑定SQL模板
		@InsertProvider( type = 模板.class, method = "dynamicSQL")

		//方法
		int batchInsert(List<T> list);

	}

```

>SQL模板

```java
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


# :coffee:咖啡 小芝士

## List 集合操作

>将目标List集合分组

```java
List<类型> applyTypeList = list.stream().map(实体类 :: 条件).distinct().collect(Collectors.toList());
```

>从List集合中去除元素(会修改List)

```java
BoList.removeIf(e -> Strings.isNullOrEmpty(e.getProjectCode()));
```

>List集合元素排序

```java
//根据 ProjectCode 逆序（需生成新的List）

List<PlanAppraiseBo> sortList = value.stream().sorted(Comparator.comparing(PlanAppraiseBo::getProjectCode).reversed()).collect(Collectors.toList());
```

>List集合过滤(不修改List)

```java
  private List<Integer> integers = Lists.list(30, 40, 10, 20);

  Set<Integer> collect = integers.stream().filter(i -> i > 20).collect(Collectors.toSet());

  assertEquals(Sets.newTreeSet(30, 40), collect);

```

## Map集合操作

>将List分组转化为Map

```java
Map<类型, List<类型>> map1 = List1.stream().collect(Collectors.groupingBy(实体类 :: 条件属性));
```
>将List根据条件转换为Map

```java
Map<String, 实体类> voteMap  = allVoteList.stream().collect(Collectors.toMap(实体::条件, item -> item));
```


>Map集合遍历

```java
   for (Map.Entry<类1, List<类2>> entry : map集合.entrySet()) {

     List<类2> value = entry.getValue();

   }
```


## String 字符串

>字符串截取

```java
String S1 = S2.substring(S2.length() - 保留位数);
```

>数字补位

```java
// 0 - 补充数； 3 - 补充位数； d - 实数；
String.format("%03d",num)     
```

>equals

```java
常量.equals(变量)    //防止出现空指针异常
```

>字符串划分

:star2:  split()

``` java
//语法 (regex - 正则表达式分隔符；limit - 分割的份数)
 public String[] split(String regex, int limit)
```

:star2: indexOf()

```java
//形式：

//返回指定字符在字符串中第一次出现处的索引，如果此字符串中没有这样的字符，则返回 -1。
public int indexOf(int ch)

//返回从 fromIndex 位置开始查找指定字符在字符串中第一次出现处的索引，如果此字符串中没有这样的字符，则返回 -1。
public int indexOf(int ch, int fromIndex) 

//返回指定字符在字符串中第一次出现处的索引，如果此字符串中没有这样的字符，则返回 -1。
int indexOf(String str)

//返回从 fromIndex 位置开始查找指定字符在字符串中第一次出现处的索引，如果此字符串中没有这样的字符，则返回 -1。
int indexOf(String str, int fromIndex)

//语法:
ch - 字符，Unicode 编码;
fromIndex - 开始搜索的索引位置，初始为0;
str -- 要搜索的子字符串。

public int indexOf(int ch )

public int indexOf(int ch, int fromIndex)

int indexOf(String str)

int indexOf(String str, int fromIndex)

```



## Lambda 表达式 ( -> )

### 简介

> “强调做什么 而不是以什么形式做”

### 格式

```java
//标准格式：
(参数类型 参数名称) ‐> { 代码语句 }

//省略格式：
可省略的内容：
1.参数列表：括号中参数列表的数据类型可以省略不写 (因为在接口里已经定义了类型);
2.参数列表：括号中的参数如果只有一个 那么类型和()都可以省略;
3.代码：如果{}中的代码只有一行 那么无论是否有返回值 可以省略{}和return和分号(但要省略必须一起省略);
```

### 使用

> 1. 无参无返回值

```java
// 调用invokeCook()方法 传递Cook接口的匿名内部类对象
        invokeCook(new Cook() {
            @Override
            public void makeFood() {
                System.out.println("开饭了");
            }
        });

        // 使用Lambda表达式简化匿名内部类的书写
        invokeCook(() -> {
            System.out.println("开饭了");
        });
```

> 2.有参数有返回值

```java
实体对象类：
       // 升序操作
        Arrays.sort(arr, new Comparator<Person>() {
            @Override
            public int compare(Person o1, Person o2) {
                return o1.getAge()-o2.getAge();
            }
        });

        // 使用Lambda表达式简化匿名内部类的书写
        Arrays.sort(arr,(Person o1, Person o2) -> {
            return o1.getAge()-o2.getAge();
        });

计算类：
     // 调用方法 参数是一个接口 可以使用匿名内部类
        invokeCalc(1, 2, new Calculate() {
            @Override
            public int calc(int a, int b) {
                return a+b;
            }
        });

        // 使用Lambda表达式简化匿名内部类的书写
        invokeCalc(1,2,(int a,int b) -> {
            return a+b;
        });
```





## 实体类

### 分类

>BO类 ： 业务类   进行业务设计，extends 实体类

>VO类 ： 视图类   显示属性包含的类 

### 注意事项

1.实体类序列化

> ​	序列化：eg: 将实体对象转化为Json对象；
>
> ​	反序列化：eg : 将Json转化为实体对象；

1.1 作用

>控制版本是否兼容
>
>若认为修改的 实体对象 是向后兼容的，则不修改 serialVersionUID；反之修改；

1.2 使用

```java
//方式一
//根据包名，类名，继承关系，非私有的方法和属性，以及参数，返回值等诸多因子计算得出的，极度复杂生成的一个64位的哈希字段
private static final long serialVersionUID = -3681388653357478350L;
```

```java
//方式二
//默认的1L
private static final long serivalVersionUID = 1L;
```

1.2 自动生成 （IDEA设置）

1）settings  ==>  serializable ==> 勾选 ：Serializable class without 'serialVersionUID'  + 'serialVersionUID' field not declared 'private static final long'

2）设置之后，选中对应的类名，然后按 alt+enter 快捷键  ==>  add 'serialVersionUID' field

## 线程

>多线程塞入流程相关数据

```java
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
