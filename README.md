# JSP
## JSP 语法
### 脚本程序
_脚本程序可以包含任意量的Java语句、变量、方法或表达式，只要它们在脚本语言中是有效的。脚本程序的语法格式:_

`<% 代码片段 %>`

### 中文编码问题
_如果我们要在页面正常显示中文，我们需要在 JSP 文件头部添加以下代码：

`<%@ page language="java" contentType="text/html; charset=UTF-8" pageEncoding="UTF-8"%>`

## JSP声明
_一个声明语句可以声明一个或多个变量、方法，供后面的Java代码使用。在JSP文件中，您必须先声明这些变量和方法然后才能使用它们。JSP声明的语法格式：_

`<%! declaration; [ declaration; ]+ ... %>`

_程序示例：_

```
<%! int i = 0; %> 
<%! int a, b, c; %> 
<%! Circle a = new Circle(2.0); %> 
```

## JSP表达式
_一个JSP表达式中包含的脚本语言表达式，先被转化成String，然后插入到表达式出现的地方。由于表达式的值会被转化成String，所以您可以在一个文本行中使用表达式而不用去管它是否是HTML标签。表达式元素中可以包含任何符合Java语言规范的表达式，但是不能使用分号来结束表达式。JSP表达式的语法格式：_

`<%= 表达式 %>`

_同样，您也可以编写与之等价的XML语句：_

```
<jsp:expression>
   表达式
</jsp:expression>
```
_程序示例：_
``````````````
<%@ page language="java" contentType="text/html; charset=UTF-8"
    pageEncoding="UTF-8"%>
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8">
<title>菜鸟教程(runoob.com)</title>
</head>
<body>
<p>
   今天的日期是: <%= (new java.util.Date()).toLocaleString()%>
</p>
</body> 
</html> 
``````````````

## JSP注释
_JSP注释主要有两个作用：为代码作注释以及将某段代码注释掉。JSP注释的语法格式：_

```````
<body>
<%-- 该部分注释在网页中不会被显示--%> 
<p>
   今天的日期是: <%= (new java.util.Date()).toLocaleString()%>
</p>
</body> 
</html> 
```````
## JSP表达式
_一个JSP表达式中包含的脚本语言表达式，先被转化成String，然后插入到表达式出现的地方。由于表达式的值会被转化成String，所以您可以在一个文本行中使用表达式而不用去管它是否是HTML标签。表达式元素中可以包含任何符合Java语言规范的表达式，但是不能使用分号来结束表达式。_
_JSP表达式的语法格式：_

`<%= 表达式 %>`

_程序示例：_

``````````````
<%@ page language="java" contentType="text/html; charset=UTF-8"
    pageEncoding="UTF-8"%>
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8">
<title>菜鸟教程(runoob.com)</title>
</head>
<body>
<p>
   今天的日期是: <%= (new java.util.Date()).toLocaleString()%>
</p>
</body> 
</html> 
``````````````

## JSP 指令
_JSP指令用来设置整个JSP页面相关的属性，如网页的编码方式和脚本语言。语法格式如下：_

`<%@ directive attribute="value" %>`

_指令可以有很多个属性，它们以键值对的形式存在，并用逗号隔开。_
_JSP中的三种指令标签：_

`<%@ page ... %>	      定义网页依赖属性，比如脚本语言、error页面、缓存需求等等'
`<%@ include ... %>	   包含其他文件`
`<%@ taglib ... %>	   引入标签库的定义`

### Page指令
_Page指令为容器提供当前页面的使用说明。一个JSP页面可以包含多个page指令。Page指令的语法格式：_

`<%@ page attribute="value" %>`

#### 属性
_下表列出与Page指令相关的属性：_

_buffer	         指定out对象使用缓冲区的大小_
_autoFlush	      控制out对象的 缓存区_
_contentType	   指定当前JSP页面的MIME类型和字符编码_
_errorPage	指定当JSP页面发生异常时需要转向的错误处理页面_
_isErrorPage	指定当前页面是否可以作为另一个JSP页面的错误处理页面_
_extends	指定servlet从哪一个类继承_
_import	导入要使用的Java类_
_info	定义JSP页面的描述信息_
_isThreadSafe	指定对JSP页面的访问是否为线程安全_
_language	定义JSP页面所用的脚本语言，默认是Java_
_session	指定JSP页面是否使用session_
_isELIgnored	指定是否执行EL表达式_
_isScriptingEnabled	确定脚本元素能否被使用_

