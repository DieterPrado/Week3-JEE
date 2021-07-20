# Week 3 JEE (Hibernate Spring)
### Table of contents
- [General info](#general-info)
- [Technologies](#technologies)
- [Setup](#setup)
- [Things learned](#things-learned)
>- What is springboot.
>- SpringToolSuite 4.
>- Servlets.
>- Servlet types.
>- MVC design pattern.
>- What is JSP.
>- What is JPQL.
>- Transactions.
>- Graphic documentation using swagger.
- [Annotations and definitions](#annotations-and-definitions)

------------

### General info

This repository contains files and explanations of things learned in the Platzi's Hibernate and Java Spring Course. This course taught about JSP and how to insert code in html pages. It also taught how to use differente technologies like spring and longbook that allow us to write less code and focus in other parts of the code and other technologies like tomcat and omnidb. In this repository you will find a project with MVC (model, view, controller) structure for reservation hotel rooms in which we create, update and delete users from the DB and can see the check-in date in the hotel and the check-out date. 

------------

### Technologies
- Java development kit 8
- Apache Tomcat 9
- OmniDB
- Spring tools 4
- Docker Desktop
- Eclipse JEE IDE
- Lombok
- Maven 3.8.1

**Dependencies:**
- Swagger2
- Swagger ui
- Spring boot starter security
- Spring boot starter data JPA
- Postgresql
- Spring boot starter test
- Spring boot starter web

------------

### Setup

##### Java development kit 8
- Go to https://www.oracle.com/java/technologies/javase/javase-jdk8-downloads.html and download on your system operative
- execute the file .jar and continue the steps with the installer

##### Maven 3.8.1
- Go to https://maven.apache.org/download.cgi
- click on Binary Zip archive and download
- Extract on your preference folder

#####  Tomcat 9
- Go to https://tomcat.apache.org/download-90.cgi
- pick on the left side tomcat 9
- on core select ZIP and download
- Extract on your preference folder

#####  OmniDB
- Go to https://omnidb.org/ and click download
- follow the steps with the installer

#####  Spring tools 4
- Go to https://spring.io/tools and click download on your operative system
- move it into your preference folder and run the file .jar

#####  Docker Desktop
- Go to https://www.docker.com/products/docker-desktop and click download on windows
- Also download toolbox https://github.com/docker/toolbox/releases from this github
- shut down your pc and initialize BIOS and star the virtualization

##### Eclipse JJE 3
- Go to https://www.eclipse.org/downloads/packages/release/neon/3 and download Eclipse IDE for Java EE developers
- continue the installation with the installer


##### Dependencies: 
- Copy the next code and insert it into the file in the dependencies part of the code.
```java
<dependency>
            <groupId>org.projectlombok</groupId>
            <artifactId>lombok</artifactId>
            <optional>true</optional>
</dependency>

<dependency>
    		<groupId>io.springfox</groupId>
    		<artifactId>springfox-swagger2</artifactId>
    		<version>2.9.2</version>
</dependency>

<dependency>
    		<groupId>io.springfox</groupId>
    		<artifactId>springfox-swagger-ui</artifactId>
    		<version>2.9.2</version>
</dependency>

<dependency>
    		<groupId>org.springframework.boot</groupId>
    		<artifactId>spring-boot-starter-security</artifactId>
</dependency>

<dependency>
    		<groupId>org.postgresql</groupId>
    		<artifactId>postgresql</artifactId>
</dependency>

<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-test</artifactId>
			<scope>test</scope>
</dependency>

<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-web</artifactId>
</dependency>
```
    
##### Plugins: 
- Copy the next code and insert it into the file in the plugins part of the code.
```java
<plugin>
				<groupId>org.springframework.boot</groupId>
				<artifactId>spring-boot-maven-plugin</artifactId>
</plugin>
<plugin>
				<groupId>io.fabric8</groupId>
				<artifactId>docker-maven-plugin</artifactId>
				<version>0.21.0</version>
</plugin>
```

------------
### Things learned
- What spring is. Its an application framework and inversion of control container for the Java platform. The frameworks core features can be used by any Java application, but there are extensions for building web applications on top of the Java EE platform.

- Spring Tool Suite 4. It provides support for developing Spring-based enterprise applications, in the next IDEs: Eclipse, Visual Studio Code, or Theia IDE.

- URL components. Protocol, domain and context.

- What servlets are. They are components on the server side that allow to process client requests and respond through the generation of dynamic content or redirect them to other resources. A servlet is simply a class which responds to a particular type of network request - most commonly an HTTP request. Servlets are usually used to implement web applications.

- MVC design pattern, a way to structure our project. MVC = model, view, controller.
>- Model - It directly manages the data, logic and rules of the application.
>- View - Any representation of information such as a chart, diagram or table.
>- Controller - Accepts input and converts it to commands for the model or view.

- Servlet types (hhtp servlet and genericservlet). 
>- Generic servlets: Are protocol independent. They contain no inherent HTTP support or any other transport protocol.
>- HTTP servlets: Have built-in HTTP protocol support and are more useful in a Sun Java System Web Server environment.
>- All servlets must implement a service() method, which is responsible for handling servlet requests. For generic servlets, simply override the service method to provide routines for handling requests. HTTP servlets provide a service method that automatically routes the request to another method in the servlet based on which HTTP transfer method is used. So, for HTTP servlets, override doPost() to process POST requests, doGet() to process GET requests, and so on.

- JSP (JavaServer Pages). It is collection of technologies that helps software developers create dynamically generated web pages based on HTML, XML, SOAP, or other document types. It allows Java code and certain predefined actions to be interleaved with static web markup content, such as HTML.

- JPQL. JPQL is a powerful query language that allows you to define database queries based on your entity model. Its structure and syntax are very similar to SQL. It doesn´t work with tables but with objects representing those tables. It supports queries and namedqueries. Example:
```java
@Query("Select r from Reserva r where r.fechaIngresoRes =:fechaInicio and r.fechaSalidaReserva =: fechaSalida")
public List<Reserva> find(@Param("fechaInicio")Date fechaInicio, @Param("fechaSalida") Date fechaSalida);

@NamedQuery(name ="Cliente.findByIdentificacion", query="Select c from Cliente c where c.identificacionCli = ?1")
```

- Spring annotations. More details below in the Annotations section.

- Transactions. A series of steps that alter the database (for example, update the values) and must be executed successfully, otherwise none of the steps will be executed. 

- Advantages of web apps.

- Web server.

- Graphical documentation using swagger.

- Spring security.

- Make authentication requiered to do certain operations.


------------

### Commands
|  Annotations and definitions | Function  |
| ------------ | ------------ |
| @Springbootapplication | Tells Spring Boot that a class manages the app.   |
| @Entitiy | Tells a java class that it is representing a table in the database.   |
| @table  | Receives the name of the table to which our class is mapping.   |
| @column  | Used when the name of our column is different from the name of the attribute of our table.   |
| @id  | Represents the primary key of the table inside the class.  |
| @EmbededId  | Represents the primary key of the table inside the class when is a composite one.   |
| @GenerateValue  | Automatically generate values for the primary keys .   |
| @OneToMany @ManyToOne  | Represent existing relationships in tables but in classes.   |
| @Embeaddable   | Classes to embed other classes  |
| @Query    | Used to make native queries   |
| @Repository   | Tells the class that it interacts with the database |
| @Component   | Indicates that a class is a spring component  |
| @Mapper   |  Tells a class it is used to map  |
| @Mappings()   | Indicates how we want to do the mapping .  |
| @Mapping   | Indicates source and target to map if they have different names. It can also used to specify which elements don't need to be mapped.  |
| @InheritInverseConfiguration   | Indicates that the conversion we will perform is the inverse and we no longer have to define mappings.  |
| @Autowired   | Spring manages objects that we haven't initialized creating them by itself.  |
| @Service   | Indicates that a class is a business logic service.  |
| @RestController   | Tells spring that a class will be a controller of a rest API |
| @GetMapping    | To obtain information  |
| @Postmapping  | To create information  |
| @PutMapping   | To update information  |
| @Deletemapping | To delete information |
| CrudRepository methods | save(), delete()|
| @WebServlet | Makes the class be treated as a servlet |
| JSP | <%! for variable declaration. <%--- to make comments. <% to insert code |
| @Transaccional | Tells that a class or method its transactional. Prevents a block of operations from be applied to the database if only a single operation fails  |
| @Configuration | To be recognized by spring as a config class |
| @Restcontroller | Makes the class to be treated as a web service |
| @Api | Allows a web service to support swagger technology for documentation |
| @ApiOperation | Represents the documentation operation |
| @ApiResponses  | Makes the documentation of the response |


