The above list only includes `SpringApplicationEvents` that are tied to a `SpringApplication`.
In addition to these, the following events are also published after `ApplicationPreparedEvent` and before `ApplicationStartedEvent`:

* A `WebServerInitializedEvent` is sent after the `WebServer` is ready. `ServletWebServerInitializedEvent` and `ReactiveWebServerInitializedEvent` are the servlet and reactive variants respectively.
* A `ContextRefreshedEvent` is sent when an `ApplicationContext` is refreshed.