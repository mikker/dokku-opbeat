# dokku-opbeat

A plugin for [dokku](https://github.com/progrium/dokku) that notifies [Opbeat](http://opbeat.com) with new releases.

## Setup

dokku-opbeat checks for the presence of three variables in your app's `ENV` and if they are all present it `curl`s Opbeat.

````sh
$ dokku config:set appname \
  OPBEAT_ORGANIZATION_ID=... \
  OPBEAT_APP_ID=... \
  OPBEAT_SECRET_TOKEN=...
````

