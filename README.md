# ubuntu2py

These scripts are designed to create a fully functional web2py environment on a Virtualbox VM running Ubuntu 14.04.  Just follow the directions and run everything from the command line.

It also installs:

MySQL  <br />
Jade  <br />
Coffeescript  <br />
Stylus  <br />
-Jeet  <br />
-Rupture  <br />


Here are the commands you'll need to run:

//create virtual box new vm with “bridged” network that “allows all” with ubuntu server.  don’t install aptitude.  <br />
//use testbed:testbed as the username:password (or change the relevant portions of my scripts.  <br />
//install programs on VM:  <br />
wget http://raw.githubusercontent.com/frog42/web2py/master/scripts/setup-web2py-ubuntu.sh  <br />
chmod +x setup-web2py-ubuntu.sh

//there will be a few prompts with the next command.  I use the defaults, but I use the internet + smarthost option.  <br />
sudo ./setup-web2py-ubuntu.sh  <br />
ifconfig

//now you can SSH into your test environment by using the IP address listed when you ran IFCONFIG.  <br />
//this means you can copy/paste instead of typing everything out.  <br />
ssh testbed@X.X.X.X  <br />
curl https://raw.githubusercontent.com/creationix/nvm/v0.24.1/install.sh | bash  <br />
source .bashrc
source .profile
nvm install stable
npm install stylus -g
npm install coffee-script -g
npm install jeet -g
npm install jade -g
npm install rupture -g
npm install axis -g

