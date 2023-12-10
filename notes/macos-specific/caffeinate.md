# `caffeinate`

Alters system's sleep behavior, typically to prevent system from sleeping.

Running with no flags or args prevents system going to sleep (*idle sleep*) as long as command's running.

## Awake for Duration

`caffeinate -t <seconds>` prevents sleep for specified number of seconds.

### Example

```sh
caffeinate -t 3600 &
```

`&` at end to run in background. Can still sleep manually even if running.

## Awake for Command

`caffeinate <command>` starts command in new process and prevents sleep until that process exits.

Use `-w <pid>` to prevent sleep until specified existing process exits.

### Example

```sh
$ caffeinate -i long_running_script.sh
```

## Other Options

* `-i` prevents system from idle sleeping.
* `-d` prevents display from sleeping.
* `-m` prevents disk from sleeping.
* `-s` keeps whole system awake. Only when on AC power.
* `-u` declares user active. If display off, this turns it on and prevents it going into idle sleep. If timeout not specified, defaults to 5 seconds.
