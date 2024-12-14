# React Native Dimensions API Inconsistency on Android

This repository demonstrates a bug related to the `Dimensions` API in React Native on Android. The issue arises when attempting to retrieve screen dimensions after a device rotation or screen size change. The values returned by `Dimensions.get('window')` or `Dimensions.get('screen')` may be incorrect or inconsistent, leading to layout problems and unexpected rendering behavior.

## Steps to Reproduce

1. Clone this repository.
2. Run the React Native app on an Android device or emulator.
3. Observe the initially correct layout.
4. Rotate the device or change the screen size.
5. Notice the layout inconsistencies or misalignment of UI elements.

## Solution

The provided solution demonstrates using the `onLayout` prop to handle layout changes and ensures accurate and up-to-date dimensions. This approach is more robust than relying solely on the initial dimensions returned by `Dimensions.get()`.