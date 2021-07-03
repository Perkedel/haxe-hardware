haxe-hardware (but it's Lime version)
=============

Simple OpenFL extension for accessing android device hardware methods. Lime version, due to missing JNI in the latest OpenFL it seems.

Currently implements methods to use the android vibrator, wake up, and access screen
dimensions.

Install via `haxelib git haxe-hardware https://github.com/Perkedel/haxe-hardware`

Add to `project.xml`:

    <haxelib name="openfl" />
    <haxelib name="haxe-hardware" if="android" />

or if you use HaxeFlixel, you do not need `<haxelib name="openfl" />` anymore.

And import into your project (haxe) with:
  
    import Hardware;

Exposed methods are currently:

    public static function vibrate(int duration):Void;
    public static function getScreenWidth():Int;
    public static function getScreenHeight():Int;
    public static function wakeUp():Void;

More can be simply added in the java source file, replicating the function and
corresponding `JNI.createStaticMethod(...)` call in `Hardware.hx`.
  
### Contributions

Thank you to [alagator](https://github.com/alagatar) for contributing `wakeUp()`!
