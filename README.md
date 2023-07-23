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
