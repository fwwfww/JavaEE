复习总结：
---
javaWeb:

  1.发出请求
  2.获取回应
  
- 容器：
 
1.管理声明周期

2.管理数据源[DBCP、C3P0、Durid、BoneCP......]
     方便数据库的连接，管理连接池

   为什么使用数据源连接池？
   1.因为web应用程序默认使用数据源
   2.提高资源(web应用程序)的利用率
   
3.容器的类型：Tomcat、Nginx、Jeety

- 写web应用程序为什么要分层？便于扩展和维护
- 如何分层：
  MVC 
 
 M:模型层 主要任务：管理类和类之间的关系
  类和类之间的关系(继承、关联、依赖、聚合)

V:视图(元数据+数据显示方式)

C:控制层  主要任务：接收表单参数；
          处理业务逻辑；
          转向；
          
- JSP+Servlet+JavaBean <br/>
  M:(JavaBean)<br/>
  V:(JSP)<br/>
  C：(Seervlet)
  
-   JSP的内置对象：<br/>
    Request、Response、Session、Application、Exception、Page、PageContext、Out、ServletConfig

jsp页面中：<br/>
Scriptlet:<br/>声明<%! %><br/>
   指令<%@ %><br/>表达式<%= %>
   <br/><%java代码%><br/>
   
在jsp页面如何引用javabean:<br/>
   动作<jsp:XXXX><br/>
   Scriptlet + 动作 == 在jsp页面所有java的代码
   
   JSP页面不应当承担所有的工作，而只是用来承担数据的显示工作其他所有的和业务有关的工作交给servlet
   
-   Servlet
    Servlet的生命周期：<br/>
    Initial()<br/>
    Services()[doGet()/doPost()]<br/>
    destory()
    
 get请求和post请求：
     
重定向和请求转发：<br/>
 重定向是两个request、请求转发是一个request;<br/>
 重定向的url地址发生变化，请求转发的url不发生变化；<br/>
 一个能带值，一个不能带值；

字符编码：GB2312、UTF-8、UTF-16、GBK、Ascii、Unicode

web字符编码（转码）： <br/>1.过滤器：web.xml;<br/>
2.页面：pageEncoding<br/>
3.servlet response.setContextType("html/text;charset=UTF-8")

数据库转码(2种方式)<br/>
 数据库本身的编码<br/> 程序中链接数据库的链接字符串
 
Spring:<br/>
 IOC:依赖注入、控制反转  applicationContext.xml<br/>
 AOP:面向切面编程(8个术语)<br/>
     切面Aspect<br/>
     切点PointCut<br/>
     织入Weave<br/>
     通知Advice<br/>
     目标对象TargetObject<br/>
     连接点JoinPoint<br/>
     代理对象ProxyObject<br/>
     Introduction<br/>
     []横切关注点Accross Cutting Point
     