# Template engines

## JSP
```java
<%@include file="./index.jsp" %>
```

```java
${param.num1} + ${param.num2} = ${result}
```

### ErrorPages
#### JSP
```java
<%@ page isErrorPage="true" %>
```

#### web.xml
```xml
<error-page>
	<exception-type>java.lang.Exception</exception-type>
	<location>/showError.jsp</location>
</error-page>
```


## Thymeleaf
