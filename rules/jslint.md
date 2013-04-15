## JS Lint规则集 [via](http://www.jslint.com/lint.html)



- Global Variables
	- JSLint expects that all variables and functions are declared before they are used or invoked. This allows it to detect implied global variables. It is also good practice because it makes programs easier to read.
	
- Semicolon
	- JSLint expects that every statement be followed by ; except for for, function, if, switch, try, and while. JSLint does not expect to see unnecessary semicolons or the empty statement.

- Comma
	- JSLint expects to see the comma used as a separator, but not as an operator (except in the initialization and incrementation parts of the for statement). It does not expect to see elided elements in array literals. Extra commas should not be used. A comma should not appear after the last element of an array literal or object literal because it can be misinterpreted by some browsers.

- 	Expression Statements
	- An expression statement is expected to be an assignment or a function/method call or delete. All other expression statements are considered to be errors.	
- for in
	- The body of every for in statement should be wrapped in an if statement that does filtering. It can select for a particular type or range of values, or it can exclude functions, or it can exclude properties from the prototype. For example, ` for (name in object) { if (object.hasOwnProperty(name)) { .... } }`
	
- switch
	- 	A common error in switch statements is to forget to place a break statement after each case, resulting in unintended fall-through. JSLint expects that the statement before the next case or default is one of these: break, return, or throw.
	
- var	
	- JSLint expects that a var will be declared only once, and that it will be declared before it is used.
	- JSLint expects that a function will be declared before it is used.
	- JSLint expects that parameters will not also be declared as vars.
	- JSLint does not expect the arguments array to be declared as a var.
	- JSLint does not expect that a var will be defined in a block. This is because JavaScript blocks do not have block scope. This can have unexpected consequences. Define all variables at the top of the function.
	
- == and !=
	- The == and != operators do type coercion before comparing. This is bad because it causes ' \t\r\n' == 0 to be true. This can mask type errors. JSLint cannot reliably determine if == is being used correctly, so it is best to not use == and != at all and to always use the more reliable === and !== operators instead.
	
- Unreachable Code
	- JSLint expects that a return, break, continue, or throw statement will be followed by a } or case or default.

- void
	- In most C-like languages, void is a type. In JavaScript, void is a prefix operator that always returns undefined. JSLint does not expect to see void because it is confusing and not very useful.
	
- Regular Expressions
	- JavaScript's syntax for regular expression literals overloads the / character. To avoid ambiguity, JSLint expects that the character preceding a regular expression literal is a ( or = or : or , character.
	
- Constructors and new
	- JSLint enforces the convention that constructor functions be given names with initial uppercase. JSLint does not expect to see a function invocation with an initial uppercase name unless it has the new prefix. 	- JSLint does not expect to see the new prefix used with functions whose names do not start with initial uppercase. This can be disabled with the newcap option.
	- JSLint does not expect to see the wrapper forms new Number, new String, new Boolean.
	- JSLint does not expect to see new Object. Use {} instead.
	- JSLint does not expect to see new Array. Use [] instead.		
