##### usage
```ts
findMember(guild: discord.Guild, memberToSolve: string, tags?: string): discord.GuildMember | undefined;
```

##### requires 
> [isSnowflake](https://github.com/Pavez7274/Pavez7274/blob/main/codes/util/discord_is_snowflake.md) <br>
> [resolveSnowflake](https://github.com/Pavez7274/Pavez7274/blob/main/codes/util/discord_resolve_snowflake.md)

##### example
```js
findMember(msg.guild, 'yaku').then((member) => console.log(member));
/* some like
User {
  id: '681919237706612743',
  bot: false,
  system: false,
  flags: [UserFlags],
  username: 'Yaku',
  discriminator: '4245',
  avatar: '2aa71c432ee693c5246406918f4ba968',
  banner: undefined,
  accentColor: undefined
}
*/
```

## Code
```js
async function findMember(guild, mts, tags) {
	await guild.members.fetch();
	let reg = new RegExp(mts, tags ?? 'gi');
	mts = mts.toLowerCase();
	if (isSnowflake(mts)) {
		return guild.members.cache.get(mts);
	};
	return guild.members.cache.find((member) => {
		let displayTag = member.displayName + member.user.discriminator;
		return mts === member.user.username.toLowerCase() ||
		mts === member.displayName ||
		mts === member.user.tag ||
		mts === displayTag ||
		reg.test(member.displayName) ||
		reg.test(displayTag) ||
		reg.test(member.user.tag) ||
		mts === member.toString() ||
		resolveSnowflake(mts) === member.user.id;
	});
};
```
