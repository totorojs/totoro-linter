## JS Hint规则集 [via](http://jshint.com/docs/#enforcing_options)

强制规则

- bitwise
	- This option prohibits the use of bitwise operators such as ^ (XOR), | (OR) and others. Bitwise operators are very rare in JavaScript programs and quite often & is simply a mistyped &&.
- latedef
	- This option prohibits the use of a variable before it was defined. JavaScript has function scope only and, in addition to that, all variables are always moved—or hoisted— to the top of the function. This behavior can lead to some very nasty bugs and that's why it is safer to always use variable only after they have been explicitly defined.	
- newcap
	- This option requires you to capitalize names of constructor functions. Capitalizing functions that are intended to be used with new operator is just a convention that helps programmers to visually distinguish constructor functions from other types of functions to help spot mistakes when using this.
- undef
	- This option prohibits the use of explicitly undeclared variables. This option is very useful for spotting leaking and mistyped variables.


推荐规则：

- camelcase
- curly
- eqeqeq
- unused
- strict
	- This option requires all functions to run in ECMAScript 5's strict mode. Strict mode is a way to opt in to a restricted variant of JavaScript. Strict mode eliminates some JavaScript pitfalls that didn't cause errors by changing them to produce errors. It also fixes mistakes that made it difficult for the JavaScript engines to perform certain optimizations.
