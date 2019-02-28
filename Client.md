# Client-cli

## Install

before install you need see [pub global](https://www.dartlang.org/tools/pub/cmd/pub-global)

```bash
pub global activate log4d
```

## Usage

```bash
$ log4d_client -h
-p, --port         port with server
                   (defaults to "8899")

-h, --[no-]help    show help info
-t, --host         host with server
                   (defaults to "localhost")

-l, --level        level for log

          [d]      debug
          [e]      error
          [i]      info
          [w]      warning
```

```bash
log4d_client abc
```


If your server is serving, the server cli will print "abc"

![img](https://raw.githubusercontent.com/kikt-blog/image/master/img/20190228173512.png)

and your `log1.log` file will write log.


![img](https://raw.githubusercontent.com/kikt-blog/image/master/img/20190228173627.png)

you also use other level

`$ log4d_client -le cf`

![img](https://raw.githubusercontent.com/kikt-blog/image/master/img/20190228173936.png)
