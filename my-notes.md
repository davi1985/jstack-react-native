# What is React Native?

React Native is a framework for building mobile applications using React.

## Mobile Development Types

- Native Development

  - Objective-C/Swift for iOS
  - Java/Kotlin for Android

- Hybrid Development (using HTML, CSS, and JS)
  -Example frameworks: Cordova, Ionic

## Possible Issues:

- Performance and UX can be concerns when using hybrid solutions.

## How to Resolve This?

- Cross-platform development can address some of these issues, enabling you to write code once and deploy it on both iOS and Android.

React Native is used in this context, as it allows building mobile apps using just JavaScript.

## How is This Possible?

- ReactDOM is used for the web.
- React Native is used for mobile apps (iOS and Android).

## Tagline

"Learn once, write anywhere."

## How Does React Native Convert Components to Native Mobile Components?

- <View /> in React Native is converted to UIView on iOS or android.view on Android.
- React Native uses JavaScript with all of its functionalities, libraries, and community-driven packages.

## React Native Architecture (BRIDGE)

In web development, we bundle all JavaScript files into a single bundle.js file for the application (using Webpack).

In React Native, a similar process happens but with Metro bundler.

- Applications built with React Native include the bundle.js file along with iOS and Android native code.

## JavaScript VM

- Hermes is the JavaScript engine responsible for interpreting and optimizing JavaScript code in React Native.

- The JS file contains the business logic, while the native side controls the UI and handles user events.

## Single Thread - JavaScript VM

- In React Native, JavaScript runs in a single thread within the JavaScript VM (e.g., Hermes).
- This means JavaScript operations are executed one after another, ensuring the predictable flow of code execution.

## Multi-threading and UI - Native Code

- The native side (iOS/Android) runs on multiple threads, which allows for concurrent execution of tasks.
- The UI thread is dedicated to rendering the user interface, which helps to ensure smooth and responsive UI updates.

## Shadow Thread - Yoga

- React Native uses Yoga, a layout engine, to calculate the layout of components.
- Yoga runs on a separate thread called the shadow thread.
- The shadow thread performs layout calculations using flexbox, enabling cross-platform layout building.
- Yoga allows React Native to create responsive layouts that adapt to both iOS and Android using the same codebase.

## How Do the JS and Native Sides Communicate?

They communicate via the Bridge.

### Example:

- In the JavaScript file, there is a handlePress() function.
- When triggered, the information is sent via the Bridge.
- The native side listens for this data from the Bridge and executes the press action triggered by the user.

The Bridge is asynchronous and uses a simple JSON structure to transfer data.

## React Native Architecture (FABRIC)

The new RN architecture adopted. The main reason to create new architecture is performance.

The code create in RN using BRIDE and FABRIC is the same.

## CLI x Expo
