##### usage
~~~ts
isSnowflake(snowflakeToSolve: string | number): boolean;
~~~
##### example
~~~js
console.log(isSnowflake('681919237706612743')); // true
console.log(isSnowflake('uwaaaaaaa!!')); // false
console.log(isSnowflake('1234')); // false
~~~

## Code
~~~js
function isSnowflake(snowflakeToSolve) {
	const typeof_0 = typeof snowflakeToSolve;
	if (!['number', 'string'].includes(typeof_0) || isNaN(snowflakeToSolve))
		return false;
	typeof_0 === 'number' && (snowflakeToSolve = snowflakeToSolve.toString());
	return /\d{17,19}/.test(snowflakeToSolve);
};
~~~
