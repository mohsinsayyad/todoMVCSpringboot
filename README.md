Prequisites:
1. Maven
2. JDK11

Run `mvn clean install` in the Maven project directory and wait for the compilation and packaging to finish. Then, run `java -jar target/tasks-0.0.1-SNAPSHOT.jar`. You should see something like:

```bash  .   ____          _            __ _ _
 /\\ / ___'_ __ _ _(_)_ __  __ _ \ \ \ \
( ( )\___ | '_ | '_| | '_ \/ _` | \ \ \ \
 \\/  ___)| |_)| | | | | || (_| |  ) ) ) )
  '  |____| .__|_| |_|_| |_\__, | / / / /
 =========|_|==============|___/=/_/_/_/
 :: Spring Boot ::               (v2.7.11)

2024-02-09 18:29:05.150  INFO 14432 --- [           main] com.todo.mvc.tasks.TasksApplication      : Starting TasksApplication v0.0.1-SNAPSHOT using Java 11.0.0.1 on DESKTOP-O8PMP6O with PID 14432 (C:\tasks\target\tasks-0.0.1-SNAPSHOT.jar started in C:\Users\tasks)
2024-02-09 18:29:05.166  INFO 14432 --- [           main] com.todo.mvc.tasks.TasksApplication      : No active profile set, falling back to 1 default profile: "default"
2024-02-09 18:29:07.446  INFO 14432 --- [           main] .s.d.r.c.RepositoryConfigurationDelegate : Bootstrapping Spring Data JPA repositories in DEFAULT mode.
2024-02-09 18:29:07.572  INFO 14432 --- [           main] .s.d.r.c.RepositoryConfigurationDelegate : Finished Spring Data repository scanning in 93 ms. Found 1 JPA repository interfaces.
2024-02-09 18:29:10.011  INFO 14432 --- [           main] o.s.b.w.embedded.tomcat.TomcatWebServer  : Tomcat initialized with port(s): 8081 (http)
2024-02-09 18:29:10.045  INFO 14432 --- [           main] o.apache.catalina.core.StandardService   : Starting service [Tomcat]
2024-02-09 18:29:10.046  INFO 14432 --- [           main] org.apache.catalina.core.StandardEngine  : Starting Servlet engine: [Apache Tomcat/9.0.74]
2024-02-09 18:29:10.238  INFO 14432 --- [           main] o.a.c.c.C.[Tomcat].[localhost].[/]       : Initializing Spring embedded WebApplicationContext
2024-02-09 18:29:10.244  INFO 14432 --- [           main] w.s.c.ServletWebServerApplicationContext : Root WebApplicationContext: initialization completed in 4899 ms
2024-02-09 18:29:10.379  INFO 14432 --- [           main] com.zaxxer.hikari.HikariDataSource       : HikariPool-1 - Starting...
2024-02-09 18:29:11.096  INFO 14432 --- [           main] com.zaxxer.hikari.HikariDataSource       : HikariPool-1 - Start completed.
2024-02-09 18:29:11.132  INFO 14432 --- [           main] o.s.b.a.h2.H2ConsoleAutoConfiguration    : H2 console available at '/h2'. Database available at 'jdbc:h2:mem:todo_tasks'
2024-02-09 18:29:11.597  INFO 14432 --- [           main] o.hibernate.jpa.internal.util.LogHelper  : HHH000204: Processing PersistenceUnitInfo [name: default]
2024-02-09 18:29:11.733  INFO 14432 --- [           main] org.hibernate.Version                    : HHH000412: Hibernate ORM core version 5.6.15.Final
2024-02-09 18:29:12.168  INFO 14432 --- [           main] o.hibernate.annotations.common.Version   : HCANN000001: Hibernate Commons Annotations {5.1.2.Final}
2024-02-09 18:29:12.503  INFO 14432 --- [           main] org.hibernate.dialect.Dialect            : HHH000400: Using dialect: org.hibernate.dialect.H2Dialect
2024-02-09 18:29:14.254  INFO 14432 --- [           main] o.h.e.t.j.p.i.JtaPlatformInitiator       : HHH000490: Using JtaPlatform implementation: [org.hibernate.engine.transaction.jta.platform.internal.NoJtaPlatform]
2024-02-09 18:29:14.278  INFO 14432 --- [           main] j.LocalContainerEntityManagerFactoryBean : Initialized JPA EntityManagerFactory for persistence unit 'default'
2024-02-09 18:29:16.179  WARN 14432 --- [           main] JpaBaseConfiguration$JpaWebConfiguration : spring.jpa.open-in-view is enabled by default. Therefore, database queries may be performed during view rendering. Explicitly configure spring.jpa.open-in-view to disable this warning
2024-02-09 18:29:17.767  INFO 14432 --- [           main] o.s.b.w.embedded.tomcat.TomcatWebServer  : Tomcat started on port(s): 8081 (http) with context path ''
2024-02-09 18:29:18.258  INFO 14432 --- [           main] com.todo.mvc.tasks.TasksApplication      : Started TasksApplication in 14.308 seconds (JVM running for 15.561)
```
Swagger API is enabled in application. Please use below URL to access Swagger UI to test REST API's

```Swagger URL - http://localhost:8081/swagger-ui/#/```
```
1. Add Tasks -
 [POST] - http://localhost:8081/api/tasks
 [Request Payload] - {  "completed": true,  "title": "Task 1"}

2. Update Tasks -
 [PUT] - http://localhost:8081/api/tasks/{id}
 [Request Payload] - {  "completed": true,  "title": "Task 1"}

3. Delete Tasks -
 [DELETE] - http://localhost:8081/api/tasks/{id}

4. Get Task for given Id -
 [GET] - http://localhost:8081/api/tasks/{id}

5. Get all tasks -
 [GET] - http://localhost:8081/api/tasks
```

Run `mvn test` to execute below mentioned test cases.
1. TasksApplicationTests.java
2. TaskControllerTests.java
3. TaskDAOImplTests.java
4. TaskExceptionHandlerTests.java
5. TaskRepositoryTests.java

```
[INFO] Results:
[INFO] 
[INFO] Tests run: 20, Failures: 0, Errors: 0, Skipped: 0
[INFO] 
[INFO] ------------------------------------------------------------------------
[INFO] BUILD SUCCESS
[INFO] ------------------------------------------------------------------------	
```

Spring Boot features used in application:
1. Spring Boot Web.
2. Spring Boot JPA.
3. Spring Boot Tests.
4. Swagger2
5. Lombok
6. H2 inmemory database.
7. Spring AOP for logging.


Flow Diagram

![image](https://github.com/mohsinsayyad/todoMVCSpringboot/assets/117346117/10d017c1-14ea-49d4-946e-7fec06bb0e05)

