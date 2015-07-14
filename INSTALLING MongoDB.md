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

That's all folks!