### Adding custom `PropertySources` to the `Environment`
#### Using `@PropertySources`

```java
@Configuration
@PropertySource("classpath:/com/myco/app.properties")
public class AppConfig {

  @Autowired
  Environment env;

  @Bean
  public TestBean testBean() {
    TestBean testBean = new TestBean();
    testBean.setName(env.getProperty("testbean.name"));
    return testBean;
  }
}
```

Note:
A PropertySource is a simple abstraction over any source of key-value pairs, 
and Spring’s StandardEnvironment is configured with two PropertySource objects — 
one representing the set of JVM system properties (System.getProperties()) and one representing the set of system environment variables (System.getenv()).

While using @PropertySource on your @SpringBootApplication may seem to be a convenient way to load a custom resource in the Environment, 
we do not recommend it. Such property sources are not added to the Environment until the application context is being refreshed. 
This is too late to configure certain properties such as logging.* and spring.main.* which are read before refresh begins.