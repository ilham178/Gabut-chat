# Ilham Mansiezz
A modular telegram Python bot running on python3 with an sqlalchemy database.

Based on [marie bot](https://github.com/PaulSonOfLars/tgbot)

### [Read indonesia README](https://github.com/ilham178/bott/edit/master/README.md)

**If you want to translate this bot**, [please go here](https://github.com/ilham178/bott/edit/master/README.md)

Can be found as [ILHAM MANSIEZZ](https://t.me/bismillahselaluadaa).


For questions regarding creating your own bot, please head to [support group](https://t.me/EmiliaOfficial) where you'll find a
group of volunteers to help. We'll also help when a database schema changes, and some table column needs to be
modified/added (this info can also be found in the commit messages)

Join the [news channel](https://t.me/gabutttttttttttttttttttttttttt) if you just want to stay in the loop about new features or
announcements.

Or [ask me in telegram](https://t.me/bismillahselaluadaa)! (Save all support questions in the support chat, where more people can help you.)

Note to maintainers that all schema changes will be found in the commit messages, and its their responsibility to read any new commits.


## Starting the bot.

Once you've setup your database and your configuration (see below) is complete, simply run:

`python3 -m tg_bot`


## Setting up the bot (Read this before trying to use!):
Please make sure to use python3.6, as I cannot guarantee everything will work as expected on older python versions!
This is because markdown parsing is done by iterating through a dict, which are ordered by default in 3.6.

### Configuration

There are two possible ways of configuring your bot: a config.py file, or ENV variables.

The prefered version is to use a `config.py` file, as it makes it easier to see all your settings grouped together.
This file should be placed in your `tg_bot` folder, alongside the `__main__.py` file . 
This is where your bot token will be loaded from, as well as your database URI (if you're using a database), and most of 
your other settings.

It is recommended to import sample_config and extend the Config class, as this will ensure your config contains all 
defaults set in the sample_config, hence making it easier to upgrade.

An example `config.py` file could be:
```
from tg_bot.sample_config import Config


class Development(Config):
    OWNER_ID = 254318997  # my telegram ID
    OWNER_USERNAME = "SonOfLars"  # my telegram username
    API_KEY = "your bot api key"  # my api key, as provided by the botfather
    SQLALCHEMY_DATABASE_URI = 'postgresql://username:password@localhost:5432/database'  # sample db credentials
    MESSAGE_DUMP = '-1234567890' # some group chat that your bot is a member of
    USE_MESSAGE_DUMP = True
    SUDO_USERS = [18673980, 83489514]  # List of id's for users which have sudo access to the bot.
    LOAD = []
    NO_LOAD = ['translation']
```

If you can't have a config.py file (EG on heroku), it is also possible to use environment variables.
The following env variables are supported:
 - `ENV`: Setting this to ANYTHING will enable env variables

 - `TOKEN`: Your bot token, as a string.
 - `OWNER_ID`: An integer of consisting of your owner ID
 - `OWNER_USERNAME`: Your username

 - `DATABASE_URL`: Your database URL
 - `MESSAGE_DUMP`: optional: a chat where your replied saved messages are stored, to stop people deleting their old 
 - `LOAD`: Space separated list of modules you would like to load
 - `NO_LOAD`: Space separated list of modules you would like NOT to load
 - `WEBHOOK`: Setting this to ANYTHING will enable webhooks when in env mode
 messages
 - `URL`: The URL your webhook should connect to (only needed for webhook mode)

 - `SUDO_USERS`: A space separated list of user_ids which should be considered sudo users
 - `SUPPORT_USERS`: A space separated list of user_ids which should be considered support users (can gban/ungban,
 nothing else)
 - `WHITELIST_USERS`: A space separated list of user_ids which should be considered whitelisted - they can't be banned.
 - `DONATION_LINK`: Optional: link where you would like to receive donations.
 - `CERT_PATH`: Path to your webhook certificate
 - `PORT`: Port to use for your webhooks
 - `DEL_CMDS`: Whether to delete commands from users which don't have rights to use that command
 - `STRICT_GBAN`: Enforce gbans across new groups as well as old groups. When a gbanned user talks, he will be banned.
 - `WORKERS`: Number of threads to use. 8 is the recommended (and default) amount, but your experience may vary.
 __Note__ that going crazy with more threads wont necessarily speed up your bot, given the large amount of sql data 
 accesses, and the way python asynchronous calls work.
 - `BAN_STICKER`: Which sticker to use when banning people.
 - `ALLOW_EXCL`: Whether to allow using exclamation marks ! for commands as well as /.

#DEPLOY DISINI
<p align="center"><a href="https://heroku.com/deploy?template=https://github.com/ilham77mansiz/Petercord-Userbotilham/tree/Petercord-Userbotilham"> <img src="https://img.shields.io/badge/Deploy%20Ke%20Heroku-magenta?style=flat&logo=heroku" width="210" height="34.45" /></a></p>

<br>
</p>
