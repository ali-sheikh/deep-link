# Deep-Link Example

A simple example demonstrating how to implement deep linking in a React Native application.

## Getting Started

Follow these steps to set up deep linking in your React Native project.

### 1. Install React Native Navigation Packages

Execute the following commands to install the required packages:

```bash
npm install @react-navigation/native
npm install react-native-reanimated react-native-gesture-handler react-native-screens react-native-safe-area-context
npm install @react-navigation/stack
cd ios && pod install
```

### 2. Configure iOS

Modify your `AppDelegate.mm` file in the iOS project:

```objective-c
// Add the header at the top of the file:
#import <React/RCTLinkingManager.h>

// Add this inside `@implementation AppDelegate` above `@end`:
- (BOOL)application:(UIApplication *)application openURL:(NSURL *)url options:(NSDictionary<UIApplicationOpenURLOptionsKey,id> *)options {
  return [RCTLinkingManager application:application openURL:url options:options];
}
```

### 3. Set Up URI Scheme for iOS

Run the following command to add the URI scheme for iOS:

```bash
npx uri-scheme add myreflection --ios
```

### 4. Set Up URI Scheme for Android

Run the following command to add the URI scheme for Android:

```bash
npx uri-scheme add myreflection --android
```

### 5. Test the Deep Link

Start the React Native server:

```bash
npx react-native start
```

Then, open the deep link on your device or emulator:

- For Android:
  ```bash
  npx uri-scheme open "myreflection://details" --android
  ```

- For iOS:
  ```bash
  npx uri-scheme open "myreflection://details" --ios
  ```

## Documentation

For more information, refer to the [React Navigation Deep Linking Documentation](https://reactnavigation.org/docs/deep-linking/).
```

This Markdown file includes headings, code blocks, and a link to the documentation, providing a clear and organized presentation of the instructions.