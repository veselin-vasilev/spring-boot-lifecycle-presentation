### `Environment`
	
The `Environment` interface is an abstraction integrated in the container that models two key aspects of the application environment: `profiles` and `properties`.

* The role of the `Environment` object with relation to profiles is in determining which profiles (if any) are currently active, and which profiles (if any) should be active by default.

* The role of the `Environment` object with relation to properties is to provide the user with a convenient service interface for configuring property sources 
and resolving properties from them.

Note:
Spring Profiles provide a way to segregate parts of your application configuration and make it only available in certain environments.

Spring properties are a unified abstraction over externalized application configuration. Properties could come from many places - YAML files, environment variables, command-line arguments, etc. 