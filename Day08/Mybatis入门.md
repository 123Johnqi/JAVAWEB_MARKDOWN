# Mybatis入门

## 什么是Mybatis

![](images/2024-06-04-19-50-20.png)

## 入门程序

![](images/2024-06-04-19-52-39.png)

## 数据库连接

![](images/2024-06-04-19-55-17.png)

* Driver：数据库驱动，MySQL为数据库驱动类的类名，若需连接MySQL数据库，则数据库的类名是固定的，为：com.mysql.cj.jdbc.Driver
* URL：
  * jdbc:mysql://是协议部分，是固定的；
  * localhost:3306代表了要连接的是哪个数据库服务器，表示本机的3306端口
  * mybatis表示要连接哪个数据库


### 数据库连接四要素

application.properties文件：

![](images/2024-06-04-19-53-21.png)

