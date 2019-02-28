# Server

## Install

before install you need see [pub global](https://www.dartlang.org/tools/pub/cmd/pub-global)

```bash
pub global activate log4d
```

## Usage

### Help

```bash
$ log4d -h
-o, --output          output path
-p, --port            server port
                      (defaults to "8899")

-h, --[no-]help       usage
-c, --[no-]console    show log in console
                      (defaults to on)
```

### Use

1. use

```bash
log4d
```

2. simple use 

```bash
mkdir -p /tmp/logs
cd /tmp/logs
log4d -o log1.log
```

