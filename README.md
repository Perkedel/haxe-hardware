haxe-hardware (but it's Lime version)
=============

Simple OpenFL extension for accessing android device hardware methods. Lime version, due to missing JNI in the latest OpenFL it seems.

Currently implements methods to use the android vibrator, wake up, and access screen
dimensions.

Install Lime via `haxelib install lime`

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

### Copyright
- [haxe-hardware (upstream)](https://github.com/ktravis/haxe-hardware ). Copyright (c) @ktravis - all rights reserved. (MIT)
- This thing, just part of the mod. Copyright (c) Perkedel Technologies - .... rights reserved. (GNU LGPL v3)

### Why this mod?
JOELwindows7: It is provided here due to incompatibility with current Haxe standard. I was tried to use this for my game mod, inspiring from the original game author's previous work that uses this library. It errored because it lacked 64-bit ARM library binaries. So here I fixed it. I may have more features coming because according to this [Pull request response](https://github.com/ktravis/haxe-hardware/pull/2#issuecomment-873434236 ), he seems have no plan of going to further work on it and may archive it in some time.  
btw, I'm sorry for being rude. I just... don't want somebody who fork my stuffs (modding), makes it proprietary, just like the MIT allows you to do so.
