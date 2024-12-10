# app_name

## Starting the project

**install flutter packages**

    flutter clean
    flutter pub get
    flutter gen-l10n

**Generating files with build runner**

    flutter pub run build_runner build --delete-conflicting-outputs

**flavor run (Running by working environment Android - iOS)**

> For running the project on a physical device, emulator or simulator, connect the device to the computer or run the simulator and run the project for one of the environments.

    flutter run --flavor development --target lib/main_development.dart

    flutter run --flavor staging --target lib/main_staging.dart

    flutter run --flavor production --target lib/main_production.dart

**flavor build (Building by working environment Android - iOS)**

> Use when building apk, appbundle or ipa file
> you can add build name and/or build number to specify version while building 

    --build-name 3.4.60 --build-number 113

_android build apk_

    flutter build apk --flavor development --target lib/main_development.dart

    flutter build apk --flavor staging --target lib/main_staging.dart

    flutter build apk --flavor production --target lib/main_production.dart

_android build appbundle_

    flutter build appbundle --flavor development --target lib/main_development.dart

    flutter build appbundle --flavor staging --target lib/main_staging.dart

    flutter build appbundle --flavor production --target lib/main_production.dart

_ios build ipa_

    flutter build ipa --flavor development --target lib/main_development.dart

    flutter build ipa --flavor staging --target lib/main_staging.dart

    flutter build ipa --flavor production --target lib/main_production.dart

**Android release AppBundle**

> To ensure code security and reduce application size, the appbundle file to be uploaded to the store is obtained with the following command.

    flutter clean

    flutter pub get

    flutter gen-l10n

    flutter pub run build_runner build --delete-conflicting-outputs

    flutter build appbundle --obfuscate --split-debug-info=./app_name_mobile/build/outputs  --release  --flavor production --target lib/main_production.dart

    flutter build appbundle --obfuscate --split-debug-info=./app_name_mobile/build/outputs  --release  --flavor productionApi19 --target lib/main_production.dart

**iOS release ipa**

> To ensure code security and reduce application size, the appbundle file to be uploaded to the store is obtained with the following command.

    flutter clean

    flutter pub get

    flutter pub run build_runner build --delete-conflicting-outputs

    flutter build ipa --obfuscate --split-debug-info=./app_name_mobile/build/outputs  --release  --flavor production --target lib/main_production.dart

> to upload the ipa file to app store

    xcrun altool --upload-app --type ios -f build/ios/ipa/*.ipa --apiKey your_api_key --apiIssuer your_issuer_id

---

---

---

# Notes

**Detailed logging**

> You can use to get more detailed logs in terminal operations

    --verbose

**scrpit**

> To see the analysis of build files

    flutter build appbundle --analyze-size --flavor productionApi19 --target lib/main_production.dart
    flutter build appbundle --analyze-size --flavor productionApi19 --target lib/main_production.dart --target-platform android-x64 // android-arm, android-arm64, or android-x64

    flutter build ios --analyze-size --flavor production --target lib/main_production.dart
