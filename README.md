# SWENG

This repository is a collection of important notes, code snippets, configuration, best practises and quirks for Java projects created in Eclipse.

[Eclipse documentation](Eclipse.md)

[Java documentation](Java.md)

[Template engines documentation](TemplateEngines.md)


## Important Notes
* Only send forms with POST
* Always use the name to identify a button (because of translations)
* use the teamname as root package name
* Try to avoid the use of unescaped Text whenever possible -> utext !


## Utility Class
Collections Class


## HTTP
### Cookies
always set Secure / HTTPonly attribute -> requires HTTPS


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
CascadeType.PERSIST --> Save the object if it doesn´t exist
### @ManyToMany
### Other
#### @Transactional
Changes will start a transaction, the transaction is DB sided
