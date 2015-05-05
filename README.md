# Graphite Notify

Send deployment events to graphite
[![Build Status](https://travis-ci.org/hellvinz/graphite-notify.png)](https://travis-ci.org/hellvinz/graphite-notify)

More information about events https://code.launchpad.net/~lucio.torre/graphite/add-events/+merge/69142

## Installation

Add this to your deploy.rb file:

```
set :graphite_url, "your/graphite/event/url"
require "graphite-notify/capistrano"
```

It is possible to set ssl verify modes with `graphite_ssl_verify` variable:

```
set :graphite_ssl_verify, OpenSSL::SSL::VERIFY_PEER
```

## Requirements

graphite: http://readthedocs.org/docs/graphite

## Tricks

As it is a capistrano task you can call it directly:

```
cap graphite:notify_deploy
```
 
## License

graphite-notify is released under the [MIT License](http://www.opensource.org/licenses/MIT).
