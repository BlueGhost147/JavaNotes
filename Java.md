# Java

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


## Sets
`mySet.add --> Returns a boolean (added successfully)`


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
