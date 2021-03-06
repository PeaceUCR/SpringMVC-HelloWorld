# SpringMVC-HelloWorld Application


![screenshot1](https://docs.spring.io/spring/docs/3.1.x/spring-framework-reference/html/images/mvc.png)

https://www.udemy.com/javaspring/learn/v4/t/lecture/432830?start=0

http://www.mkyong.com/spring-mvc/spring-mvc-hello-world-example/

http://docs.spring.io/spring/docs/3.1.x/spring-framework-reference/html/mvc.html#mvc-config


# Note
In Spring MVC , the core dispatcher component is the DispatcherServlet, which act as the front-controller (design pattern). Every web request has to go through this DispatcherServlet, and the DispatcherServlet will dispatch the web request to suitable handlers.

1.in the web.xml, you define servlet-name and servlet-class (DispatcherServlet),then the Spring XML Configuration will be in "servlet-name"-servlet.xml file.

2.in "servlet-name"-servlet.xml file,  

https://www.tutorialspoint.com/spring/spring_web_mvc_framework.htm
The web.xml file will be kept in the WebContent/WEB-INF directory of your web application. Upon initialization of HelloWeb DispatcherServlet, the framework will try to load the application context from a file named [servlet-name]-servlet.xml located in the application's WebContent/WEB-INFdirectory. In this case, our file will be HelloWebservlet.xml.

Next, <servlet-mapping> tag indicates what URLs will be handled by which DispatcherServlet. Here all the HTTP requests ending with .jsp will be handled by the HelloWeb DispatcherServlet.

If you do not want to go with default filename as [servlet-name]-servlet.xml and default location as WebContent/WEB-INF, you can customize this file name and location by adding the servlet listener ContextLoaderListener in your web.xml file as follows −

{context:component-scan base-package="" } 
tells Spring to scan those packages for Annotations.


The {mvc:annotationDriven} tag 

{mvc:annotation-driven } declares explicit support for annotation-driven MVC controllers (i.e. @RequestMapping, @Controller, although support for those is the default behaviour), as well as adding support for declarative validation via @Valid and message body marshalling with @RequestBody/ResponseBody.
https://stackoverflow.com/questions/3977973/whats-the-difference-between-mvcannotation-driven-and-contextannotation

{bean}
 InternalResourceViewResolver is used to resolve “internal resource view” (in simple, it’s final output, jsp or htmp page) based on a predefined URL pattern. In additional, it allow you to add some predefined prefix or suffix to the view name (prefix + view name + suffix), and generate the final view page URL. 
https://www.mkyong.com/spring-mvc/spring-mvc-internalresourceviewresolver-example/


3. in the HelloWorldController.java

@Controller(http://docs.spring.io/spring-framework/docs/2.5.6/api/org/springframework/stereotype/Controller.html)
Indicates that an annotated class is a "Controller" (e.g. a web controller).
This annotation serves as a specialization of @Component, allowing for implementation classes to be autodetected through classpath scanning. It is typically used in combination with annotated handler methods based on the RequestMapping annotation.

@RequestMapping(http://docs.spring.io/spring-framework/docs/2.5.6/api/org/springframework/web/bind/annotation/RequestMapping.html)
change the value in RequestMapping,like \hello, then in the browser, you have to type /hello to get the view
return type (https://stackoverflow.com/questions/18607290/which-return-type-use-in-spring-mvc-in-requestmapping-method)

ModelAndView(http://docs.spring.io/spring/docs/current/javadoc-api/org/springframework/web/servlet/ModelAndView.html)

# How to use: open by eclipse,right click the project name, run on server.
