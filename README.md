# SWENG

## Eclipse

### Setup
Windows>Preferences>Java>Editor>Content Assist>"Insert best guessed arguments" on

### Format
[Strg] + [Shift] + [F]

### Important Notes

* Only send forms with POST
* Always use the name to identify a button (because of translations)
* use the teamname as root package name

## Iterator
Handles collection in an optional way
Provides a remove methode -> no ConcModExc
`
Iterator<int> it = myList.iterator();

while(it.hasNext())
{
	int = myNum = it.next();
	(...)
}
`

## HTTP

### Cookies 
immer Secure / HTTPonly attribut setzten -> benötigt HTTPS

## Servlet 

### CodeSnippets

`processRequest(request, response);
RequestDispatcher rd = request.getRequestDispatcher("departmentView.jsp");
rd.forward(request, response);`

`HttpSession session = request.getSession();`

`response.addCookie(null);`
	
`Integer.parseInt((String) request.getParameter("num1"));`

`request.setAttribute("result", result);`

## JSP
`<%@include file="./index.jsp" %>`

`${param.num1} + ${param.num2} = ${result}`


### ErrorPages
#### JSP
`<%@ page isErrorPage="true" %>`

#### web.xml
`
<error-page>
	<exception-type>java.lang.Exception</exception-type>
	<location>/showError.jsp</location>
</error-page>
`

## Thymeleaf
Never use unescaped Text -> utext !


## Sets
`mySet.add --> Returns a boolean (added successfully)`





