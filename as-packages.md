# As package

`log4d` support can use in your dart code.

## Install

edit your `pubspec.yaml`

```dart
 log4d: $latest_version
```

## Import

```dart
import 'package:log4d/log4d.dart';
```

## Fetch package from pub

use in dart

```bash
pub get
```

Use in flutter:

```dart
flutter packages get
```

## Use

### Server

```dart
var server = Log4dServer(port: 8899,
 outpath: "/tmp/log/dart.log"
);
server.serve();
```

### Client

```dart
var client = Log4dClient(port: 8899);
await client.connect();
```


