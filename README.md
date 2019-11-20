# springmvc-xml
xml SpringwebMVC


基于xml的方式配置的 springmvc 说明

1. 首先在web.xml 文件中配置 tomcat 容器。
2. 需要一个全局配置参数 contextConfigLocation 用于寻找 根配置文件。
3. 需要配置一个过滤器 ， org.springframework.web.context.ContextLoaderListener 该过滤器回自动加载根配置，并将根配置后面的配置加载，并置入
   父容器中。
4. 配置DispathcerServlet 值是 org.springframework.web.servlet.DispatcherServlet
5. 为 DispathcerServlet 配置上下文。方式和 全局方式类似，但是 设置为 <init-parame> 的方式。
6. 在 mvc 的配置的上下文中，需要开启<context:component-scan base-package="controller"/> <mvc:annotation-driven/> 元素配置了 包扫面功能和 
   开启mvc的功能 如果需要配置 视图解析器，需要加载 bean 
