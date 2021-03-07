### Container Extension

The Spring IoC container can be extended by plugging in implementations of special integration interfaces.

#### `BeanPostProcessor`
The `BeanPostProcessor` interface defines callback methods that you can implement to provide your own (or override the container’s default) instantiation logic, dependency resolution logic, and so forth. If you want to implement some custom logic after the Spring container finishes instantiating, configuring, and initializing a bean, you can plug in one or more custom `BeanPostProcessor` implementations.

#### `BeanFactoryPostProcessor`
`BeanFactoryPostProcessor` operates on the bean configuration metadata. That is, the Spring IoC container lets a `BeanFactoryPostProcessor` read the configuration metadata and potentially change it before the container instantiates any beans other than `BeanFactoryPostProcessor` instances.

Note:
Spring provides some container extension points, which, if implemented, allow us to muck about with the beans that come out of the ApplicationContext. 

BeanPostProcessor - operates on already instantiated beans. That is, the Spring IoC container instantiates a bean instance and then BeanPostProcessor instances do their work.
You can configure multiple BeanPostProcessor instances, and you can control the order in which these BeanPostProcessor instances run by setting the order property. You can set this property only if the BeanPostProcessor implements the Ordered interface.

BeanFactoryPostProcessor - allows you to operate on the bean configuration metadata - the bean definitions 
You can configure multiple BeanFactoryPostProcessor instances, and you can control the order in which these BeanFactoryPostProcessor instances run by setting the order property. However, you can only set this property if the BeanFactoryPostProcessor implements the Ordered interface.
A bean factory post-processor is automatically run when it is declared inside an ApplicationContext, in order to apply changes to the configuration metadata that define the container.