# MVVM Clean Architecture Study Project

This is a study project that implements the MVVM (Model-View-ViewModel) architecture with Clean Architecture principles. The project serves as a learning tool to explore unit testing using JUnit and mocking with the Truth library, along with dependency injection using Hilt.

## Features

- **MVVM Architecture**: Separation of concerns by dividing the project into Model, View, and ViewModel layers.
- **Clean Architecture**: Ensures scalability and maintainability by organizing the code into distinct layers.
- **Unit Testing**: Implementation of unit tests using JUnit, Mockito, and Truth to ensure reliability.
- **Dependency Injection**: Managed dependencies with Hilt for better modularization and testability.

## Project Structure

The project is organized into the following main packages:

- `repository`: Contains the repository classes responsible for data handling.
- `usecase`: Includes the use cases which encapsulate the business logic.
- `viewmodel`: Contains the ViewModel classes that manage UI-related data.
- `view`: Holds the UI components like activities and fragments.

## Dependencies

This project uses the following libraries:

- **MVVM & Clean Architecture**:
  - [ViewModel](https://developer.android.com/topic/libraries/architecture/viewmodel): For managing UI-related data efficiently.
  - [LiveData](https://developer.android.com/topic/libraries/architecture/livedata): For observing data changes and automatically updating the UI.
  - [Fragment KTX](https://developer.android.com/kotlin/ktx): For enhanced fragment management.

- **Dependency Injection**:
  - [Hilt](https://dagger.dev/hilt/): For dependency injection, simplifying the use of Dagger in Android.

- **Networking**:
  - [Retrofit](https://square.github.io/retrofit/): For making HTTP requests.
  - [Gson Converter](https://github.com/square/retrofit/tree/master/retrofit-converters/gson): For converting JSON to Kotlin objects.

- **Unit Testing**:
  - [JUnit](https://junit.org/junit5/): For writing unit tests.
  - [Mockito](https://site.mockito.org/): For mocking dependencies in unit tests.
  - [Truth](https://truth.dev/): For making assertions in tests.
  - [Coroutines Test](https://github.com/Kotlin/kotlinx.coroutines/tree/master/kotlinx-coroutines-test): For testing Kotlin coroutines.
  - [Core Testing](https://developer.android.com/jetpack/androidx/releases/arch-core): For testing LiveData and ViewModel.

### Dependency Versions

```kotlin
val lifecycle_version = "2.8.4"

// Retrofit
implementation("com.squareup.retrofit2:retrofit:2.11.0")
implementation("com.squareup.retrofit2:converter-gson:2.11.0")
// ViewModel
implementation("androidx.lifecycle:lifecycle-viewmodel-ktx:$lifecycle_version")
// LiveData
implementation("androidx.lifecycle:lifecycle-livedata-ktx:$lifecycle_version")
// Loading ViewModel
implementation("androidx.fragment:fragment-ktx:1.8.2")
// Hilt Dagger
implementation("com.google.dagger:hilt-android:2.48.1")
// KSP
ksp("com.google.dagger:hilt-android-compiler:2.48.1")
// Truth
testImplementation("com.google.truth:truth:1.4.4")
// Coroutines Test
testImplementation("org.jetbrains.kotlinx:kotlinx-coroutines-test:1.9.0-RC.2")
// Mockito
testImplementation("org.mockito:mockito-core:5.7.0")
// Core Testing
testImplementation("androidx.arch.core:core-testing:2.2.0")
