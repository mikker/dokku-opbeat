# dokku-opbeat

**NB: At the moment the plugin only includes commits up to and _not including_ the most recent one. That's not right but I haven't found the time to fix it yet. Would love a PR ❤️**

A plugin for [dokku](https://github.com/progrium/dokku) that notifies [Opbeat](http://opbeat.com) with new releases.

## Setup

dokku-opbeat checks for the presence of three variables in your app's `ENV` and if they are all present it `curl`s Opbeat.

````sh
$ dokku config:set appname \
  OPBEAT_ORGANIZATION_ID=... \
  OPBEAT_APP_ID=... \
  OPBEAT_SECRET_TOKEN=...
````

