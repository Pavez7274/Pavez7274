##### usage
~~~ts
String.toCodeBlock(lang?: String): String;
~~~
##### example
~~~js
const _0 = 'println("uwu");';
DiscordChannel.send(_0.toCodeBlock('rs');
// send this
// ```rs
// println("uwu");
// ```
~~~

## Code
~~~js
const { escapeCodeBlock } = require('discord.js').Util;
String.prototype.toCodeBlock = function(lang = ''){
	return `\`\`\`${lang}
${escapeCodeBlock(this)}
\`\`\``
};
~~~
