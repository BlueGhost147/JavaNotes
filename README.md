# SWENG

## Eclipse

### Setup
Windows > Preferences > Java > Editor > Content Assist > "Insert best guessed arguments" on

### Format
[Strg] + [Shift] + [F]

### Optimize Inports
[Strg] + [Shift] + [O]

### Important Notes
* Only send forms with POST
* Always use the name to identify a button (because of translations)
* use the teamname as root package name


## Iterator
Handles collection in an optional way
Provides a remove methode -> no ConcModExc

```java
Iterator<int> it = myList.iterator();

while(it.hasNext())
{
	int = myNum = it.next();
	(...)
}
```

## Utility Class
Collections Class

## HTTP
### Cookies
always set Secure / HTTPonly attribute -> requires HTTPS

## Servlet
### CodeSnippets

```java
processRequest(request, response);
RequestDispatcher rd = request.getRequestDispatcher("departmentView.jsp");
rd.forward(request, response);
return;
```

```java
HttpSession session = request.getSession();
```

```java
response.addCookie(null);
```

```java
Integer.parseInt((String) request.getParameter("num1"));
```

```java
request.setAttribute("result", result);
```

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
Never use unescaped Text -> utext !

## Sets
`mySet.add --> Returns a boolean (added successfully)`

# Other
## Hibernate - hbm2ddl.auto
#### create-drop
delete DB and recreate it on startup, perfect for testing
#### update
try' to apply changes to the db, may not work
#### validate
Application won´t start if the DB changed, won´t apply changes to the db on startup

# Important Anotations
## Spring
### @Controller
### @RequestMapping("\index")
## Spring - Hibernate
### @Transactional
Changes will start a transaction, the transaction is DB sided


