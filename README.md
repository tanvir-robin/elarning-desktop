# E-Learning Desktop App

A Flutter desktop application for e-learning with YouTube video integration.

## Features

- **Cross-platform Support**: Works on macOS, Windows, and Web
- **Firebase Authentication**: Secure user login system
- **Course Management**: View enrolled courses with detailed information
- **YouTube Video Integration**: Play educational videos directly in the app
- **Responsive Design**: Adapts to different screen sizes

## YouTube Video Support

The app includes built-in YouTube video player support with the following features:

### Supported Platforms
- ✅ macOS
- ✅ Windows  
- ✅ Web

### Adding Videos to Courses

To add YouTube videos to a course, include a `videos` array in your course data:

```dart
Map<String, dynamic> courseData = {
  'title': 'Flutter Development Course',
  'description': 'Learn Flutter from scratch',
  'instructor': 'John Doe',
  'duration': '10 hours',
  'price': 99.99,
  'cover': 'https://example.com/course-cover.jpg',
  'videos': [
    'https://www.youtube.com/watch?v=8jLoD9a5hsE',
    'https://www.youtube.com/watch?v=1ukSR1GRtMU',
    'https://www.youtube.com/watch?v=WxwK8jqhWqE',
  ],
};
```

### Sample Educational Videos

The app includes sample educational videos for testing:

- Flutter Tutorial for Beginners
- Dart Programming Tutorial  
- Firebase Tutorial
- React Tutorial
- JavaScript Tutorial

### Video Player Features

- **Auto-play disabled** by default for better user experience
- **HD quality** support
- **Progress indicators** with custom colors
- **Caption support** enabled
- **Responsive design** with 16:9 aspect ratio
- **Error handling** for invalid URLs

## Getting Started

1. Clone the repository
2. Install dependencies: `flutter pub get`
3. Configure Firebase (see Firebase setup below)
4. Run the app: `flutter run`

## Firebase Setup

1. Create a Firebase project
2. Add your Firebase configuration files:
   - `macos/Runner/GoogleService-Info.plist` (for macOS)
   - `android/app/google-services.json` (for Android)
   - `ios/Runner/GoogleService-Info.plist` (for iOS)
3. Enable Authentication and Firestore in Firebase Console

## Dependencies

- `youtube_player_flutter: ^8.1.2` - YouTube video player
- `firebase_core: ^3.14.0` - Firebase core functionality
- `firebase_auth: ^5.6.0` - Firebase authentication
- `cloud_firestore: ^5.6.9` - Firestore database
- `window_manager: ^0.3.7` - Desktop window management

## Platform-Specific Notes

### macOS
- Network permissions configured for YouTube access
- Camera and microphone permissions added for video features

### Windows
- Web content support enabled
- No additional configuration required

### Web
- Works out of the box with web-optimized YouTube player

## Troubleshooting

### Videos Not Playing
1. Check internet connection
2. Verify YouTube URLs are valid
3. Ensure platform permissions are granted
4. Check console for error messages

### Performance Issues
- Videos are loaded on-demand to improve performance
- Consider limiting the number of videos per course for better performance

## Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test on all platforms
5. Submit a pull request

## License

This project is licensed under the MIT License.
