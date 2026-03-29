# CardioCare AI - Flutter

A comprehensive heart disease detection mobile application built with Flutter and BLoC state management. This app provides AI-powered risk assessment, health tracking, and personalized recommendations for cardiovascular health.

## Complete frontend and backend source code.

📄 Full documentation: [COMPREHENSIVE_PROJECT_DOCUMENTATION.md](COMPREHENSIVE_PROJECT_DOCUMENTATION.md)
## 🎯 Features

- **Heart Health Assessment**: Comprehensive health check questionnaire with medical parameters
- **AI-Powered Risk Analysis**: Calculate cardiovascular risk based on multiple factors
- **Risk Visualization**: Beautiful UI showing risk levels with color-coded indicators
- **Detailed Explanations**: AI-generated explanations of contributing risk factors
- **Assessment History**: Track your health assessments over time
- **User Profile**: Manage personal information and emergency contacts
- **Persistent Storage**: All data saved locally using SharedPreferences

## 🏗️ Architecture

This project follows Clean Architecture principles with BLoC (Business Logic Component) pattern for state management.

### Project Structure

```
lib/
├── blocs/                    # BLoC files for state management
│   ├── assessment_bloc.dart
│   ├── assessment_event.dart
│   ├── assessment_state.dart
│   ├── profile_bloc.dart
│   ├── profile_event.dart
│   └── profile_state.dart
├── config/                   # Configuration files
│   ├── app_colors.dart      # Color constants
│   └── app_constants.dart   # App-wide constants
├── models/                   # Data models
│   ├── health_assessment.dart
│   └── user_profile.dart
├── screens/                  # UI screens
│   ├── splash_screen.dart
│   ├── home_screen.dart
│   ├── check_screen.dart
│   ├── analyzing_screen.dart
│   ├── result_screen.dart
│   ├── explain_screen.dart
│   ├── history_screen.dart
│   └── profile_screen.dart
├── utils/                    # Utility classes
│   ├── risk_calculator.dart
│   ├── storage_service.dart
│   └── helpers.dart
├── widgets/                  # Reusable widgets
└── main.dart                # App entry point
```

## 📦 Dependencies

### Core Dependencies
- `flutter_bloc: ^8.1.3` - State management
- `equatable: ^2.0.5` - Value equality
- `shared_preferences: ^2.2.2` - Local storage
- `google_fonts: ^6.1.0` - Custom fonts
- `intl: ^0.19.0` - Internationalization
- `uuid: ^4.3.3` - Unique ID generation

### UI Dependencies
- `animate_do: ^3.1.2` - Animations
- `percent_indicator: ^4.2.3` - Progress indicators
- `fl_chart: ^0.66.0` - Charts
- `shimmer: ^3.0.0` - Loading effects
- `flutter_slidable: ^3.0.1` - Slidable widgets
- `flutter_svg: ^2.0.9` - SVG support

### Dev Dependencies
- `flutter_lints: ^3.0.0` - Linting rules
- `bloc_test: ^9.1.5` - BLoC testing

## 🚀 Getting Started

### Prerequisites

- Flutter SDK (3.0.0 or higher)
- Dart SDK (3.0.0 or higher)
- Android Studio / VS Code with Flutter extension
- iOS Simulator (for macOS) or Android Emulator

### Installation

1. **Clone or navigate to the project directory:**
   ```bash
   cd cardiocare_flutter
   ```

2. **Install dependencies:**
   ```bash
   flutter pub get
   ```

3. **Run the app:**
   ```bash
   flutter run
   ```

### Running on Specific Platforms

**Android:**
```bash
flutter run -d android
```

**iOS (macOS only):**
```bash
flutter run -d ios
```

**Web:**
```bash
flutter run -d chrome
```

## 🧪 Testing

Run unit and widget tests:
```bash
flutter test
```

Run tests with coverage:
```bash
flutter test --coverage
```

## 🏥 How It Works

### 1. Health Assessment Flow
1. User fills out comprehensive health questionnaire
2. Data includes: age, sex, chest pain type, blood pressure, cholesterol, etc.
3. Form validation ensures all required fields are completed

### 2. Risk Calculation
The app calculates cardiovascular risk based on:
- **Age**: Higher age increases risk
- **Chest Pain Type**: Typical angina is high risk
- **Blood Pressure**: Hypertension indicator
- **Cholesterol Levels**: High cholesterol increases risk
- **Exercise-Induced Angina**: Strong risk indicator
- **ST Depression**: Cardiac ischemia marker
- **Number of Vessels**: Blocked coronary arteries
- **Thalassemia**: Blood flow defects

### 3. Risk Levels
- **Low Risk (0-25%)**: Green indicators, maintenance recommendations
- **Medium Risk (25-70%)**: Yellow indicators, lifestyle modifications suggested
- **High Risk (70-95%)**: Red indicators, urgent medical consultation recommended

### 4. Persistent Data
- All assessments saved locally
- History tracking with timestamps
- User profile information stored securely
- No internet connection required

## 🎨 UI/UX Features

- **Modern Material Design**: Clean, intuitive interface
- **Smooth Animations**: Engaging user experience
- **Color-Coded Risk Levels**: Easy visual understanding
- **Responsive Layout**: Works on all screen sizes
- **Dark/Light Theme Support**: (Coming soon)
- **Accessibility**: Screen reader support, high contrast

## 📱 Screens Overview

### Splash Screen
- Animated logo with pulse effect
- Heartbeat wave animation
- Auto-navigation to home

### Home Screen
- Dashboard with latest assessment
- Quick access cards
- Bottom navigation
- Greeting and summary

### Check Screen
- Multi-section form
- Input validation
- Helper text and hints
- Progress indication

### Analyzing Screen
- Loading animation
- Progress steps
- Heartbeat visualization
- 3-second analysis simulation

### Result Screen
- Circular progress indicator
- Risk level badge
- Recommendations list
- Action buttons (explain, download, share)

### Explain Screen
- Contributing factors breakdown
- Impact levels (high/medium/low)
- Contribution percentages
- Detailed explanations

### History Screen
- Timeline of assessments
- Statistics summary
- Swipe to delete
- Tap to view details

### Profile Screen
- User information
- Emergency contacts
- Settings access
- Logout option

## 🔐 Data Privacy

- All data stored locally on device
- No cloud sync or external servers
- User controls all their data
- Can delete assessments anytime
- No tracking or analytics

## 🛠️ Customization

### Changing Colors
Edit `lib/config/app_colors.dart` to customize the color scheme.

### Modifying Risk Calculation
Edit `lib/utils/risk_calculator.dart` to adjust risk scoring algorithm.

### Adding New Fields
1. Update `FormData` model in `lib/models/health_assessment.dart`
2. Add form fields in `lib/screens/check_screen.dart`
3. Update risk calculator logic

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📞 Support

For support, email support@cardiocare.ai or create an issue in the repository.

## ⚠️ Medical Disclaimer

This application is for informational purposes only and is not intended to be a substitute for professional medical advice, diagnosis, or treatment. Always seek the advice of your physician or other qualified health provider with any questions you may have regarding a medical condition.

## 🙏 Acknowledgments

- Flutter team for the amazing framework
- BLoC library maintainers
- UI design inspired by modern health apps
- Medical guidelines from cardiovascular research

---

**Built with ❤️ using Flutter**
