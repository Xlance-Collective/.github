## Folder Structure

The project follows a recommended folder structure for a Flutter application, promoting modularity, readability, and maintainability.
```bash
├── lib
|   ├── auth  (module)
|   |     ├── model
|   |     |     └── user.dart
|   |     ├── controller
|   |     |     └── auth_controller.dart
|   |     ├── view
|   |     |     ├── log_in_screen.dart
|   |     |     ├── sign_up_screen.dart
|   |     |     └── account_screen.dart
|   |     └── helper
|   |           ├── auth_mixin.dart
|   |           └── user_role_enum.dart 
|   |
|   ├── controller
|   |     └── setting_controller.dart
|   |
|   ├── service
|   |     ├── push_notification_service.dart
|   |     ├── excel_service.dart
|   |     ├── printer_service.dart
|   |     └── payment_service.dart
|   |
|   ├── view
|   |     ├── components
|   |     |      ├── loading_widget.dart
|   |     |      └── text_input_widget.dart
|   |     | 
|   |     ├── main_screen.dart
|   |     ├── splash_screen.dart
|   |     └── setting_screen.dart
|   | 
│   ├── utils
|   |     ├── constants.dart
|   |     ├── assets.dart
|   |     ├── themes.dart
|   |     ├── colors.dart
|   |     └── general_function.dart
|   |
|   |
|   ├── modules
|   |     ├── product
|   |     |       ├── model
|   |     |       |      ├── product.dart
|   |     |       |      └── cart_item.dart
|   |     |       ├── controller
|   |     |       |      ├── product_controller.dart ( Change Notifider or GetxController with ProductMixin )
|   |     |       |      └── cart_controller.dart
|   |     |       ├── helper
|   |     |       |      ├── product_mixin.dart
|   |     |       |      ├── product_type_enums.dart
|   |     |       |      └── date_formatter.dart
|   |     |       └── view
|   |     |              ├── components
|   |     |              |     ├── product_card_widget.dart
|   |     |              |     └── category_bar.dart
|   |     |              ├── product_landing_screen.dart
|   |     |              ├── product_detail_screen.dart
|   |     |              └── cart_screen.dart
|   |     └── order
|   |             ├── model
|   |             |      ├── order.dart
|   |             |      └── order_history.dart
|   |             ├── controller
|   |             |      ├── order_controller.dart ( Change Notifider or GetxController with OrderMixin )
|   |             |      └── history_controller.dart
|   |             ├── helper
|   |             |      ├── order_mixin.dart
|   |             |      ├── order_status_enums.dart
|   |             |      └── order_price_input_formatter.dart
|   |             └── view
|   |                    ├── components
|   |                    |     ├── order_card_widget.dart
|   |                    |     └── payment_dialog.dart
|   |                    ├── order_submit_screen.dart
|   |                    ├── order_detail_screen.dart
|   |                    └── order_history_screen.dart
|   |            
│   ├── main.dart
|   └── app.dart
|
├── android
├── ios
├── assets
├── pubspec.yaml
└── README.md
```
The top-level directory is the `lib` directory, which contains the main entry point file `main.dart` and the source code for the application.

- **models**: This directory is used to store the data models used in the application.
- **services**: It contains classes responsible for interacting with APIs, databases, or other external services.
- **utils**: This directory holds utility classes and functions that provide common functionalities.
- **views**: It contains the UI code for the application.
  - **screens**: This directory is used for top-level screens or pages of the application.
    - **screen_providers**: This directory is used for screen level providers.
    - **screen_controllers**: This directory is used for screen level controllers.
    - **widgets**: This directory is used for screen level widgets.
  - **widgets**: It contains reusable UI components that are used across multiple screens.
- **controllers**: It holds classes that manage the state and business logic of the application.
- **providers**: It holds classes that manage the state and business logic of the application.
- **repositories**: This directory contains classes that abstract the data sources and provide a clean interface for accessing data.
  
Other important directories and files in the project include:

- **android**: This directory contains the Android-specific configuration and code.
- **ios**: This directory contains the iOS-specific configuration and code.
- **assets**: It is used to store static assets that are not part of the codebase, such as images, fonts, and configuration files.
- **pubspec.yaml**: This file is the specification file for the Flutter project's dependencies and assets.
- **README.md**: This file provides an overview of the project folder structure and any additional project-specific instructions.

## Getting Started

To get started with the project, follow these steps:

1. Clone the repository.
2. Install Flutter and Dart SDK on your machine if not already installed.
3. Open the project in your preferred IDE or text editor.
4. Run `flutter pub get` to fetch the project dependencies.
5. Launch the application on an emulator or a physical device using the appropriate Flutter command.

## Gitignore template
```bash
# Flutter/Dart specific files
.dart_tool/
.flutter-plugins
.flutter-plugins-dependencies
.packages
.pub/
build/
ios/Flutter/.last_build_id
ios/Flutter/App.framework/
ios/Flutter/Flutter.framework/
ios/Flutter/flutter_assets/
macos/Flutter/App.framework/
macos/Flutter/Flutter.framework/
macos/Flutter/flutter_assets/
web/flutter_service_worker.js
web/flutter_service_worker.js.map
web/index.html
web/main.dart.js
web/main.dart.js.map

# Android specific files
/android/
**/android/**/gradle-wrapper.jar
**/android/.gradle/
**/android/captures/
**/android/gradlew
**/android/gradlew.bat
**/android/local.properties
**/android/**/GeneratedPluginRegistrant.*

# iOS specific files
**/ios/.generated/
**/ios/Flutter/App.framework/
**/ios/Flutter/Flutter.framework/
**/ios/Flutter/flutter_assets/
**/ios/Flutter/Flutter.podspec
**/ios/Flutter/Generated.xcconfig
**/ios/Flutter/Generated.xcconfig.legacy
**/ios/Flutter/GeneratedPluginRegistrant.*

# IntelliJ related files
**/.idea/
**/*.iml
**/*.iws
**/*.ipr
.idea/

# Visual Studio Code related files
**/.vscode/
**/.history/

# Android Studio related files
**/.android/
**/.android/gradle.properties
**/.android/gradle/

# Gradle related files
**/gradle/
**/gradlew
**/gradlew.bat

# Flutter analysis and test results
**/build/
**/coverage/
.dart_tool/
.flutter-plugins
.flutter-plugins-dependencies
.flutter-plugins-master.lock
.flutter-plugins.pub-cache-checksum
.flutter-plugins-dependencies
.flutter-plugins-master.lock
.flutter-plugins.pub-cache-checksum
.flutter-plugins-dependencies
.flutter-plugins-master.lock
.flutter-plugins.pub-cache-checksum
.flutter-plugins-dependencies
.flutter-plugins-master.lock
.flutter-plugins.pub-cache-checksum

# Miscellaneous
**/.*.swp
**/*.log
```
