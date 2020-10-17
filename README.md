# FB8796506 - xcodebuild build does not write logs, errors or warnings to the result bundle

This project has some simple compile warnings in `AppDelegate.swift`.

```
xcodebuild build -resultBundlePath Build.xcresult CODE_SIGN_IDENTITY="" CODE_SIGNING_REQUIRED=NO CODE_SIGN_ENTITLEMENTS="" CODE_SIGNING_ALLOWED=NO
```

Inspect the `Build.xcresult` bundle in Xcode with:

```
open Test.xcresult
```

Observe that the result bundle opens and can be browsed but has no details. No logs, no warnings.

> Did I misinterpret the documentation? Is the `-resultBundlePath` only available when running tests? If tthat is the case, would you consider taking a feedback suggestion to allow this for `build` too?

