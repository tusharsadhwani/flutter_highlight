# flutter_highlight

Syntax highlighter for Flutter. https://git-touch.github.io/highlight/

> NOTE: this is a fork of https://github.com/git-touch/highlight, with only the
> flutter_highlight package. This was created to add editable highlight views.

## Web demo [here](https://tusharsadhwani.github.io/flutter_highlight)

## Usage

```dart
import 'package:flutter/material.dart';
import 'package:flutter_highlight/flutter_highlight.dart';
import 'package:flutter_highlight/themes/github.dart';

class MyWidget extends StatelessWidget {
  @override
  Widget build(BuildContext context) {
    var code = '''main() {
  print("Hello, World!");
}
''';

    return HighlightView(
      // The original code to be highlighted
      code,

      // Specify language
      // It is recommended to give it a value for performance
      language: 'dart',

      // Specify highlight theme
      // All available themes are listed in `themes` folder
      theme: githubTheme,

      // Specify padding
      padding: EdgeInsets.all(12),

      // Specify text style
      textStyle: TextStyle(
        fontFamily: 'My awesome monospace font',
        fontSize: 16,
      ),
    );
  }
}
```

## References

- [All available languages](https://github.com/pd4d10/highlight/tree/master/highlight/lib/languages)
- [All available themes](https://github.com/pd4d10/highlight/blob/master/flutter_highlight/lib/themes)

## License

MIT
