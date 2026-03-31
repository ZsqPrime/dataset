# README

#### 처리 흐름
1. 클라이언트의 요청이 DispatcherServlet에 전달된다.
2. DispatcherServlet은 HandlerMapping을 사용하여 클라이언트의 요청을 처리할 컨트롤러 객체를 구한다. 
3. DispatcherServlet은 컨트롤러 객체를 이용해서 클라이언트의 요청을 처리한다. 
4. 컨트롤러는 클라이언트의 요청 처리 결과 정보를 담은 ModelAndView 객체를 리턴한다. 
5. DispatcherServlet은 ViewResolver로부터 응답 결과를 생성할 뷰 객체를 구한다. 
6. 뷰는 클라이언트에 전송할 응답을 생성한다. 



#### 단계1: DispatcherServlet 설정 및 컨텍스트 설정

**web.xml에 다음 2가지 설정을 추가한다.**

1. 클라이언트의 요청을 전달받을 DispatcherServlet 설정
2. 공통으로 사용할 어플리케이션 컨텍스트 설정


web.xml

	<?xml version="1.0" encoding="UTF-8">
	<web-app>
		<servlet>
			<servlet-name>dispatcher</servlet-name>
			<servlet-class>org.springframework.web.servlet.DispatcherServlet</servlet-class>
			<init-param>
				<param-name>contextConfigLocation</param-name>
				<param-value>classpath:servlet-context.xml</param-value>
			</init-param>
			<load-on-startup>1</load-on-startup>
		</servlet>
		
		<servlet-mapping>
			<servlet-name>dispatcher</servlet-name>
			<url-pattern>*.do</url-pattern>
		</servlet-mapping>
	
	</web-app>

* DispatcherServlet 설정은 기본적으로 /WEB-INF/[서블릿명]-servlet.xml을 참조. (dispatcher-servlet.xml)
* 별도로 파일을 설정하려면 contextConfigLocation을 설정하면 됨