# XCAssetsSample

This sample project try to expose a complex case of using multiple assets with multiple targets.

It has originally been created to test [CocoaPods/CocoaPods#3263](https://github.com/CocoaPods/CocoaPods/pull/3263)

### Structure

The project contains 3 App targets

* each target is linked with a `Common.xcassets` (same for the 3 targets)
* each target also has its own `Images.xcassets` (different for each target)
* 2 of the 3 app targets have a dependency defined in their `Podfile` to a pod that contains an `xcassets` in its spec's `resources`.

The aim of this sample is to ensure that `pod install` will integrate assets properly
and that each app target will contain the expected assets (no more, no less), so that
we can consider [CocoaPods/CocoaPods#1546](https://github.com/CocoaPods/CocoaPods/issues/1546) as fixed.
