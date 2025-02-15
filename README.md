## Description

This mod adds per user IP based authorization.

This mod is very useful for offline mode Minecraft servers because it ensures that a user with a username can only join from a specified IP. This avoids impersonating other users and stealing their dear resources.


## Commands

Register a player without an IP and auto assign it on user first join.
```
/ipauth add player
```
Register a player with specify IP addresses the player can join with.
```
/ipauth add player ip1 ip2 ip3 ...
```
Remove a player completely.
```
/ipauth remove player
```
Remove IP addresses the player can join with.
```
/ipauth remove player ip1 ip2 ip3
```
Set auto_auth property from the game.
```
/ipauth setautoauth true|false
```
Set use_uuid property from the game.
```
/ipauth setuseuuid true|false
```
Get general information.
```
/ipauth info
```
Get info on a IP or a user.
```
/ipauth info IP|user
```
## Config

The config is in JSON format.

```jsonc
{
 authorized: {
  "USERNAME": ["IP 1", "IP 2"]
 },
 auto_authorize: true, // on first join, automatically register the user to authorized list with the joining IP. (will be auto_auth on next release)
 use_uuid: true // use the uuid instead of using the username to identify the users in the authorized list.
}
```
