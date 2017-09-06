# Steam Hour Boost

To add new users to the `database.json` run `coffee user.coffee` and follow the instructions.

By default it will boost the games CS 1.6, CS:S and CS:GO. If you want to change the games that are being boosted, edit the `database.json` directly!

## How to install
First you need to install a recent version of `node.js`, `coffee-script` and `pm2`:

```bash
sudo apt-get install curl
curl -sL https://deb.nodesource.com/setup_8.x | sudo -E bash -
sudo apt-get install -y nodejs
sudo apt-get install -y build-essential
sudo npm -g install npm@latest
sudo npm -g install coffee-script pm2
sudo pm2 install coffeescript
```

Afterwards upload this script to your server, or clone it using `git`:

```bash
# If git is missing on your server google on how to install it.
# On Debian/Ubuntu the command is 'sudo apt-get install git'
git clone https://github.com/rpgeS/Steam-Hour-Boost.git
```

`cd` into the folder and install the dependencies

```bash
cd Steam-Hour-Boost
npm install .
```

## How to use

After that you can add accounts using `coffee user.coffee`. When you are ready, start the script using `pm2`:

```bash
pm2 start boost.coffee
```

That's it!

## How do I restart the script?

That's easy. Just tell `pm2` to do so:

```bash
pm2 restart all
```

If you have multiple processes running you may want to specificy the id of the process to restart, you can find it using

```bash
pm2 ls
```
