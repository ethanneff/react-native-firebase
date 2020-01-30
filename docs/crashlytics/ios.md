---
title: iOS Manual Installation
description: Manually integrate Crashlytics into your iOS application.
---

# iOS Manual Installation

The following steps are only required if your environment does not have access to React Native auto-linking.

## CocoaPods Installation

### Add the RNFBCrashlytics Pod

Add the `RNFBCrashlytics` Pod to your projects `/ios/Podfile`:

```ruby{3}
target 'app' do
  # Add the RNFBCrashlytics podspec to your app target:
  pod 'RNFBCrashlytics', :path => '../node_modules/@react-native-firebase/crashlytics'
end
```

### Update Pods & rebuild the project

You may need to update your local Pods repo in order for the Pods to be installed in your project:

```bash
$ cd /ios/
$ pod install --repo-update
```

Once the Pods have installed locally, rebuild your iOS project:

```bash
npx react-native run-ios
```