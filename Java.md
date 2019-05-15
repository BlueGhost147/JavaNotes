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

# Other
## Hibernate - hbm2ddl.auto
#### create-drop
delete DB and recreate it on startup, perfect for testing
#### update
try' to apply changes to the db, may not work
#### validate
Application won't start if the DB changed, won't apply changes to the db on startup

# Important Anotations
## Spring
### @Controller
### @RequestMapping("\index")
## Spring - Hibernate
### Class
#### @Entity
```java
@Entity
class MyClass {...}
```

#### @Table(name="TableName")
```java
@Entity
@Table(name="TableName")
class MyClass {...}
```

### Attribute
#### @Id
```java
@Id
@Column(name="empId")
private int id;
```

#### @Column(name="name", nullable=true, lenght=100)
```java
@Column(name="empName",nullable=false,lenght=100)
private String name;
```

#### @Temporal(TemporalType.DATE)
```java
@Temporal(TemporalType.DATE)
private Date dayOfBirth
```

#### @Version
Prevents datalose if data is overriden
```java
@Version
private long version;
```

### @Embedded
performance??

### @AttributeOverrides
```java
@Embedded
	@AttributeOverrides({
		@AttributeOverride(name = "street", column = @Column(name = "delivery_street")),
		@AttributeOverride(name = "city", column = @Column(name = "delivery_city")),
		@AttributeOverride(name = "country", column = @Column(name = "delivery_country")),
		@AttributeOverride(name = "zip", column = @Column(name = "delivery_zip"))
	})
Address deliveryAddress;
```

### @ManyToOne
```java
@ManyToOne(cascade = CascadeType.PERSIST)
private MyClass myobj;
```
CascadeType.PERSIST --> Save the object if it doesnÂ´t exist
### @ManyToMany
### Other
#### @Transactional
Changes will start a transaction, the transaction is DB sided
