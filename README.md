# **js-sandbox**


**Built-in modules**

* [Simple-statistics](https://github.com/simple-statistics/simple-statistics)

**Commands**

`!gc` - delete last 100 bot messages in current channel

`!mem` - current memory usage

`!say [channelId] [msg]`

`!react [channelId] [messageId] [reaction]`

`!rstr [channelId] [messageId] [text]`

`!servers` - list of servers where bot installed

`!mycolor [hexcolor|colorName] --purge`

`!cmdlist` - output all custom commands
`!cmdlist --my` - output own created custom commands

`!rmcmd [NAMECMD]` - remove your custom command

___

`channelId` is optional (default - current channel)

`reaction` is global or custom emoji. (Examples: :regional_indicator_a: )

`text` should consists only english letters


# Custom commands

You can add custom commands from chat in discord. Example

```javascript
'custom command'
'cmd=nameCmd'
'desc=this command output 42'
console.log(42);
```

Now you can write `!nameCmd` to chat discord. Bot answer will be `42`.

First line must be `'custom command'`. It indicate for bot.

Second line for naming of command `'cmd=COMMAND_NAME'`. Max length name - 16 chars. Only letters.

Third line not required. Use it for description of your command.

Rewrite custom command unavailable. Use `!rmcmd nameCmd` for remove custom command.

## Http

In your code available function `request`. Example:

```js
request('http://api.ipify.org/?format=json', function (error, response, body) {
    if (!error && response.statusCode == 200) {
        console.log(body);
    }
})
```
Http available for custom commands too.



