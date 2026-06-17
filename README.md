# AI Mechanic Assistant

A complete Android application for vehicle management and OBD-II fault scanning, built for the BIT4107 CAT submission.

## Features

- **Module 1: Authentication**: Login with hardcoded credentials (`admin@mechanic.com` / `password123`) and biometric authentication support.
- **Module 2: Dashboard**: Interactive overview of vehicle counts, repair stats, and recent additions.
- **Module 3: Vehicle Management**: Full CRUD operations using Room database. Manage vehicle details including make, model, year, and license plate.
- **Module 4: Fault Scanner**: Fetches OBD-II fault codes from a REST API with offline caching and pull-to-refresh functionality.
- **Module 5: Reports**: Timeline of all repair logs with sharing capabilities.
- **Technical**: MVVM Architecture, Jetpack Navigation, Room DB, Retrofit, ViewBinding, Coroutines, and Material Design 3.

## Setup Instructions

1. **Prerequisites**: Android Studio Ladybug or newer, JDK 17+.
2. **Build**: Sync Gradle files and build the project.
3. **Run**: Deploy to an Android emulator or physical device (Min SDK 24).
4. **Credentials**:
   - Email: `admin@mechanic.com`
   - Password: `password123`

## Architecture

- **UI Layer**: Fragments using ViewBinding and Navigation Component.
- **ViewModel Layer**: State management using LiveData/StateFlow.
- **Repository Layer**: Orchestrates data between local Room DB and remote API.
- **Data Layer**: Room for local persistence, Retrofit for networking.

## Troubleshooting

- If sync fails, ensure `gradle.properties` has `android.useAndroidX=true`.
- For biometric auth, ensure your device/emulator has a fingerprint registered.
