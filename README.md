# Aura-AI
🚀 Aura AI – Universal Voice-Controlled Smartphone Assistant

<p align="center">
  <b>Your Smartphone. Your Voice. Your AI Assistant.</b>
</p><p align="center">
  A smart, voice-controlled Android assistant designed to make smartphone interaction easier, safer, and more accessible across different device configurations.
</p>---

📌 Overview

Aura AI is an intelligent Android voice assistant designed to enable hands-free smartphone interaction through natural voice commands.

The project focuses on providing a unified assistant experience across smartphones with different hardware configurations, including budget devices, older smartphones, and modern Android devices.

Aura AI aims to simplify everyday smartphone operations through voice recognition, intelligent command processing, device compatibility analysis, smart routines, and permission-based device interactions.

Instead of navigating multiple applications manually, users can interact with their smartphones using voice commands.

✨ Key Features

🎙️ 1. Voice-Controlled Interaction

- Natural voice command recognition.
- Configurable "Hey Aura" wake-word experience.
- Text-to-speech responses.
- Multilingual voice support, including English, Telugu, Hindi, Tamil, and Kannada.
- Hands-free interaction through a foreground voice service.

📱 2. Universal Device Compatibility

Aura AI analyzes device hardware and recommends an appropriate operating mode.

Three operating modes are provided:

Mode| Description
Light Mode| Optimized for older and budget smartphones.
Standard Mode| Balanced experience for mid-range devices.
Advanced Mode| Intended for higher-performance smartphones.

Device information includes:

- Manufacturer and device model.
- Android version and API level.
- CPU architecture.
- Total and available RAM.
- Storage availability.
- Battery percentage and charging status.
- Network connectivity.
- Speech recognition availability.

⚙️ 3. Smartphone Operations

Aura AI includes device-control functionality for supported Android operations.

Examples include:

- Launching installed applications.
- Opening WhatsApp, YouTube, Maps, Camera, Chrome, and Settings.
- Flashlight control.
- Volume adjustment.
- Media controls.
- Alarm creation.
- Phone calling and SMS operations where permissions are granted.

🔐 4. Security and Privacy

Security is an important part of Aura AI.

Implemented security-related functionality includes:

- Permission-aware device operations.
- Confirmation prompts for sensitive actions.
- Privacy mode.
- Emergency stop functionality.
- Security event logging.
- Voice profile enrollment and verification interfaces.
- Exclusion of password-protected fields when reading screen content.

🧠 5. Smart Routines

Users can create and manage routines for frequently performed operations.

Example routines include:

- Good Morning.
- Bedtime.
- Driving Mode.
- Custom voice-triggered routines.

Routine functionality includes:

- Routine creation and management.
- Voice-triggered execution.
- Routine steps.
- Execution status tracking.

♿ 6. Accessibility Integration

Aura AI includes an Android Accessibility Service designed to support hands-free screen understanding.

Capabilities include:

- Observing application window changes.
- Reading accessible screen text.
- Identifying clickable screen elements.
- Excluding password fields from screen-text extraction.

Accessibility functionality requires explicit user authorization through Android settings.

---

🛠️ Technology Stack

Category| Technologies
Programming Language| Kotlin
Platform| Android
UI Framework| Jetpack Compose
Design Components| Material 3
Architecture| MVVM-oriented architecture
Local Database| Room Database
Asynchronous Processing| Kotlin Coroutines & Flow
Navigation| Navigation Compose
Preferences| DataStore
AI Integration| Firebase AI dependencies
Networking| Retrofit & OkHttp
JSON Processing| Moshi
Dependency Injection| Application-managed components
Testing| JUnit, Robolectric, AndroidX Testing
Build System| Gradle with Kotlin DSL

---

🏗️ Project Architecture

Aura AI follows a modular structure to separate user interface components, application logic, device operations, and local data management.

Aura-AI/
│
├── app/
│   ├── src/
│   │   ├── main/
│   │   │   ├── java/com/example/
│   │   │   │   │
│   │   │   ├── core/
│   │   │   │   ├── data/
│   │   │   │   ├── ui/
│   │   │   │   │
│   │   │   ├── MainActivity.kt
│   │   │   └── AuraApplication.kt
│   │   │
│   │   ├── res/
│   │   ├── AndroidManifest.xml
│   │   ├── test/
│   │   └── androidTest/
│   │
│   └── build.gradle.kts
│
├── gradle/
│   └── libs.versions.toml
│
├── build.gradle.kts
├── settings.gradle.kts
├── gradle.properties
├── .gitignore
└── .env.example

Core Modules

Module| Responsibility
"core/voice"| Voice recognition and voice profile management
"core/engine"| Intent parsing, action planning, and safety management
"core/device"| Smartphone hardware and system operations
"core/hardware"| Device compatibility and hardware diagnostics
"core/services"| Background voice and accessibility services
"core/routine"| Smart routine execution
"data/local"| Room database and data access objects
"data/repository"| Data repository management
"ui/screens"| Application screens
"ui/components"| Reusable UI components
"ui"| ViewModel and application state management

