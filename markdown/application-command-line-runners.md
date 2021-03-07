### Application and Command-line runners
An application is considered ready as soon as application and command-line runners have been called.

Tasks expected to run during startup should be executed by <span class="fragment highlight-red" data-fragment-index="0">`CommandLineRunner`</span> and 
<span class="fragment highlight-red" data-fragment-index="0">`ApplicationRunner`</span> components instead of using Spring component lifecycle callbacks 
such as `@PostConstruct`.

Note:
We will see example implementations of both of these components in the demo after.