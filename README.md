# Flare-Flutter
Flutter runtime written in Dart with SKIA based rendering.

## Installation
Download the repository and add `flare` as a local [dependency in your pubspec.yaml file](https://flutter.io/platform-plugins/).
## Exporting for Flutter
Export from Flare with the *"Export to Engine"* menu. In the Engine dropdown, choose *Generic*, and in the Format dropdown your favorite form of compression, Binary for efficiency or JSON for readability.

## Adding Assets
Once you've exported your file, add the **.flr** file to your project's [Flutter assets](https://flutter.io/assets-and-images/). 

## Example
Take a look at the provided [example application](https://github.com/2d-inc/Flare-Flutter/tree/master/example) for how to use the FlareActor Widget with the exported Flare file.

## Usage
The easiest way to get started is by using the provided **FlareActor** widget. This is a stateless Flutter widget that allows for one Flare file with one active animation playing to be embedded in your Flutter App. 


You can change the currently playing animation by changing the animation property's name. 


You can also specify the mixSeconds to determine how long it takes for the animation to interpolate from the previous one. A value of 0 means that it will just pop to the new animation. A value of 0.5 will mean it takes half of a second to fully mix the new animation on top of the old one.

```
import 'package:flare/flare_actor.dart';
class MyHomePage extends StatefulWidget {
  @override
  _MyHomePageState createState() => new _MyHomePageState();
}

class _MyHomePageState extends State<MyHomePage> {
  @override
  Widget build(BuildContext context) {
    return new FlareActor("assets/ball.flr", alignment:Alignment.center, fit:BoxFit.contain, animation:"Triangling");
  }
}
```

## Contributing
1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request.

## License
See the [LICENSE](LICENSE) file for license rights and limitations (MIT).
