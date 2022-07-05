### `ApplicationContext` + `BeanFactory`
`BeanFactory` - provides the configuration framework and basic functionality.

`ApplicationContext` - adds more enterprise-specific functionality. A complete superset of the `BeanFactory`. The internal state of Spring Boot applications is mostly represented by the Spring `ApplicationContext`.

If the application context has started successfully, Spring Boot assumes that the application is in a valid state.

Note: 
You should use an `ApplicationContext` unless you have a good reason for not doing so, 
with `GenericApplicationContext` and its subclass `AnnotationConfigApplicationContext` as the common implementations for custom bootstrapping.

In SpringBoot's case, we don't really care about which one is used, since it is configured for us.

The internal state of Spring Boot applications is mostly represented by the Spring `ApplicationContext`.

If the application context has started successfully, Spring Boot assumes that the application is in a valid state.

Typically, an application developer does not need to subclass `ApplicationContext` implementation classes. 
Instead, the Spring IoC container can be extended by plugging in implementations of special integration interfaces.

Since we're talking about Spring Boot, the choice is made for us and most of the time we'll have no reason to think about extending the `ApplicationContext`.