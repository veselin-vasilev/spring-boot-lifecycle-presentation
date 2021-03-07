### Adding custom `PropertySources` to the `Environment`
#### Manually registering with the context

```java
ConfigurableApplicationContext ctx = // some way to get the context - could be through an application event, or by implementing ApplicationContextAware, etc.
MutablePropertySources sources = ctx.getEnvironment().getPropertySources();
sources.addFirst(new MyPropertySource());
```