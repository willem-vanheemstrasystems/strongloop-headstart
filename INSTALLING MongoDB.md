MongoDB

Installing on Mac OS X
See also: http://www.instructables.com/id/Install-Homebrew-MongoDB-on-a-Mac/

Using Homebrew (see above link for installation):

homebrew install mongodb

To have launchd start mongodb at login:
    ln -sfv /usr/local/opt/mongodb/*.plist ~/Library/LaunchAgents
Then to load mongodb now:
    launchctl load ~/Library/LaunchAgents/homebrew.mxcl.mongodb.plist
Or, if you don't want/need launchctl, you can just run:
    mongod --config /usr/local/etc/mongod.conf

NOTE: Want a GUI for administrating MongoDB, try Robomongo (http://robomongo.org) which is available for Windows, Mac, and Linux.

To learn more about MongoDB, go here

http://www.tutorialspoint.com/mongodb/

Adding a user to a MongoDB database (e.g. myDb):

See also http://www.pello.info/index.php/blog/enabling-basic-authentication-for-mongodb-databases

use myDb
db.createUser(
  {
    user: "admin",
    pwd: "KeepASecret",
    roles: [ "root" ]
    
  }
)
Successfully added user: { "user" : "admin", "roles" : [ "root" ] }

Or

use myDb
db.createUser(
  {
    user: "myotherdbuser",
    pwd: "KeepASecret",
    roles: ["readWrite","dbAdmin"]
  }
)

NOTE: The db.createUser() function is not recognised by RoboMongo (as RoboMongo uses an old version of MongoDb). Instead execute this command from the MongoDb CLI (see http://docs.mongodb.org/v2.2/mongo/), like so on Mac OS X:

cd /usr/local/

To start MongoDb type:

./bin/mongo

Now you will be in the MongoDb Command Line Interface (CLI)

So to add a user like before, type:

use myDb (if that is the name of your database)

db.createUser(
  {
    user: "myotherdbuser",
    pwd: "KeepASecret",
    roles: ["readWrite","dbAdmin"]
  }
)


That's all folks!