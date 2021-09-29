# HLS - Training day 9
Congrats!!!!
You learn all knowledges around ReactJS. Let move on React Native

## Learn the Basics

If you're feel boring, You can watch a video youtube
- English: https://www.youtube.com/watch?v=qSRrxpdMpVc
- Vietnamese: https://www.youtube.com/watch?v=qiwdV4lT59w

React Native is like React, but it uses native components instead of web components as building blocks. So to understand the basic structure of a React Native app, you need to understand some of the basic React concepts, like JSX, components, `state`, and `props`. If you already know React, you still need to learn some React-Native-specific stuff, like the native components. This tutorial is aimed at all audiences, whether you have React experience or not.

Let's do this thing.

### Hello World

In accordance with the ancient traditions of our people, we must first build an app that does nothing except say `Hello, world!`. Here it is:

```
import React from 'react';
import { StyleSheet, Text, View } from 'react-native';

const App: () => Node = () => {
  return (
    <View style={styles.container}>
      <Text style={styles.title}>HLS</Text>
      <Text>Hello world</Text>
    </View>
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

If you are feeling curious, you can play around with sample code directly in the web simulators. You can also paste it into your App.js file to create a real app on your local machine.

## What's going on here?
The other unusual thing in this code example is `<View> <Text>HLS</Text> <Text>Hello world</Text> </View>`. It looks like HTML on the web, except instead of web things like `<div>` or `<span>`, you use React components. In this case, `<Text>` is a Core Component that displays some text and View is like the `<div>` or `<span>`.

![Core](./assets/core.svg)

## Transfer components
React Native has many Core Components for everything from form controls to activity indicators. You can find them all documented in the API section. You will mostly work with the following Core Components

|REACT NATIVE UI COMPONENT|ANDROID VIEW|IOS VIEW|WEB ANALOG|DESCRIPTION|
|--|--|--|--|--|
|`<View>`|`<ViewGroup>`|`<UIView>`|A non-scrollling `<div>`	|A container that supports layout with flexbox, style, some touch handling, and accessibility controls
|
|`<Text>`	|`<TextView>`	|`<UITextView>`	|`<p>`	|Displays, styles, and nests strings of text and even handles touch events
|
|`<Image>`	|`<ImageView>`	|`<UIImageView>`	|`<img>`	|Displays different types of images|
|`<ScrollView>`	|`<ScrollView>`	|`<UIScrollView>`	|`<div>`	|A generic scrolling container that can contain multiple components and views
|
|`<TextInput>`	|`<EditText>`	|`<UITextField>`	|`<input type="text">`	|Allows the user to enter text
|

As you see React Native components is a special component of React Components. So when do you re-think from React Js to React native. It's so simple to start

![sample](./assets/sample.svg)

## Core Components and APIs

### Basic Components
|Components|Note|
|--|--|
|[View](https://reactnative.dev/docs/view) |The most fundamental component for building a UI.|
|[Text](https://reactnative.dev/docs/text) |A component for displaying text.|
|[Image](https://reactnative.dev/docs/image) |A component for displaying images.|
|[TextInput](https://reactnative.dev/docs/textinput) |A component for inputting text into the app via a keyboard.|
|[ScrollView](https://reactnative.dev/docs/scrollview)|Provides a scrolling container that can host multiple components and views.|
|[StyleSheet](https://reactnative.dev/docs/stylesheet)|Provides an abstraction layer similar to CSS stylesheets..|

### User Interface
These common user interface controls will render on any platform.


|Components|Note|
|--|--|
|[Button](https://reactnative.dev/docs/button) |A basic button component for handling touches that should render nicely on any platform.|
|[Switch](https://reactnative.dev/docs/switch) |Renders a boolean input.|

### List Views
Unlike the more generic ScrollView, the following list view components only render elements that are currently showing on the screen. This makes them a performant choice for displaying long lists of data.

|Components|Note|
|--|--|
|[FlatList](https://reactnative.dev/docs/flatlist) |A component for rendering performant scrollable lists.|
|[SectionList](https://reactnative.dev/docs/sectionlist) |Like FlatList, but for sectioned lists.|

### Android Components and APIs
Many of the following components provide wrappers for commonly used Android classes.

|Components|Note|
|--|--|
|[BackHandler](https://reactnative.dev/docs/BackHandler) |Detect hardware button presses for back navigation.|
|[DrawerLayoutAndroid](https://reactnative.dev/docs/DrawerLayoutAndroid) |Renders a DrawerLayout on Android.|
|[PermissionsAndroid](https://reactnative.dev/docs/PermissionsAndroid) |Provides access to the permissions model introduced in Android M.|
|[ToastAndroid](https://reactnative.dev/docs/ToastAndroid) |Create an Android Toast alert.|

### iOS Components and APIs
Many of the following components provide wrappers for commonly used UIKit classes.


|Components|Note|
|--|--|
|[ActionSheetIOS](https://reactnative.dev/docs/ActionSheetIOS) |API to display an iOS action sheet or share sheet.|

### Others
These components may be useful for certain applications. For an exhaustive list of components and APIs, check out the sidebar to the left (or menu above, if you are on a narrow screen).

|Components|Note|
|--|--|
|[ActivityIndicator](https://reactnative.dev/docs/ActivityIndicator) |Displays a circular loading indicator.|
|[Alert](https://reactnative.dev/docs/Alert) |Launches an alert dialog with the specified title and message.|
|[Animated](https://reactnative.dev/docs/Animated) |A library for creating fluid, powerful animations that are easy to build and maintain.|
|[Dimensions](https://reactnative.dev/docs/Dimensions) |Provides an interface for getting device dimensions.|
|[KeyboardAvoidingView](https://reactnative.dev/docs/KeyboardAvoidingView) |Provides a view that moves out of the way of the virtual keyboard automatically.|
|[Linking](https://reactnative.dev/docs/Linking) |Provides a general interface to interact with both incoming and outgoing app links.|
|[Modal](https://reactnative.dev/docs/Modal) |Provides a simple way to present content above an enclosing view.|
|[PixelRatio](https://reactnative.dev/docs/Animated) |Provides access to the device pixel density.|
|[RefreshControl](https://reactnative.dev/docs/RefreshControl) |This component is used inside a ScrollView to add pull to refresh functionality.|

## Reference
- https://reactnative.dev
- https://www.tutorialspoint.com/react_native/react_native_overview.htm