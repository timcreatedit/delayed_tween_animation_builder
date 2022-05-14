<!-- 
This README describes the package. If you publish this package to pub.dev,
this README's contents appear on the landing page for your package.

For information about how to write a good package README, see the guide for
[writing package pages](https://dart.dev/guides/libraries/writing-package-pages). 

For general information about developing packages, see the Dart guide for
[creating packages](https://dart.dev/guides/libraries/create-library-packages)
and the Flutter guide for
[developing packages and plugins](https://flutter.dev/developing-packages). 
-->

``DelayedTweenAnimationBuilder`` behaves like Flutter's ``TweenAnimationBuilder``but adds 
the option to delay the animation by a given duration.

## Features

- Delays are one of the most useful features of ``simple_animations``'s ``PlayAnimation`` Widget - use them without depending on the entire package! 
- Delay the initial animation of a ``TweenAnimationBuilder``
- Optionally delay every subsequent animation of a change

## Usage

```dart
// This is how you would have a widget appear after 1 second
Widget build(BuildContext context) {
  return DelayedTweenAnimationBuilder<double>(
    delayOnlyOnce: true,
    duration: const Duration(seconds: 1),
    tween: Tween(begin: 0, end: 1),
    builder: (context, value, child) => Opacity(
      opacity: value,
      child: child,
    ),
    child: const FlutterLogo(),
  );
}
```

## Additional information

This package is very simple and will therefore most probably not receive many updates. We will do our best to always maintain compatibility with the most current Flutter version however!
New features will only be added if they fit the scope of this widget so it won't get bloated.

If you find a bug or want to add things like tests, feel free to open a pull request!