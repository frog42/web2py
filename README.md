# ubuntu2py

**These scripts are designed to create a fully functional web2py environment on a Virtualbox VM running Ubuntu 14.04.  Just follow the directions and run everything from the command line.**

It also installs:

Jade
Coffeescript
Stylus
-Jeet
-Rupture


Here are the commands you'll need to run:

# create virtual box new vm with “bridged” network that “allows all” with ubuntu server.  don’t install aptitude.
# use testbed:testbed as the username:password (or change the relevant portions of my scripts.
# install programs on VM:
wget http://raw.githubusercontent.com/frog42/web2py/master/scripts/setup-web2py-ubuntu.sh
chmod +x setup-web2py-ubuntu.sh

# there will be a few prompts with the next command.  I use the defaults, but I use the internet + smarthost option.
sudo ./setup-web2py-ubuntu.sh
ifconfig

# now you can SSH into your test environment by using the IP address listed when you ran IFCONFIG.
# this means you can copy/paste instead of typing everything out.
ssh testbed@X.X.X.X
curl https://raw.githubusercontent.com/creationix/nvm/v0.24.1/install.sh | bash
source .bashrc
source .profile
nvm install stable
npm install stylus -g
npm install coffee-script -g
npm install jeet -g
npm install jade -g
npm install rupture -g
npm install axis -g
