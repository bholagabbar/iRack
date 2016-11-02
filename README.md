# irackbot
A bot for built for Efficient and Manageable Cross-Platform Open Source Communication by relaying messages across Slack and IRC channels differently

##Another IRC-Slack bot?

A lot of Open Source communities rely on [IRC ](https://en.wikipedia.org/wiki/Internet_Relay_Chat) for their communication. IRC's great
but let's face it, it doesn't really compare that well to modern team messaging clients like [Slack](https://slack.com/).

* A lot of your conversations are drowned and lost inbetween messages from other users discussing other issues
* It's hard to keep track of what you've discussed and keep a log of messages received.
* Proxy issues with IRC resulting in instant ban from IRC servers when you haven't done s**t (pretty common)

You could be working on a project / involved with this
community and you end up facing all these problems. So being the wannabe developer that you are, you end up building
something that solves all of these problems.

##Uhh, so what's different?

* This bot relays messages from Slack to IRC and vice-versa.<br>
*Well, that's not new.*

* You can mention users on the other platform (from Slack to IRC and vice versa) by just pinging them with their original username.<br>
*Ehh nothing new*

* You can get a list of all the users on the other platform with just a single command.<br>
*Ok not bad..*<br>

* You can configure your bot, with a single ping command, to **filter all incoming IRC communication and include only those messages
where any one of your members on the Slack channel have been mentioned**. Meanwhile, all your communication from Slack is still
relayed to IRC and everyone can see what you're discussing and reach out to you anytime.
<br>
*That's just what I need!*<br>


####Some regular chat

![Some regular chat](http://i.imgur.com/o5e9xXC.png)


####A few features

![image](http://i.imgur.com/4J3T3Fl.png)

##Setup

####Requirements: You need to have [Java](https://java.com/en/download/) and [Maven](https://maven.apache.org/install.html) installed and configured.

1. Setup a Slack Bot for your team channel through the official slack website [by going here](https://www.google.co.in/webhp?sourceid=chrome-instant&ion=1&espv=2&ie=UTF-8#q=slack%20bot%20for%20my%20team) and clicking on *creating a new bot user*.
2. Generate and copy the Authentication Token you get. Keep it safely.
3. Once you create the bot it should be visible on your Slack Team. Invite it to the channel you are going to use it on.
4. Clone this repository, go to `/src/main/resources` and open the `config.properties` file. Enter all the configuration details following the template given. Make sure all your details are correct, especially your *Team Name* as this currently cannot be verified programmatically. On entering any other incorrect details, you will have an exception thrown.
5. Go back to the project root directory and open up your terminal pointing to that directory
6. Run `mvn clean install`.
7. After a successful build, `cd` to `/target` and run `java -jar irackbot-1.0.jar` to get your bot started.

##Usage

### Modes: What makes this bot different is you can tell it to receive either all messages from IRC *(Mode 1)* or only those where your channel members are mentioned *(Mode 2)*

##### For the examples, I'm assuming my bot is named *irack-bot* on both channels. Needless to say, you have the choice to keep whatever name suits you through the config file.

* *Get users on Slack From IRC*: `@irack-bot slack_users`
* *Get users on IRC From Slack*: `@irack-bot irc_users`
* *Change mode on Slack*: `@irack-bot change_mode`
* *Ping users from IRC to Slack or vice versa*: `@slack/ircusername[Space *important*], message`

##Credits

This bot was built using the [pircbot](http://www.jibble.org/pircbot.php) library by [Jibble](http://www.jibble.org/) and the [simple-slack-api](https://github.com/Ullink/simple-slack-api) by [Ullink](https://github.com/Ullink). Kudos to them for building these useful tools so effectively with an easy to use API.


##Contributions

Pull requests and Issues are welcome. Please do supplement them with enough information so as to get a clear idea about the same. Also, please do Star this repository if you liked irackbot !

##License

This tool is licensed under the [Creative Commons CC0 1.0 Universal](http://creativecommons.org/publicdomain/zero/1.0/) license.