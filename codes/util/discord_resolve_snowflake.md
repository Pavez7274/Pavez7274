## usage
~~~ts
resolveSnowflake(resolvable: string): string | boolean;
~~~
## example
~~~js
msg.guild.cache.get(resolveSnowflake('<@681919237706612743>'));
// this example isn't good and less practical, but I think it can be understood.
~~~

## code
~~~js
function resolveSnowflake(resolvable) {
	resolvable = resolvable?.replace(/[<!@#:&a-z>]/gim, "");
	return isNaN(Number(resolvable)) && resolvable;
};
~~~
