### `Environment`
	
The `Environment` interface is an abstraction integrated in the container that models two key aspects of the application environment: `profiles` and `properties`.

* The role of the `Environment` object with relation to profiles is in determining which profiles (if any) are currently active, and which profiles (if any) should be active by default.

* The role of the `Environment` object with relation to properties is to provide the user with a convenient service interface for configuring property sources 
and resolving properties from them.