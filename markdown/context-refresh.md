### Context Refresh

An application is considered live as soon as the context has been refreshed. Refreshing the context means that all beans will be loaded, post-processor beans will be detected 
and activated, singletons are pre-instantiated, and the ApplicationContext object is ready for use.

Note: 
As long as the context has not been closed, a refresh can be triggered multiple times, provided that the chosen ApplicationContext actually supports such “hot” refreshes. 
It is worth mentioning that we will not cover all spring context/container states and the various events associated to them. We're mostly interested in those which 
will help us understand the Spring Boot lifecyle, not the underlying container lifecycle. The other events such as the ContextStartedEvent or the ContextStoppedEvent will 
likely be covered in a future Bean Lifecyle-focused session we will run. 