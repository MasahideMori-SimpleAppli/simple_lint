# simple_lint

## Overview
This package provides a lightweight lint rule set based on **flutter_lints**,
with an additional rule that enforces **package-level imports**.  
This helps prevent accidental instance duplication that can occur when files
are imported using inconsistent relative paths, ensuring that shared objects
behave as intended.

## Usage

1. Add `simple_lint` to your project:

```yaml
dev_dependencies:
  simple_lint: ^0.0.1
```

2. In your project's **analysis_options.yaml**, include the lint rules provided by this package:

```yaml
include: package:simple_lint/simple_lint.yaml
```

That's all — the lint rules will be applied automatically.

## Support
There is currently no support.

## About version control
The C part will be changed at the time of version upgrade.
- Changes such as adding variables, structure change that cause problems when reading previous files.
    - C.X.X
- Adding methods, etc.
    - X.C.X
- Minor changes and bug fixes.
    - X.X.C

## License
This software is released under the BSD 3-Clause License, see LICENSE file.

## Copyright notice
The “Dart” name and “Flutter” name are trademarks of Google LLC.  
*The developer of this package is not Google LLC.