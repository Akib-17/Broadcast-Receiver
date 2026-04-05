# Broadcast Receiver App

A Flutter mobile application demonstrating broadcast receivers, media playback, and gesture handling.

## Assignment Details

**Course:** CSE 489 - Mobile Application Development  
**Assignment:** Assignment 2  
**Platform:** Flutter (Cross-platform)

## Features Implemented

### 1. Broadcast Receiver
- **Custom Broadcast Receiver**: Send and receive custom text messages using Dart Streams
  - Selection screen with dropdown/spinner
  - Text input screen for custom messages
  - Receiver screen that displays broadcast messages in real-time
  
- **System Battery Notification Receiver**: Monitor device battery status
  - Real-time battery percentage display
  - Battery state monitoring (charging, discharging, full)
  - Visual indicators with color-coded battery levels

### 2. Image Scale
- Load images from the internet
- Pinch-to-zoom gesture support using `InteractiveViewer`
- Pan and drag functionality
- Double-tap to reset zoom

### 3. Video Player
- Stream video from the internet
- Play/Pause controls
- Seek functionality with progress bar
- Forward/Rewind 10 seconds
- Time display (current position / total duration)

### 4. Audio Player
- Stream audio from the internet
- Play/Pause/Stop controls
- Seek functionality with progress slider
- Time display and progress tracking
- Visual feedback with animated UI

## Technical Implementation

### Architecture
- **Pure Flutter/Dart**: No native Android/iOS code required
- **Stream-based Broadcasting**: Uses Dart's `StreamController` for custom broadcasts
- **State Management**: `StatefulWidget` with `setState()`
- **Navigation**: Material Design Navigation Drawer

### Packages Used
```yaml
dependencies:
  battery_plus: ^6.0.0      # Battery monitoring
  video_player: ^2.8.0      # Video playback
  audioplayers: ^6.0.0      # Audio playback
```

### Project Structure
```
lib/
├── main.dart                          # App entry point with navigation drawer
├── services/
│   └── broadcast_service.dart         # Stream-based broadcast service
└── screens/
    ├── broadcast/
    │   ├── broadcast_selection_screen.dart
    │   ├── custom_input_screen.dart
    │   ├── custom_receiver_screen.dart
    │   └── battery_screen.dart
    ├── image_scale_screen.dart
    ├── video_screen.dart
    └── audio_screen.dart
```

## How to Run

### Prerequisites
- Flutter SDK (3.9.2 or higher)
- Android Studio / VS Code with Flutter extensions
- Android Emulator or Physical Device

### Installation Steps

1. **Clone or navigate to the project directory**
   ```bash
   cd broadcast_receiver
   ```

2. **Install dependencies**
   ```bash
   flutter pub get
   ```

3. **Run the app**
   ```bash
   flutter run
   ```

   Or use your IDE's run button.

## Usage Guide

### Navigation
- Open the **Navigation Drawer** by tapping the menu icon (☰) or swiping from the left edge
- Select any feature from the drawer menu

### Broadcast Receiver
1. Select "Broadcast Receiver" from the drawer
2. Choose between:
   - **Custom broadcast receiver**: Enter a text message and send it to the receiver
   - **System battery notification receiver**: View real-time battery status

### Image Scale
1. Select "Image Scale" from the drawer
2. Use pinch gestures to zoom in/out
3. Drag to pan around the zoomed image
4. Double-tap to reset zoom level

### Video Player
1. Select "Video" from the drawer
2. Tap the play button to start the video
3. Use the slider to seek to different positions
4. Use forward/rewind buttons for quick navigation

### Audio Player
1. Select "Audio" from the drawer
2. Tap the play button to start audio playback
3. Use the slider to seek through the audio
4. Tap stop to reset playback

## Key Learning Outcomes

1. **Flutter UI Development**: Material Design components, layouts, and navigation
2. **State Management**: Managing app state with StatefulWidget
3. **Streams**: Using Dart Streams for event-driven communication
4. **Package Integration**: Working with third-party Flutter packages
5. **Gesture Detection**: Implementing touch gestures (pinch, pan, tap)
6. **Media Playback**: Video and audio streaming and controls
7. **System Integration**: Accessing device battery information

## Beginner-Friendly Approach

This implementation uses:
- ✅ **Pure Flutter/Dart** - No native Android/Java/Kotlin code
- ✅ **Well-commented code** - Clear explanations throughout
- ✅ **Simple architecture** - Easy to understand file structure
- ✅ **Standard packages** - Community-maintained, well-documented packages
- ✅ **Material Design** - Familiar UI patterns and components

## Notes

- **Internet Required**: Video, audio, and image features require an active internet connection
- **Permissions**: Battery monitoring works automatically (handled by the package)
- **Cross-platform**: This app works on Android, iOS, Web, and Desktop (with minor adjustments)

## Troubleshooting

### Dependencies not installing
```bash
flutter clean
flutter pub get
```

### App not running
```bash
flutter doctor
```
Check for any issues and follow the suggested fixes.

### Video/Audio not playing
- Ensure you have an active internet connection
- Check if the URLs are accessible
- Try restarting the app

## Future Enhancements

- Add local file support for video/audio
- Implement volume controls
- Add playlist functionality
- Support for multiple image sources
- Offline mode with cached media

## License

This project is created for educational purposes as part of CSE 489 coursework.
