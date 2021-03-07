### Liveness state and Readiness State

The `Livenes` state of an application tells whether its internal state allows it to work correctly, or recover by itself if it’s currently failing.
A broken `Liveness` state means that the application is in a state that it cannot recover from, and the infrastructure should restart the application.

The `Readiness` state of an application tells whether the application is ready to handle traffic. 
A failing `Readiness` state tells the platform that it should not route traffic to the application for now. 

Note:
For liveness:
The internal state of Spring Boot applications is mostly represented by the Spring ApplicationContext. 
If the application context has started successfully, Spring Boot assumes that the application is in a valid state.
An application is considered live as soon as the context has been refreshed.

For readiness:
This typically happens during startup, while `CommandLineRunner` and `ApplicationRunner` components are being processed, 
or at any time if the application decides that it’s too busy for additional traffic.