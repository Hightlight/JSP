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


## JSP注释
_JSP注释主要有两个作用：为代码作注释以及将某段代码注释掉。JSP注释的语法格式：_

`
<body>
<%-- 该部分注释在网页中不会被显示--%> 
<p>
   今天的日期是: <%= (new java.util.Date()).toLocaleString()%>
</p>
</body> 
</html> 
`


