# 办公系统(二次开发)

#### 安装教程

1.  mvn install lib/目录中的jar 文件拷贝到D盘根目录下，
		mvn install:install-file -DgroupId=com.zhuozhengsoft -DartifactId=pageoffice -Dversion=4.6.0.4 -Dpackaging=jar -Dfile=d:/pageoffice4.6.0.4.jar  
		mvn install:install-file -DgroupId=com.oracle -DartifactId=ojdbc8 -Dversion=12.2.0.1 -Dpackaging=jar -Dfile=D:\ojdbc8.jar  
		mvn install:install-file -DgroupId=dm -DartifactId=dm.jdbc.driver -Dversion=1.8.0 -Dpackaging=jar -Dfile=D:\DmJdbcDriver18.jar  
		mvn install:install-file -DgroupId=com.kingbase8 -DartifactId=pgjdbc-core-parent -Dversion=1.1.2 -Dpackaging=jar -Dfile=D:\kingbase8-8.2.0.jar  
		mvn install:install-file -DgroupId=com.dingtalk.open -DartifactId=taobao-sdk-java-auto -Dversion=1479188381469-20200218 -Dpackaging=jar -Dfile=D:\taobao-sdk-java-auto_1479188381469-20200218.jar  
		mvn install:install-file -DgroupId=cyunsoft.common -DartifactId=cyunsoft-common -Dversion=0.0.1-SNAPSHOT -Dpackaging=jar -Dfile=d:/cyunsoft-common-0.0.1-SNAPSHOT.jar  
		mvn install:install-file -DgroupId=cyunsoft.bean -DartifactId=cyunsoft-bean -Dversion=0.0.1-SNAPSHOT -Dpackaging=jar -Dfile=d:/cyunsoft-bean-0.0.1-SNAPSHOT.jar  
		mvn install:install-file -DgroupId=cyunsoft.coreservice -DartifactId=cyunsoft-coreservice -Dversion=0.0.1-SNAPSHOT -Dpackaging=jar -Dfile=d:/cyunsoft-coreservice-0.0.1-SNAPSHOT.jar  
		mvn install:install-file -DgroupId=cyunsoft.bi -DartifactId=cyunsoft-bi -Dversion=0.0.1-SNAPSHOT -Dpackaging=jar -Dfile=d:/cyunsoft-bi-0.0.1-SNAPSHOT.jar  
		mvn install:install-file -DgroupId=cyunsoft.imservice -DartifactId=cyunsoft-imservice -Dversion=0.0.1-SNAPSHOT -Dpackaging=jar  -Dfile=d:/cyunsoft-imservice-0.0.1-SNAPSHOT.jar  		
		开发环境正常启动后用jasperreports-6.12.2.jar 替换仓库中的jasperreports-6.12.2.jar，否则BI报表会出现中文乱码
2.  配置数据库信息
src/main/resources/application.properties
```
jdbc.driverClassName=org.apache.derby.jdbc.ClientDriver
jdbc.url=jdbc:derby://94.74.94.246:3306/UnionDB;create=true
jdbc.username=root
jdbc.password=PrieiXed1w

```
3.  安装MYSQL8.0.21版本 后导入lib/mysql.sql
4.  运行cyunsoft-appservice中的AppGo.java 即可启动项目。
注：sigar-x86-winnt.dll文件拷贝到工程所用的jdk和jre的bin目录。
项目启动时需要d:/cyunsoft/attach和d:/cyunsoft/lic目录，建议事件下载安装测试版，一切需求的目录与静态文件都有了。
工程项目启动时会报ORCALE驱动文件缺少的错误。安提示在ORCALE安装目录中查找，并放到相应的位置。
工程项目启动成功后，在登陆系统时提示长不以指定的实体类时，请去除SpringBoot的热部署功能，再次启动即可。

#### 远程协同开发
远程在家办公的童鞋可以使用VPN连接内网，账户密码运维已通过邮箱发送给各位项目组的铜须:
1.打开docs/UnionPayVPNConnect.exe
3.详情参考docs目录下的信息中心VPN使用手册。