# Spring4MvcValidationUsingJavax
* Spring 4 + MVC + Java Configuration + Maven + Hibernate Validation + Javax, Example

* Template example for Spring 4 MVC + JSP View with pure Java Configuration (no XML), using Maven build tool.
* Spring4 + MVC, Integration without using the web.xml and Spring_Servlet.xml file. 
* By using WebMvcConfigurerAdapter class and WebApplicationInitializer interface to replace above files.
* Validation using javax and Hibernate-Validation(Email, NotEmply, etc..)

> **###1. Technologies**
* Spring 4.0.6.RELEASE
* Maven 3.1
* JSTL 1.2

> **###2. To Run this project locally**
* $ git clone https://github.com/AkashChauhanSoftEngi/Spring4MvcValidationUsingJavax
* $ mvn tomcat7:run

> **###3.  Access** 
* http://localhost:8080/Spring4MvcValidationAnnotation

> **###4. Important points to remember**
* Hibernate validator provide many other validations which not present in javax, like
```java
	@Email @NotEmpty
	private String email;
```
* When using javax or hibernate validations, it is simple to do validate model classes
* using @Valid ModelClass obj
```java
	@RequestMapping(value = "doSuccess", method = RequestMethod.POST)
	public String saveRegistration(@Valid Student student, Model model) {}
```
* To write instant message if code breaks, use like this[example]
```java
	@NotNull(message = "This can not be null")
	@Size(min=3, max=30,message = "THis can not be null")
```


