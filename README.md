# Week 3 JEE (Hibernate Spring)
### Table of contents
- General info
- Technologies
- Setup
- Things learned
- Commands


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


Dependencies:

##### Lombok
- Copy the next code and insert it into the file in the dependencies part of the code.
-  `<dependency>
            <groupId>org.projectlombok</groupId>
            <artifactId>lombok</artifactId>
            <optional>true</optional>
		</dependency>`


##### Swagger 2
- Copy the next code and insert it into the file in the dependencies part of the code.
-  `<dependency>
    		<groupId>io.springfox</groupId>
    		<artifactId>springfox-swagger2</artifactId>
    		<version>2.9.2</version>
		</dependency>`

    
##### Swagger ui
- Copy the next code and insert it into the file in the dependencies part of the code.
-  `<dependency>
    		<groupId>io.springfox</groupId>
    		<artifactId>springfox-swagger-ui</artifactId>
    		<version>2.9.2</version>
		</dependency>`

##### Spring boot starter security
- Copy the next code and insert it into the file in the dependencies part of the code.
-  `<dependency>
    		<groupId>org.springframework.boot</groupId>
    		<artifactId>spring-boot-starter-security</artifactId>
		</dependency>`
    
##### PostgreSQL
- Copy the next code and insert it into the file in the dependencies part of the code.
-  `<dependency>
    		<groupId>org.postgresql</groupId>
    		<artifactId>postgresql</artifactId>
		</dependency>`    
    
##### Spring boot starter test
- Copy the next code and insert it into the file in the dependencies part of the code.
-  `<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-test</artifactId>
			<scope>test</scope>
		</dependency>` 

##### Spring boot starter web
- Copy the next code and insert it into the file in the dependencies part of the code.
-  `<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-web</artifactId>
		</dependency>` 

    
##### Spring boot maven plugin
- Copy the next code and insert it into the file in the plugins part of the code.
-  `  <plugin>
				<groupId>org.springframework.boot</groupId>
				<artifactId>spring-boot-maven-plugin</artifactId>
			</plugin>`    
      
##### Docker maven plugin
- Copy the next code and insert it into the file in the plugins part of the code.
-  `  <plugin>
				<groupId>io.fabric8</groupId>
				<artifactId>docker-maven-plugin</artifactId>
				<version>0.21.0</version>
			</plugin>`     

------------
### Things learned
- What springframework is.
- Spring Tool Suite 4.
- URL components.
- What servlets are.
- MVC pattern design.
- Servlet characteristics.
- Servlet types (hhtp servlet and genericservlet)
- JSP.
- JPQL.
- Spring annotations.
- Transactions.
- Advantages of web apps.
- Web server.
- Graphical documentation using swagger.
- Spring security.
- Make authentication requiered to do certain operations.


------------

### Commands
|  Command | Function  |
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


