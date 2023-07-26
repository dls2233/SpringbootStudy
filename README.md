#总结：
1.maven：Maven是专门用于管理和构建Java项目的工具，建出的maven项目是通用的。
2.功能：提供了一套标准化的项目结构，提供了一套标准化的构建流程（编译，测试，打包，发布……），提供了一套依赖管理机制。
4.maven对项目构建的生命周期:clean:清理工作,default:核心工作，包括编译、测试、打包、安装、部署等,site:产生报告，发布站点
5.依赖管理：在pom.xml中
6.坐（资源的唯一标识）主要构成如下：
groupId：定义当前Maven项目隶属组织名称（通常是域名反写，例如：org.springframework.boot）
artifactId：定义当前Maven项目名称（通常是模块名称，例如 movie-service、user-service） 
version：定义当前项目版本号
7.JSON：适用于进行数据交互的场景，如网站前台与后台之间的数据交互。
8.json是以键值对进行书写的，而具体的语法如下:
数组（Array）用方括号(“[]”)表示。
对象（0bject）用大括号(“{}”)表示。
名称/值对(name/value）组合成数组和对象。
名称(name）置于双引号中，值（value）有字符串、数值、布尔值、null、对象和数组。
并列的数据之间用逗号(“,”）分隔
9.springboot:快速地基于spring进行java应用开发。
10.yaml/yml:YAML，一种数据序列化格式。具有容易阅读、容易与脚本语言交互、以数据为核心，重数据轻格式的特点。
11.yaml的语法格式如下:
大小写敏感
属性层级关系使用多行描述，每行结尾使用冒号结束
使用缩进表示层级关系，同层级左侧对齐，只允许使用空格（不允许使用Tab键）
==属性值前面添加空格（属性名与属性值之间使用冒号+空格作为分隔）==
 #号 表示注释
12Mybatis：持久层框架，用于简化 JDBC 开发
13.Java概念与数据库概念：类与表，属性与字段/列，对象与记录/行一一对应
14.映射文件：使用mybatis的映射文件mapper并在其中编写sql语句进行代理开发，这能较好地解决原生的硬编码和后期维护问题。
映射文件中的namespace与接口全类名的相同
映射文件中编写sql语句的标签id属性与mapper接口中的方法名保持一致
15.收集数据的方法：
  1. 如果查询出的数据只有一条，可以通过
    1. 实体类对象接收
    2. List集合接收
    3. Map集合接收，结果{password=123456, sex=男, id=1, age=23, username=admin}
  2. 如果查询出的数据有多条，一定不能用实体类对象接收，会抛异常TooManyResultsException，可以通过
    1. 实体类类型的LIst集合接收
    2. Map类型的LIst集合接收
    3. 在mapper接口的方法上添加@MapKey注解
16.resultMap：自定义映射，用于一对多或多对一或字段名和属性名不一致的情况
17.resultMap中常用属性
  resultMap标签:
  id：表示自定义映射的唯一标识，不能重复
  type：查询的数据要映射的实体类的类型  
  子标签：  
  id：设置主键的映射关系  
  result：设置普通字段的映射关系  
  子标签属性：  
  property：设置映射关系中实体类中的属性名  
  column：设置映射关系中表中的字段名
18.@Param来自定义属性名称,然后就可以在映射文件中使用自定义属性名进行接收了
13.starter:是springboot为了简化开发时引依赖的过程而整出的一类"整合包"。
14.@Componet:用来标注一个类，将该类填装到spring容器中
15.@Autowired：自动填装
16.@Configuration&@Bean：spring的配置类。
17.@Service：这个注解主要是标注到业务逻辑层上，将其注入到spring容器中，方便将其注入到其他类中(例如controller)。本质上还是一个@Component。
18.@Mappep；由mybatis提供，该spring容器由mybatis实现该接口，并让mybatis找到它，为该接口生成实现类，并最终放到spring容器中。
