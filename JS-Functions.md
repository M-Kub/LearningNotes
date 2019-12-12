# Different JavaScript Function notations.

## Declaration Notation

	function square(x) {
		return x * x;
	}

This is a function declaration. The statement defines the binding *square* and points it at the given function.

One subtlety with this function definition is that code that uses the function can also be written before the function is declared. Just like in thefollowing example.

	console.log("The future says:", futur());

	function future() {
		return "No flying cars in the future.";
	}

Function declarations are not part of the regular top-to-bottom controlflow. They are conceptually moved to the top of their scope, and can be used by all the code in that scope.

## Arrow Functions

The *ArrowFunction* instead of the *function* keyword, it uses an arrow(=>) thats made up of an equal sign and an greater than sign.

	const power = (base, exponent) => {
		let result = 1;
		for (let count = 0; count < exponent; count++) {
			result *= base;
		}
		return result;
	};

The arrow after the list of parameters is meant to mean something like "This input (the parameters) produces this result (the body)."
When ther is only one parameter name, the paranthese around the parameter list can be omitted. If the body of the function is only a single expression, rather than a block in braces, that expression will be returned from the function. So, these two definitions of square do the same thing:

	const square1 = (x) => { return x * x; };
	const sqaure2 = x => x * x;

When an arrow function has no parameters at all, its parameter list is just an empty set of parantheses.

	const horn = () => {
		console.log("Toot");
	}

