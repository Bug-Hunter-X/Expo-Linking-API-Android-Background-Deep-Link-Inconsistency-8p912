# Expo Linking API Android Background Deep Link Inconsistency

This repository demonstrates an uncommon bug related to the Expo `Linking` API on Android. The issue occurs when handling deep links while the app is already running in the background. The `Linking.addEventListener` callback isn't consistently triggered, preventing proper deep link processing.

## Bug Reproduction

1. Clone this repository.
2. Run the app on an Android device or emulator.
3. Send a deep link to the app while it's running in the background.
4. Observe that the app may not process the deep link as expected.

## Solution

The proposed solution involves using a more robust approach that combines `Linking.addEventListener` with a background task management strategy (for instance, using a service or headlesstask) to ensure the deep link is always processed reliably, even when the app is in the background.