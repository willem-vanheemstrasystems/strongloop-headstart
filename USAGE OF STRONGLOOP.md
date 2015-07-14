STRONGLOOP

For documentation on Strongloop, see

http://docs.strongloop.com

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










