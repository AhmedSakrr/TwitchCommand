# TwitchCommand [![Open Source Love](https://badges.frapsoft.com/os/v2/open-source.svg?v=103)](https://github.com/ellerbrock/open-source-badges/) [![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](http://makeapullrequest.com) [![GPL Licence](https://badges.frapsoft.com/os/gpl/gpl.svg?v=103)](https://opensource.org/licenses/GPL-3.0/)
A PoC Command and Conquer tool that uses Twitch Chat as a base server. This program connects clients to a designated Twitch Chat and listens for commands.

# Requirements
- Twitch account.
- Python 3.4
- PyInstaller (will be required with the next build.)

# Disclaimer
The usage of this program directly violates the Twitch Developer Agreement. The usage of it will lead to the termination of your account and possible further action based on the severity of its usage.

This program was created as a Proof of Concept and it is not intended to be used in a malicious way. I am not responsible for any damages or criminal charges that come from using it.

# Features
Currently the program only has one main feature which is a cmd command. It will be demo'd below.

# Usage
Navigate to the twitch page of the channel you selected when making the program.

Upon connection to a server, a new client will announce its presence and client name. If you would like to view a list of all connected clients please use the list command. 
```
!list
```
This program also features a cmd command. It can be used on a per-user basis or as a mass command to all connected client.
```
!act client command action true
```
- Act is the keyword to use a command for the client.
- Client specifies a singular user or a group. You can use a specific name (ex: DESKTOP-TEST) or 'all'.
- Command specifies the intended module to use. Currently it only supports cmd.
- Action is what to use with the selected module. For example 'start.' will open the current directory on the clients PC.
- True is just a placeholder value as I was too lazy to scrub \r\n off the final value. You can write anything.

An example command would be as follows:
```
!act all cmd start. true
```
This would open the current directory on every connected clients PC.

# Creating the program.
## Coming soon: a builder.
Making the program is quite simple. 
- Change the NICK value on line 8 to your Twitch username.
- Change the PASS value on line 9 to your OAuth password (acquire it here: https://twitchapps.com/tmi/)
- Change the CHAN value on line 10 to a desired channel to listen in. It's recommended to use your personal twitch chat as a streamer may ban an account they see posting odd messages and commands.

# Upcoming features
- More modules.
- A builder to simplify making the program as well as making it an exe.
- Whatever else I feel like.