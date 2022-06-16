##### usage
~~~ts
resolveSnowflake(strToSolve: string): string | boolean;
~~~
##### example
~~~js
msg.guild.cache.get(resolveSnowflake('<@681919237706612743>'));
// this example isn't good and less practical, but I think it can be understood.
~~~

## Code
~~~js
function resolveSnowflake(strToSolve) {
	const _0 = strToSolve.replace(/[<!@#:&a-z>]/gim, '');
	return isNaN(Number(_0)) && _0;
};
~~~
