#S pring Exam

For version 5

Sourced from [Core Spring 5.0 Certification Study Guide](https://d1fto35gcfffzn.cloudfront.net/academy/Core-Spring-5.0-Certification-Study-Guide.pdf)

## Container, Dependency, and IOC

- What is dependency injection and what are the advantages?
- What is a pattern? What is an anti-pattern. Is dependency injection a pattern?
- What is an interface and what are the advantages of making use of them in Java?
- Why are they recommended for Spring beans
- What is meant by “application-context?
- What is the concept of a “container” and what is its lifecycle?
- How are you going to create a new instance of an ApplicationContext?
- Can you describe the lifecycle of a Spring Bean in an ApplicationContext?
- How are you going to create an ApplicationContext in an integration test test?
- What is the preferred way to close an application context? Does Spring Boot do this for
- you?
- Can you describe:
	- Dependency injection using Java configuration?
	- Dependency injection using annotations (@Component, @Autowired)?
	- Component scanning, Stereotypes and Meta-Annotations?
	- Scopes for Spring beans? What is the default scope?
- Are beans lazily or eagerly instantiated by default? How do you alter this behavior?
- What is a property source? How would you use @PropertySource?
- What is a BeanFactoryPostProcessor and what is it used for? When is it invoked?
	- Why would you define a static @Bean method?
	- What is a ProperySourcesPlaceholderConfigurer used for?
- What is a BeanPostProcessor and how is it different to a BeanFactoryPostProcessor? What do they do? When are they called?
- What is an initialization method and how is it declared on a Spring bean?
- What is a destroy method, how is it declared and when is it called?
	- Consider how you enable JSR-250 annotations like @PostConstruct and @PreDestroy? When/how will they get called?
  	- How else can you define an initialization or destruction method for a Spring bean?
- What does component-scanning do?
- What is the behavior of the annotation @Autowired with regards to field injection,
- constructor injection and method injection?
- What do you have to do, if you would like to inject something into a private field? Ho does
- this impact testing?
- How does the @Qualifier annotation complement the use of @Autowired?
- What is a proxy object and what are the two different types of proxies Spring can create?
- What are the limitations of these proxies (per type)?
- What is the power of a proxy object and where are the disadvantages?
- What are the advantages of Java Config? What are the limitations?
- What does the @Bean annotation do?
- What is the default bean id if you only use @Bean? How can you override this?
- Why are you not allowed to annotate a final class with @Configuration
- How do @Configuration annotated classes support singleton beans?
- Why can’t @Bean methods be final either?
- How do you configure profiles?, What are possible use cases where they might be useful?
- Can you use @Bean together with @Profile?
- Can you use @Component together with @Profile?
- How many profiles can you have?
- How do you inject scalar/literal values into Spring beans?
- What is @Value used for?
- What is Spring Expression Language (SpEL for short)?
- What is the Environment abstraction in Spring?
- Where can properties in the environment come from – there are many sources for properties – check the documentation if not sure. Spring Boot adds even more.
- What can you reference using SpEL?
- What is the difference between $ and # in @Value expressions?

## Aspect oriented programming

- What is the concept of AOP? Which problem does it solve? What is a cross cutting concern?
	- Name three typical cross cutting concerns.
	- What two problems arise if you don't solve a cross cutting concern via AOP?
- What is a pointcut, a join point, an advice, an aspect, weaving?
- How does Spring solve (implement) a cross cutting concern?
- Which are the limitations of the two proxy-types?
	- What visibility must Spring bean methods have to be proxied using Spring AOP? 
- How many advice types does Spring support. Can you name each one?
	- What are they used for?
	- Which two advices can you use if you would like to try and catch exceptions?
- What do you have to do to enable the detection of the @Aspect annotation? 
	- What does @EnableAspectJAutoProxy do?
- If shown pointcut expressions, would you understand them?
	For example, in the course we matched getter methods on Spring Beans, what would be the correct pointcut expression - to match both getter and setter methods?
- What is the JoinPoint argument used for?
- What is a ProceedingJoinPoint? When is it used?

## Data Management: JDBC, Transactions, JPA, Spring Data
- 
- What is the difference between checked and unchecked exceptions?
	- Why does Spring prefer unchecked exceptions?
	- What is the data access exception hierarchy?
- How do you configure a DataSource in Spring? Which bean is very useful for development/test databases?
- What is the Template design pattern and what is the JDBC template?
- What is a callback? What are the three JdbcTemplate callback interfaces that can be used
- with queries? What is each used for? (You would not have to remember the interface
- names in the exam, but you should know what they do if you see them in a code sample).
- Can you execute a plain SQL statement with the JDBC template?
- When does the JDBC template acquire (and release) a connection - for every method
- called or once per template? Why?
- How does the JdbcTemplate support generic queries? How does it return objects and
- lists/maps of objects?
- What is a transaction? What is the difference between a local and a global transaction?
- Is a transaction a cross cutting concern? How is it implemented by Spring?
- How are you going to define a transaction in Spring?
- What does @Transactional do? What is the PlatformTransactionManager?
- Is the JDBC template able to participate in an existing transaction?
- What is a transaction isolation level? How many do we have and how are they ordered?
- What is @EnableTransactionManagement for?
- What does transaction propagation mean?
- What happens if one @Transactional annotated method is calling another
- @Transactional annotated method on the same object instance?
- Where can the @Transactional annotation be used? What is a typical usage if you put it
- at class level?
- What does declarative transaction management mean?
- What is the default rollback policy? How can you override it?
- What is the default rollback policy in a JUnit test, when you use the
- @RunWith(SpringJUnit4ClassRunner.class) in JUnit 4 or @ExtendWith(SpringExtension.class) in JUnit 5, and annotate your @Test annotated method with @Transactional?
- Why is the term "unit of work" so important and why does JDBC AutoCommit violate this pattern?
- What does JPA stand for - what about ORM?
	- What is the idea behind an ORM? What are benefits/disadvantages or ORM?
	- What is a PersistenceContext and what is an EntityManager. What is the relationship between both?
	- Why do you need the @Entity annotation. Where can it be placed?
- What do you need to do in Spring if you would like to work with JPA?
- Are you able to participate in a given transaction in Spring while working with JPA?
- Which PlatformTransactionManager(s) can you use with JPA?
- What does @PersistenceContext do?
- What do you have to configure to use JPA with Spring? How does Spring Boot make this
- easier?
- What is an "instant repository"? (hint: recall Spring Data)
- How do you define an “instant” repository? Why is it an interface not a class?
- What is the naming convention for finder methods?
- How are Spring Data repositories implemented by Spring at runtime?
- What is @Query used for?

## Spring Boot

- What is Spring Boot?
- What are the advantages of using Spring Boot?
- Why is it “opinionated”?
- How does it work? How does it know what to configure?
- What things affect what Spring Boot sets up?
- How are properties defined? Where is Spring Boot’s default property source?
- Would you recognize common Spring Boot annotations and configuration properties if you
- saw them in the exam?
- What is the difference between an embedded container and a WAR?
- What embedded containers does Spring Boot support?
- What does @EnableAutoConfiguration do?
- What about @SpringBootApplication?
- Does Spring Boot do component scanning? Where does it look by default?
- What is a Spring Boot starter POM? Why is it useful?
- Spring Boot supports both Java properties and YML files. Would you recognize and
- understand them if you saw them?
- Can you control logging with Spring Boot? How?

Note that the second Spring Boot section (Going Further) is not required for this exam. Remember: Unless a question explicitly references Spring Boot (like those in this section) you can assume Spring Boot is not involved in any question. 

## Spring MVC and the Web Layer

- MVC is an abbreviation for a design pattern. What does it stand for and what is the idea behind it?
- Do you need spring-mvc.jar in your classpath or is it part of spring-core?
- What is the DispatcherServlet and what is it used for?
- Is the DispatcherServlet instantiated via an application context?
- What is a web application context? What extra scopes does it offer?
- What is the @Controller annotation used for?
- How is an incoming request mapped to a controller and mapped to a method?
- What is the difference between @RequestMapping and @GetMapping?
- What is @RequestParam used for?
- What are the differences between @RequestParam and @PathVariable?
- What are some of the parameter types for a controller method?
	- What other annotations might you use on a controller method parameter? (You can ignore form-handling annotations for this exam)
- What are some of the valid return types of a controller method?
- What is a View and what's the idea behind supporting different types of View?
- How is the right View chosen when it comes to the rendering phase?
- What is the Model?
- Why do you have access to the model in your View? Where does it come from?
- What is the purpose of the session scope?
- What is the default scope in the web context?
- Why are controllers testable artifacts?
- What does a ViewResolver do?

## Security

Please note that @Secured and the Spring Security JSP tag library may be referenced in the exam but are not in the main course notes. @Secured is in the advanced section.

- What are authentication and authorization? Which must come first?
- Is security a cross cutting concern? How is it implemented internally?
- What is the delegating filter proxy?
- What is the security filter chain?
- What is a security context?
- Why do you need the intercept-url?
- In which order do you have to write multiple intercept-url's?
- What does the ** pattern in an antMatcher or mvcMatcher do?
- Why is an mvcMatcher more secure than an antMatcher?
- Does Spring Security support password hashing? What is salting?
- Why do you need method security? What type of object is typically secured at the method level (think of its purpose not its Java type).
- What do @PreAuthorized and @RolesAllowed do? What is the difference between them?
	- What does Spring’s @Secured do?
	- How are these annotations implemented?
	- In which security annotation are you allowed to use SpEL?
- Is it enough to hide sections of my output (e.g. JSP-Page or Mustache template)?
	- Spring security offers a security tag library for JSP, would you recognize it if you saw it in an example?

## REST

- What does REST stand for?
What is a resource?
- What does CRUD mean?
- Is REST secure? What can you do to secure it?
- What are safe REST operations?
- What are idempotent operations? Why is idempotency important?
- Is REST scalable and/or interoperable?
- Which HTTP methods does REST use?
- What is an HttpMessageConverter?
- Is REST normally stateless?
- What does @RequestMapping do?
- Is @Controller a stereotype? Is @RestController a stereotype?
	- What is a stereotype annotation? What does that mean?
- What is the difference between @Controller and @RestController?
- When do you need @ResponseBody?
- What does @PathVariable do?
- What are the HTTP status return codes for a successful GET, POST, PUT or DELETE operation?
- When do you need @ResponseStatus?
- Where do you need @ResponseBody? What about @RequestBody? Try not to get these muddled up!
- If you saw example Controller code, would you understand what it is doing? Could you tell if it was annotated correctly?
- Do you need Spring MVC in your classpath?
- What Spring Boot starter would you use for a Spring REST application?
- What are the advantages of the RestTemplate?
- If you saw an example using RestTemplate would you understand what it is doing?

## Testing

- Do you use Spring in a unit test?
- What type of tests typically use Spring?
- How can you create a shared application context in a JUnit integration test?
- When and where do you use @Transactional in testing?
- How are mock frameworks such as Mockito or EasyMock used?
- How is @ContextConfiguration used?
- How does Spring Boot simplify writing tests?
- What does @SpringBootTest do? How does it interact with @SpringBootApplication and @SpringBootConfiguration?