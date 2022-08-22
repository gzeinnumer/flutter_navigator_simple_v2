# flutter_navigator_simple_v2

```dart
Navigator.push(context, MaterialPageRoute(builder: (context)=> const SecondRouteView()));
```

- main.dart
```dart
import 'package:flutter/material.dart';

void main() {
  runApp(const FirstRouteView());
}

class FirstRouteView extends StatelessWidget {
  const FirstRouteView({Key? key}) : super(key: key);

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: const Text('First Route'),
      ),
      body: Center(
        child: ElevatedButton(
            child: const Text("To Second Route"),
            onPressed: (){
              Navigator.push(context, MaterialPageRoute(builder: (context)=> const SecondRouteView()));
            },
        ),
      ),
    );
  }
}

class SecondRouteView extends StatelessWidget {
  const SecondRouteView({Key? key}) : super(key: key);

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: const Text(''),
      ),
      body: Center(
        child: ElevatedButton(
            child: const Text("Go Back To First Route"),
            onPressed: () {
              Navigator.pop(context);
            },
        ),
      ),
    );
  }

  void _showSnackbar(BuildContext context, String message) {
    final snackBar = SnackBar(content: Text(message));
    ScaffoldMessenger.of(context).showSnackBar(snackBar);
  }
}
```


---

```
Copyright 2022 M. Fadli Zein
```