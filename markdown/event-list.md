
1. An `ApplicationStartingEvent` is sent at the start of a run but before any processing, 
except for the registration of <span class="fragment highlight-red" data-fragment-index="1">listeners</span> and <span class="fragment highlight-red" data-fragment-index="1">initializers</span>.

2. An `ApplicationEnvironmentPreparedEvent` is sent when the <span class="fragment highlight-red" data-fragment-index="1">Environment</span> to be used
  in the <span class="fragment highlight-red" data-fragment-index="1">context</span> is known but before
  the <span class="fragment highlight-red" data-fragment-index="1">context</span> is created.

3. An `ApplicationContextInitializedEvent` is sent when the <span class="fragment highlight-red" data-fragment-index="1">ApplicationContext</span> is prepared 
and <span class="fragment highlight-red" data-fragment-index="1">ApplicationContextInitializers</span> have been called but before
any <class class="fragment highlight-red" data-fragment-index="1">bean definitions</class> are loaded.

4. An `ApplicationPreparedEvent` is sent just before the <span class="fragment highlight-red" data-fragment-index="1">refresh</span> is started but 
after <span class="fragment highlight-red" data-fragment-index="1">bean definitions</span> have been loaded.

5. An `ApplicationStartedEvent` is sent after the <span class="fragment highlight-red" data-fragment-index="1">context</span> has been refreshed but before 
any <span class="fragment highlight-red" data-fragment-index="1">application and command-line runners</span> have been called.

6. An `AvailabilityChangeEvent` is sent right after with <span class="fragment highlight-red" data-fragment-index="1">LivenessState.CORRECT</span> to indicate that the application is considered as live.

7. An `ApplicationReadyEvent` is sent after any <span class="fragment highlight-red" data-fragment-index="1">application and command-line runners</span> have been called.

8. An `AvailabilityChangeEvent` is sent right after with <span class="fragment highlight-red" data-fragment-index="1">ReadinessState.ACCEPTING_TRAFFIC</span>
to indicate that the application is ready to service requests.

9. An `ApplicationFailedEvent` is sent if there is an exception on startup.