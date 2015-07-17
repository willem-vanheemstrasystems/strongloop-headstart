STRONGLOOP

For documentation on Strongloop, see

http://docs.strongloop.com

IMPORTANT: Make sure you have rights and ownership to the following folder:

/usr/local/lib/node_modules/strongloop

Check by typing:

cd /usr/local/lib/node_modules
ls -l

You could set the ownership as follows (where wvanheemstra is your username):

sudo chown -Rv wvanheemstra:staff strongloop

IMPORTANT: Are you on the latest version of LoopBack? Run slc update and try the lb-ng command again.

IMPORTANT: After you have installed StrongLoop (i.e. BackLoop), make sure that the Angular SDK is installed as well, by running from within the application folder (e.g. loopback-getting-started) the following command:

npm install -g loopback-sdk-angular-cli

Example App
See http://docs.strongloop.com/display/public/LB/Create+a+simple+API

To create an example app with loopback, from the repository root folder type:

slc --help

This should show you the manual of strongloop, if not you need to install strongloop like so:

npm install -g strongloop

Once loopback is installed type the following:

slc loopback

You will be prompted with questions to create the example app (e.g. loopback-getting-started).

After having answered all questions, change to the directory of the example app, e.g.:

cd/loopback-getting-started

Create a model in your app (e.g. CoffeeShop), by typing:

slc loopback:model

Compose your API, run, deploy, profile, and monitor it with Arc:

slc arc

Run the app (use 'node .' for development mode, use 'slc start' when ready for deployment):

node .

API Explorer:

Open a web browser at http://0.0.0.0:3000/explorer to see the API Explorer

It will list all REST points for all models (e.g. CoffeeShops)

More info here, http://docs.strongloop.com/display/public/LB/Use+API+Explorer
___

StrongLoop Studio

StrongLoop Studio is used to 
- API Composer: visually create datasources and models.
- Profiler: Profile applications'CPU and memory consumption.

Install StrongLoop Studio by typing at the root of the application folder (e.g. loopback-getting-started):

npm install -g http://get-studio.strongloop.com/strong-studio.tgz

NOTE: If you install the above globally (-g), it doesn't really matter where in the document tree you type the command.

Run StrongLoop Studio as follows:

strong-studio

It will open the browser and show the web page that is the StrongLoop Studio.

Your studio is running here: http://localhost:52565/#studio   (the portnumber is different per session)










