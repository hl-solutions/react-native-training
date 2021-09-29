# HLS - Training day 8
Congrats!!!!
You learn all knowledges around ReactJS. Let move on React Native

## Setting up React Native the development environment

If you're feel boring, You can watch a video youtube
- English: https://www.youtube.com/watch?v=0DhQd_EK1Ng
- English: https://www.youtube.com/watch?v=0-S5a0eXPoc
- Vietnamese: https://www.youtube.com/watch?v=S2iyaNWXxWM
- Vietnamese: https://www.youtube.com/watch?v=wccsinPgE4k

Follow these instructions if you need to build native code in your project. For example, if you are integrating React Native into an existing application, or if you "ejected" from Expo, you'll need this section.

The instructions are a bit different depending on your development operating system, and whether you want to start developing for iOS or Android. If you want to develop for both Android and iOS, that's fine - you can pick one to start with, since the setup is a bit different.

## Development OS
For android setup and other OS you check check at: [React native setup](https://reactnative.dev/docs/environment-setup)
### Macos
#### Installing dependencies
You will need Node, Watchman, the React Native command line interface, Xcode and CocoaPods.

While you can use any editor of your choice to develop your app, you will need to install Xcode in order to set up the necessary tooling to build your React Native app for iOS.

**Node & Watchman**

```
brew install node
brew install watchman
```

If you have already installed Node on your system, make sure it is Node 12 or newer.
Watchman is a tool by Facebook for watching changes in the filesystem. It is highly recommended you install it for better performance.

**Xcode**
The easiest way to install Xcode is via the Mac App Store. Installing Xcode will also install the iOS Simulator and all the necessary tools to build your iOS app.

If you have already installed Xcode on your system, make sure it is version 10 or newer.

**Command Line Tools**
You will also need to install the Xcode Command Line Tools. Open Xcode, then choose "Preferences..." from the Xcode menu. Go to the Locations panel and install the tools by selecting the most recent version in the Command Line Tools dropdown.

**Installing an iOS Simulator in Xcode**
To install a simulator, open Xcode > Preferences... and select the Components tab. Select a simulator with the corresponding version of iOS you wish to use.

**CocoaPods**
CocoaPods is built with Ruby and it will be installable with the default Ruby available on macOS. You can use a Ruby Version manager, however we recommend that you use the standard Ruby available on macOS unless you know what you're doing.

Using the default Ruby install will require you to use sudo when installing gems. (This is only an issue for the duration of the gem installation, though.)

```
sudo gem install cocoapods
```


## React Native Command Line Interface#
React Native has a built-in command line interface. Rather than install and manage a specific version of the CLI globally, we recommend you access the current version at runtime using npx, which ships with Node.js. With npx react-native <command>, the current stable version of the CLI will be downloaded and executed at the time the command is run.

### Creating a new application
You can use React Native's built-in command line interface to generate a new project. Let's create a new React Native project called "HLS"
```
npx react-native init HLS
```

**[Optional] Using a specific version or template**

If you want to start a new project with a specific React Native version, you can use the --version argument:

```
npx react-native init HLS --version X.XX.X
```

You can also start a project with a custom React Native template, like TypeScript, with --template argument:
```
npx react-native init HLS --template react-native-template-typescript
```

### Running your React Native application
#### Step 1: Start Metro
First, you will need to start Metro, the JavaScript bundler that ships with React Native. Metro "takes in an entry file and various options, and returns a single JavaScript file that includes all your code and its dependencies."[—Metro Docs](https://facebook.github.io/metro/docs/concepts/)

To start Metro, run npx react-native start inside your React Native project folder:
```
npx react-native start
```

#### Step 2: Start your application
Let Metro Bundler run in its own terminal. Open a new terminal inside your React Native project folder. Run the following:

```
npx react-native run-ios
```
You should see your new app running in the iOS Simulator shortly.
[reactnative](./assets/reactnative.png)

Here the edit APP component at `App.js`
```
import React from 'react';
import type {Node} from 'react';
import { Colors } from 'react-native/Libraries/NewAppScreen';import { SafeAreaView, StatusBar, StyleSheet, Text, useColorScheme, View, } from 'react-native';

const App: () => Node = () => {
  const isDarkMode = useColorScheme() === 'dark';

  const backgroundStyle = {
    flex: 1,
    backgroundColor: isDarkMode ? Colors.darker : Colors.lighter,
  };

  return (
    <SafeAreaView style={backgroundStyle}>
      <StatusBar barStyle={isDarkMode ? 'light-content' : 'dark-content'} />
      <View style={styles.container}>
        <Text style={styles.title}>HLS</Text>
        <Text>Hello world</Text>
        <Text>Welcome to React Native</Text>
      </View>
    </SafeAreaView>
  );
};

const styles = StyleSheet.create({
  container: {
    flex: 1,
    padding: 20,
    alignItems: 'center',
    justifyContent: 'center',
  },
  title: {
    fontSize: 24,
    fontWeight: 'bold',
    paddingVertical: 20,
  },
});

export default App;
```
[hls](./assets/hls.png)

## Reference
**Learning Resources**
- https://reactnative.dev/docs/intro-react
- https://www.tutorialspoint.com/react_native/index.htm
