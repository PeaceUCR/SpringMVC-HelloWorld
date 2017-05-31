# SpringMVC-HelloWorld Application

https://www.udemy.com/javaspring/learn/v4/t/lecture/432830?start=0

http://www.mkyong.com/spring-mvc/spring-mvc-hello-world-example/

http://docs.spring.io/spring/docs/3.1.x/spring-framework-reference/html/mvc.html#mvc-config

![springMVC](http://docs.spring.io/spring/docs/3.1.x/spring-framework-reference/html/images/mvc.png)

# Note for the project,how to understand the code in this project
In Spring MVC , the core dispatcher component is the DispatcherServlet, which act as the front-controller (design pattern). Every web request has to go through this DispatcherServlet, and the DispatcherServlet will dispatch the web request to suitable handlers.

1.in the web.xml, you define servlet-name and servlet-class (DispatcherServlet),then the Spring XML Configuration will be in "servlet-name"-servlet.xml file.

2.in "servlet-name"-servlet.xml file,  

context:component-scan base-package=""
tells Spring to scan those packages for Annotations.


The "mvc:annotationDriven" tag essentially sets you your Spring context to allow for dispatching requests to Controllers.
The tag will configure two beans DefaultAnnotationHandlerMapping and AnnotationMethodHandlerAdapter.

"bean"

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
