# Vue_SpringBoot_Demo
## Tech Stack
### Front End
- Vue.js
- Element
- axios
### Back End
- SpringBoot
### DataBase
- MySQL
- Redis


## How to run
### Server
1. Open `spring-demo` in Iintellij IDEA
2. Reload project (right click on `pom.xml` and chose `Maven`)
3. Run `/src/main/java/com.example.vuedemo/VuedemoApplication`

### Front End
1. Open `vue-demo`
2. Run `npm run dev` in terminal

## Screenshot
### Login Page
[![Dxyf1g.png](https://s3.ax1x.com/2020/12/07/Dxyf1g.png)](https://imgchr.com/i/Dxyf1g)

### Success
[![DxyO9U.png](https://s3.ax1x.com/2020/12/07/DxyO9U.png)](https://imgchr.com/i/DxyO9U)

*Some codes in the blog need to be changed*

1.pom.xml
```
		<!-- 测试支持 -->
		<dependency>
			<groupId>org.junit.jupiter</groupId>
			<artifactId>junit-jupiter-api</artifactId>
			<version>5.7.0</version>
			<scope>test</scope>
		</dependency>
```

2.mysql 8.0以上的要在pom.xml下更新dependence jar包,还有application.properties下com.mysql.jdbc.Driver改为com.mysql.cj.jdbc.Driver

3.pom.xml中依赖的mysql-connector-java版本号要改成5.1.46，不然在编译后端程序时会有很多数据库连接错误

4.application.properties设置的url也需要更新，经过多次尝试下面这个版本OK：

Repalce `db_name` with your db name
```
spring.datasource.url=jdbc:mysql://127.0.0.1:3306/<db_name>?characterEncoding=UTF-8&serverTimezone=GMT%2B8&useSSL=false
```


## Learn from

1. [Vue + Spring Boot 项目实战](https://blog.csdn.net/Neuf_Soleil/article/details/88925013)
2. [Building a RESTful Web Service](https://spring.io/guides/gs/rest-service/)