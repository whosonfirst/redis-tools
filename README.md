# redis-tools

Tools. For doing stuff with Redis.

## bin

### info

Print information about Redis's current state to STDOUT. If no keys are specificed then all keys(and their values) are displayed.

For example:

```
$> info <key1> <key2> ...
```

### publish

Publish one or more messages to a PubSub channel.

```
$> publish -h
Usage: publish [options]

Options:
  -h, --help   show this help message and exit
  --host=HOST  The host of the Redis server to connect to
  --port=PORT  The port of the Redis server to connect to
  --json       Serialize all input as JSON before publishing (default is
               False)
```

For example:

```
$> publish <channel> <msg1> <msg2> ...
```

_This should be taught to read from STDIN._

### subscribe

Subscribe to a PubSub channel and print each message received to STDOUT.

```
$> subscribe -h
Usage: subscribe [options]

Options:
  -h, --help   show this help message and exit
  --host=HOST  The host of the Redis server to connect to
  --port=PORT  The port of the Redis server to connect to
```

For example

```
$> subscribe <channel>
```

## See also

* http://redis.io/
* https://pypi.python.org/pypi/redis
