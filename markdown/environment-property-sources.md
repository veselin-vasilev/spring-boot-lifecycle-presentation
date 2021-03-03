### Adding custom `PropertySources` to the `Environment`
#### Using `EnvironmentPostProcessor` (Spring Boot specific)

```java
public class EnvironmentPostProcessorExample implements EnvironmentPostProcessor {

  private final YamlPropertySourceLoader loader = new YamlPropertySourceLoader();

  @Override
  public void postProcessEnvironment(ConfigurableEnvironment environment, SpringApplication application) {
    Resource path = new ClassPathResource("com/example/myapp/config.yml");
    PropertySource<?> propertySource = loadYaml(path);
    environment.getPropertySources().addLast(propertySource);
  }

  private PropertySource<?> loadYaml(Resource path) {
    if (!path.exists()) {
        throw new IllegalArgumentException("Resource " + path + " does not exist");
    }
    try {
        return this.loader.load("custom-resource", path).get(0);
    }
    catch (IOException ex) {
        throw new IllegalStateException("Failed to load yaml configuration from " + path, ex);
    }
  }						
}
```