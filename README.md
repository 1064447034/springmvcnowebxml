# springmvcnowebxml
springmvc无web.xml

代码调试过程中，发现没有调用ContextLoaderListener（创建spring容器），是因为没有web.xml，没有配置
<listener>
	<listener-class>org.springframework.web.context.ContextLoaderListener</listener-class>
</listener>
而在MyWebApplicationInitializer中，手动创建了spring容器；