---

📋 Requirements

To build and run Aura AI, you need:

- Android Studio.
- Android SDK.
- JDK 11 or compatible Gradle-supported JDK.
- Kotlin support.
- Android smartphone or emulator.
- Internet connection for online-dependent features.
- Android microphone and notification permissions.

Minimum Android SDK: API 26 (Android 8.0).

Target Android SDK: API 36.

Some functionalities depend on Android version, device hardware, manufacturer restrictions, and granted permissions.

---

🚀 Installation and Setup

1. Clone the Repository

git clone https://github.com/udaykiran2503/Aura-AI.git

2. Open the Project

1. Open Android Studio.
2. Select Open.
3. Navigate to the cloned "Aura-AI" directory.
4. Wait for Gradle synchronization to complete.

3. Configure Environment Variables

The project includes an ".env.example" file.

If you enable or use Gemini API functionality, configure the required API key using your development environment's secrets configuration.

Example:

GEMINI_API_KEY=YOUR_GEMINI_API_KEY

Never upload actual API keys, passwords, or private credentials to GitHub.

4. Build the Application

From the project root directory:

./gradlew assembleDebug

On Windows PowerShell:

.\gradlew.bat assembleDebug

5. Run the Application

- Connect an Android smartphone using USB debugging, or launch an emulator.
- Select the device in Android Studio.
- Click Run.
- Grant the required permissions when prompted.

---

🎤 Example Voice Commands

The following are examples of intended commands supported by the application's command-processing functionality:

Voice Command| Expected Operation
"Hey Aura"| Wake-word interaction
"Turn on flashlight"| Enable flashlight
"Turn off flashlight"| Disable flashlight
"Open WhatsApp"| Launch WhatsApp
"Open YouTube"| Launch YouTube
"Open Settings"| Open Android Settings
"Find my phone"| Trigger supported phone-finding behavior
"Good Morning"| Execute matching routine
"Good Night"| Execute bedtime routine
"Stop"| Emergency stop command

Actual execution depends on the relevant implementation, permissions, device capabilities, and Android restrictions.

---

🔒 Permissions and Privacy

Aura AI uses Android permissions to provide its functionality.

Depending on the features enabled, permissions may include:

- "RECORD_AUDIO" – Voice input.
- "POST_NOTIFICATIONS" – Foreground service notifications.
- "FOREGROUND_SERVICE" – Background service execution.
- "FOREGROUND_SERVICE_MICROPHONE" – Microphone foreground service.
- "CAMERA" – Flashlight hardware access.
- "CALL_PHONE" – Direct phone calling.
- "READ_CONTACTS" – Contact lookup.
- "SEND_SMS" – SMS functionality.
- "INTERNET" – Online services.
- "ACCESS_NETWORK_STATE" – Network availability.
- "BIND_ACCESSIBILITY_SERVICE" – Accessibility service authorization.

Aura AI does not bypass Android security restrictions. Sensitive operations require appropriate permissions and user authorization.

---

📊 Development Goals

Aura AI is designed around the following objectives:

1. Make smartphone interaction possible through voice commands.
2. Improve accessibility and hands-free usability.
3. Adapt functionality to different hardware configurations.
4. Provide intelligent command interpretation.
5. Simplify repetitive tasks through smart routines.
6. Maintain user privacy and security.
7. Reduce dependency on manual touchscreen interactions.

---

🚧 Future Enhancements

Potential future improvements include:

- Advanced offline AI command processing.
- More reliable wake-word detection.
- Expanded multilingual natural language understanding.
- Improved cross-application automation.
- AI-powered contextual assistance.
- More advanced voice authentication.
- Device-specific performance optimization.
- Improved accessibility-based navigation.
- Additional offline capabilities for older smartphones.

---

⚠️ Important Limitations

Aura AI is an Android application and operates within Android's security and background-execution restrictions.

- Continuous background listening depends on Android foreground-service rules.
- Some manufacturers restrict background execution aggressively.
- Certain operations require explicit runtime permissions.
- Accessibility automation requires manual activation by the user.
- Not every Android device supports every hardware feature.
- Some online AI functionality requires API configuration and network connectivity.

Universal compatibility is a development goal, not a guarantee that every feature works on every smartphone.

---

🤝 Contributing

Contributions, suggestions, bug reports, and feature improvements are welcome.

To contribute:

1. Fork this repository.
2. Create a feature branch.
3. Implement your changes.
4. Test your modifications.
5. Submit a pull request.

---

📄 License

This project is currently provided for educational and development purposes.

A formal open-source license can be added by the repository owner.

---

👨‍💻 Author

Uday Kiran

- GitHub: "@udaykiran2503" (https://github.com/udaykiran2503)
- LinkedIn: "Uday Kiran" (https://www.linkedin.com/in/uday-kiran-n)

---

<p align="center">
  <b>✨ Aura AI – Experience Your Smartphone Without Touching It. ✨</b>
</p>
