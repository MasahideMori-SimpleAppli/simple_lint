# simple_lint

## Overview

**simple_lint** provides a lightweight lint rule set based on **flutter_lints**,  
with two additional rules focused on enforcing consistent import styles:

- `always_use_package_imports: true`
- `prefer_relative_imports: false`

Together, these prevent subtle instance-duplication bugs that can occur when  
the same file is imported using a mix of package imports and relative paths —  
a common cause of unexpected “singleton breakage” in Dart/Flutter projects.

## Usage

1. Add `simple_lint` to your project:

```yaml
dev_dependencies:
  simple_lint: ^1.0.0
```

2. In your project's analysis_options.yaml, include the lint rules:

```yaml
include: package:simple_lint/simple_lint.yaml
```

That's all — the lint rules will be applied automatically.


## Lint Rules Included

```yaml
include: package:flutter_lints/flutter.yaml

linter:
  rules:
    always_use_package_imports: true
    prefer_relative_imports: false

analyzer:
  exclude:
    - build/**
    - test/**
```

These rules ensure consistent package-level imports and help avoid
accidental duplication of objects across different import paths.

## Support

No official support is provided at the moment.

## Versioning Policy

Versioning follows this pattern:

- C.X.X — Breaking changes (e.g., modifications that prevent compatibility with previous versions)
- X.C.X — Additive, non-breaking updates (e.g., new rules or features)
- X.X.C — Minor adjustments, documentation changes, and bug fixes

## License

This software is released under the BSD 3-Clause License.
See the LICENSE file for details.

## Trademarks

- “Dart” and “Flutter” are trademarks of Google LLC.  
  *This package is not developed or endorsed by Google LLC.*
