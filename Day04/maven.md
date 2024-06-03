# maven

## maven作用

![](images/2024-05-02-16-43-23.png)

## 配置maven环境

配置idea的maven设置

![](images/2024-05-05-21-57-37.png)

### idea创建maven项目

![](images/2024-05-05-21-58-20.png)

### maven坐标

![](images/2024-05-05-21-58-49.png)

* groupId：是公司项目组唯一的标识符，也是对应Java的包的结构（main目录里Java的目录结构）。 groupId分为几个字段，例如org.springframework.boot，前面的org叫【域】，后面是域名。

域又分为org、com、cn等等许多，其中org为非营利组织，com为商业组织，cn代表域为中国

apache公司的tomcat项目例子：项目的groupId是org.apache，它的域是org，公司名称是apache，artifactId是tomcat

* artifactId：是项目组中的某模块的唯一的标识符，实际对应小项目的名称。artifactId一般是项目名或者模块名。

* version：指定了项目的当前版本，SNAPSHOT意为快照，Release版本则代表稳定的版本。

* name：声明了一个对于用户更为友好的项目名称，不是必须的，推荐为每个pom声明name，以方便信息交流。

>包名（package name）一般是group id+artifact id


### 导入maven项目

![](images/2024-05-05-22-05-30.png)

![](images/2024-05-05-22-05-49.png)

## 依赖管理

### 依赖配置

![](images/2024-05-05-22-39-49.png)

### 依赖传递

依赖具有传递性

![](images/2024-05-05-22-43-11.png)

#### 排除依赖

![](images/2024-05-05-22-44-56.png)

### 依赖范围

![](images/2024-05-05-22-50-02.png)

打包范围无效指的是打包以后，不会将无效的jar包放在文件夹中

### 生命周期

![](images/2024-05-05-22-58-25.png)

![](images/2024-05-05-22-58-46.png)


 maven的install可以将项目本身编译并打包到本地仓库，这样其他项目引用本项目的jar包时不用去私服上下载jar包，直接从本地就可以拿到刚刚编译打包好的项目的jar包，很灵活，避免每次都需要重新往私服发布jar包的痛苦。

![](images/2024-05-05-22-59-14.png)

> 执行clean后面的阶段时，clean并不会执行，因为clean和后面的不属于同一套生命周期

#### 执行生命周期的方式

![](images/2024-05-05-22-57-30.png)

>maven是基于插件的框架，因此所有生命周期本质上都是使用插件完成的

若想跳过某个阶段不执行，可在idea中点击“小闪电”跳过