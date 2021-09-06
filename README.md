### 项目概述
:+1:*学生管理系统 : 对学生各种信息进行日常管理，如查询、修改、增加、删除等

主要功能 ：  
一、可以对学生、教师、班级、年级、管理员进行如下操作  
    (1).根据名字查询  
    (2).添加  
    (3).修改  
    (4).删除  
  
二、修改登录密码  
  
三、支持对学生、教师信息按班级名称分页显示、对班级信息按年级名称分页显示  

其他功能 ：便捷的导航菜单和标签页、验证码安全登录、提交前验证信息


:key:*数据库中默认的管理员身份信息 : 账户名 : `钟荣伟` , 密码 `123`*


### 开发环境
| 工具    | 版本或描述                |    
| ------- | ------------------------ |    
| `OS`    | Windows 10               | 
| `JDK`   |  1.8                     |    
| `IDE`   | IntelliJ IDEA 2021.6     |    
| `Maven` | 3.6.0                    |    
| `MySQL` | 8.0.11                   |



### 用户权限介绍
- *管理员 : 具有所有管理模块的操控权限*
- *教师 : 具有学生信息管理模块的所有权限,且在教师信息管理模块中具有查询及添加信息的权限*
- *学生 : 具有学生信息管理模块的查询及添加信息的权限*
- *其他 : 所有用户都可以修改自己的登录信息，如密码*


### 项目截图 (`管理员身份登录`)
- *用户登录页面*

![](https://github.com/ZhongRongWei/SMS/blob/master/demonstration_picture/%E7%99%BB%E5%BD%95%E7%95%8C%E9%9D%A2.JPG)

- *欢迎页面*

![](https://github.com/ZhongRongWei/SMS/blob/master/demonstration_picture/%E6%AC%A2%E8%BF%8E%E9%A1%B5%E9%9D%A2.JPG)

- *学生信息管理页面*

![](https://github.com/ZhongRongWei/SMS/blob/master/demonstration_picture/%E5%AD%A6%E7%94%9F%E7%AE%A1%E7%90%86.JPG)

- *教师信息管理页面*

![](https://github.com/ZhongRongWei/SMS/blob/master/demonstration_picture/%E6%95%99%E5%B8%88%E7%AE%A1%E7%90%86.JPG)

- *班级信息管理页面*

![](https://github.com/ZhongRongWei/SMS/blob/master/demonstration_picture/%E7%8F%AD%E7%BA%A7%E7%AE%A1%E7%90%86.JPG)

- *年级信息管理页面*

![](https://github.com/ZhongRongWei/SMS/blob/master/demonstration_picture/%E5%B9%B4%E7%BA%A7%E7%AE%A1%E7%90%86.JPG)


- *管理员信息管理页面*

![](https://github.com/ZhongRongWei/SMS/blob/master/demonstration_picture/%E7%AE%A1%E7%90%86%E5%91%98.JPG)

- *个人信息管理页面*

![](https://github.com/ZhongRongWei/SMS/blob/master/demonstration_picture/%E4%B8%AA%E4%BA%BA%E4%BF%A1%E6%81%AF%E7%AE%A1%E7%90%86.JPG)


### 项目截图 (`教师身份登录`)
- *教师仅具有学生信息管理模块的所有权限,且在教师信息管理模块中只具有查询及添加信息的权限*
![](https://github.com/ZhongRongWei/SMS/blob/master/demonstration_picture/%E6%95%99%E5%B8%88%E7%99%BB%E5%BD%95.JPG)


### 项目截图 (`学生身份登录`)
- *学生仅具有学生信息管理模块的查询及添加信息的权限*
![](https://github.com/ZhongRongWei/SMS/blob/master/demonstration_picture/%E5%AD%A6%E7%94%9F%E7%99%BB%E5%BD%95.JPG)


### 项目结构
```
├─src
│  └─main
│      ├─java
│      │  └─pers
│      │      └─huangyuhui
│      │          └─sms
│      │              ├─bean
│      │              ├─controller
│      │              ├─dao
│      │              ├─interceptor
│      │              ├─service
│      │              │  └─impl
│      │              └─util
│      ├─resource
│      │  ├─database-conf
│      │  ├─mapper
│      │  ├─mybatis-conf
│      │  └─spring-conf
│      └─webapp
│          ├─image
│          │  └─portrait
│          ├─static
│          │  ├─easyui
│          │  │  ├─css
│          │  │  ├─js
│          │  │  └─themes
│          │  │      ├─default
│          │  │      │  └─images
│          │  │      ├─icons
│          │  │      ├─locale
│          │  │      └─metro
│          │  │          └─images
│          │  └─h-ui
│          │      ├─css
│          │      ├─images
│          │      │  └─gq
│          │      ├─js
│          │      ├─lib
│          │      │  ├─Hui-iconfont
│          │      │  │  └─1.0.1
│          │      │  ├─icheck
│          │      │  └─jquery
│          │      │      └─1.9.1
│          │      └─skin
│          │          └─default
│          └─WEB-INF
│              └─view
│                  ├─admin
│                  ├─clazz
│                  ├─common
│                  ├─error
│                  ├─grade
│                  ├─student
│                  ├─system
│                  └─teacher


```

#### 项目文件说明-`数据库文件`
```
ssm_sms.sql
```

#### 项目文件说明-`数据库配置信息`
```
c3p0.properties
```

#### 项目文件说明-`Spring 核心配置文件`
```
applicationContext.xml
```

#### 项目文件说明-`Spring MVC 核心配置文件`
```
springmvc-config.xml
```

#### 项目文件说明-`MyBatis 核心配置文件`
```
mybatis-config.xml
```

#### 项目文件说明-`Mapper 接口映射文件`
```
mapper/
```

#### 数据库ER图
![](https://github.com/ZhongRongWei/SMS/blob/master/demonstration_picture/ER%E5%9B%BE.JPG)

#### Jar包依赖关系图
![](https://github.com/ZhongRongWei/SMS/blob/master/demonstration_picture/jar%E5%8C%85%E4%BE%9D%E8%B5%96%E5%9B%BE.jpg)

