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

# Animated Bouncing Draggable DIalog

**Bouncing Draggable Dialog** package lets you add an animated bouncing draggable dialog to your Flutter app.

## Features

The BouncingDraggableDialog widget is built to be `a unique dialog` that can be used in your Flutter app, replacing the `default` Flutter dialog. By using the `content`, `height` and `width`properties, you can provide the content to be displayed as well as the size of the dialog.

The package will handle the animation by itself.

![package_thumb](https://user-images.githubusercontent.com/68671238/184510724-1c908e69-83fa-4485-909f-95fbbb3c63d8.png)

<hr>

## Getting started

1. Add the latest version of package to your `pubspec.yaml` (and run `dart pub get`):

```dart
dependencies:
  bouncing_draggable_dialog: ^1.0.0
```

2. Import the package and use it in your Flutter App.

```dart
import 'package:bouncing_draggable_dialog/bouncing_draggable_dialog.dart';
```

<hr>

## Usage

There are a number of properties that you can modify:

- content (your dialog content)
- height (height of the dialog)
- width (width of the dialog)

**Example Usage ( complete with all params ):**

<table>
 <tr>
 <td>

```dart

class HomePageScreen extends StatefulWidget {
  const HomePageScreen({Key? key}) : super(key: key);

  @override
  State<HomePageScreen> createState() => _HomePageScreenState();
}

class _HomePageScreenState extends State<HomePageScreen> {
  Widget content() {
    return Center(
      child: Column(
        mainAxisAlignment: MainAxisAlignment.center,
        children: [
          Text(
            'Breaking News!',
            style: TextStyle(
              color: Colors.black,
              fontWeight: FontWeight.w700,
              fontSize: 20,
            ),
          ),
          SizedBox(
            height: 8.0,
          ),
          Divider(
            color: Colors.black,
          ),
          Padding(
            padding: const EdgeInsets.all(8.0),
            child: Text(
              'Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.',
              style: TextStyle(
                color: Colors.black,
                fontWeight: FontWeight.normal,
                fontSize: 12,
              ),
              textAlign: TextAlign.center,
            ),
          ),
          Padding(
            padding: const EdgeInsets.only(right: 24.0, top: 8.0, bottom: 8.0),
            child: Container(
              alignment: Alignment.bottomRight,
              child: GestureDetector(
                onTap: () {
                  Navigator.pop(context);
                },
                child: Text(
                  'Close',
                  style: TextStyle(
                    color: Colors.black,
                    fontWeight: FontWeight.bold,
                    fontSize: 14,
                  ),
                ),
              ),
            ),
          ),
        ],
      ),
    );
  }
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      body: Builder(builder: (context) {
        return Center(
            child: GestureDetector(
                onTap: () {
                  showDialog(
                      context: context,
                      builder: (BuildContext context) {
                        return BouncingDraggableDialog(
                          width: 400,
                          height: 200,
                          content: content(),
                        );
                      });
                },
                child: Text('Open dialog')));
      }),
    );
  }
}

```
   </td>
   <td>
     Here's what it looks like:

<hr>



https://user-images.githubusercontent.com/68671238/184511080-e57d0539-05e4-4eb7-bc30-b2ebf6d53966.mp4




   </td>
  </tr>
  </table>
<hr>

## Next Goals
We are working on some improvements including:

- [ ] Make the widget more customizable.

## Issues & Feedback
Please file an [issue!](https://github.com/aliMissaoui/Flutter-Package-Bouncing-Draggable-Dialog/issues) to send feedback or report a bug. Thank you!

```
