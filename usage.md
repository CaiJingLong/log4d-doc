# Usage

Usually, when developing locally, start the server ahead of time.

## 1. Start server

`$ log4d -o build/dart.log`

## 2. use code in your flutter

create a `LogHelper` instance

```dart
import 'dart:async';

import 'package:log4d/log4d.dart';

class LogHelper {
  Log4dClient _client;

  bool isLog = true;

  bool isRemote = true;

  LogHelper._() {
    _client = Log4dClient();
  }

  Future connectRemote() async {
    await _client.connect();
  }

  static LogHelper _instance;

  factory LogHelper() {
    _instance ??= LogHelper._();
    return _instance;
  }

  void info(String msg) {
    if (isLog) print(msg);
    
    if (isLog && isRemote) {
      _client.sendEntity(
        LogEntity()
          ..level = Level.info
          ..msg = msg,
      );
    }
  }
}

```

`main.dart`

```dart

void main() async {
  var log = LogHelper();
  await log.connectRemote();

  log.info("你好");
}
```

## Stop use

```dart
LogHelper().isLog = false;
LogHelper().isRemote = false;
```

## Other

Only suitable for local debugging.  
With a WebSocket connection, it will not automatically reconnect when it is disconnected abnormally.