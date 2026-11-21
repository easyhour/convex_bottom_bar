# convex_navigation_bar

Customizable convex bottom navigation bars with animated tabs, badges, multiple styles and Material and Cupertino support.

An independently maintained, public fork of `convex_bottom_bar`. It is a general-purpose Flutter library and does not depend on EasyHour services or a private account.

## Requirements

- Flutter 3.50 or later and Dart 3.14 or later.
- Standalone `material_ui` and `cupertino_ui` libraries. This release is incompatible with the legacy in-SDK design-system types.

## Installation

```yaml
dependencies:
  convex_navigation_bar: ^4.0.0
```

```dart
import 'package:convex_navigation_bar/convex_navigation_bar.dart';
import 'package:material_ui/material_ui.dart';
```

See [the example](example/lib/main.dart), [migration guide](MIGRATION.md) and [release checklist](RELEASING.md). The previous `convex_bottom_bar.dart` barrel remains available inside the new package as a compatibility export; the old package name is not an alias.

## Usage

```dart
Scaffold(
  body: const Center(child: Text('Home')),
  bottomNavigationBar: ConvexAppBar(
    items: const [
      TabItem(icon: Icons.home, title: 'Home'),
      TabItem(icon: Icons.map, title: 'Explore'),
      TabItem(icon: Icons.person, title: 'Profile'),
    ],
    onTap: (index) {
      // Update the selected page in your application state.
    },
  ),
);
```

Supports fixed, fixedCircle, react, reactCircle, textIn, titled and flip styles, custom builders, badges and TabController integration. Pure Flutter widgets can be used across Flutter platforms; validate platform builds in your application.

## Origin and license

Derived from [convex_bottom_bar](https://github.com/easyhour/convex_bottom_bar) at `f1cc10494ce8b116e00d03bdfaf7ac969e411512`. Original authors, copyright notices and licenses are preserved in [LICENSE](LICENSE). Historical API documentation is archived in [UPSTREAM_README.md](UPSTREAM_README.md); its version and support claims do not apply to this fork.

This fork updates dependencies, design-system imports, examples and development tooling. See [CHANGELOG.md](CHANGELOG.md) for changes.
