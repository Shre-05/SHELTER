# SHELTER (Safe Haven for Every Lady’s Threat Emergency Response)

## Overview

**SHELTER** is a women’s safety app designed to send emergency notifications to pre-designated contacts when a woman feels threatened or in danger. The app allows the user to trigger an alert using voice input, a quick button, or a custom message. Once the alert is triggered, the app will notify the emergency contacts with the user's location and any message or voice note recorded by the user.

## Key Features

- **Emergency Alerts**: Send quick alerts via a voice command or button press.
- **Voice and Text Input**: Users can send either a voice message or text message when in danger.
- **Location Sharing**: Automatically shares the user's real-time location with emergency contacts.
- **Notification System**: Instantly notify pre-configured contacts when an alert is triggered.
- **Quick Access Button**: A simple UI allowing fast and easy alert activation.
  
## Technologies Used

- **Android Studio**: Main development platform.
- **Java/Kotlin**: Primary programming language for Android.
- **Firebase**: For real-time database and notifications (optional, for notification features).
- **Google Maps API**: For location sharing.
- **Speech Recognition API**: For voice-based input and commands.
  
## Project Structure

- **MainActivity.java/Kotlin**: Handles the core logic of alert triggering and input handling.
- **LocationService.java**: Collects and sends real-time location data to the designated contacts.
- **AlertNotificationService.java**: Sends notifications through SMS or other channels.
- **UI Layout (XML files)**: User interface for the app, including the main dashboard and alert options.
  
## Setup Instructions

### Prerequisites

- Android Studio installed on your machine.
- Knowledge of Android development, Java/Kotlin, and XML.
- Basic understanding of Google Maps API for location sharing and Firebase for notifications (optional).

### Steps

1. **Clone the repository**:
   ```bash
   git clone https://github.com/Shre-05/SHELTER.git
   ```

2. **Open the project in Android Studio**:
   - Open Android Studio.
   - Choose **Open an existing Android Studio project**.
   - Navigate to the folder where you cloned the project and open it.

3. **Configure Google Maps API**:
   - Get an API key from [Google Cloud](https://console.cloud.google.com/) for Maps services.
   - Add the API key to your `AndroidManifest.xml` under:
     ```xml
     <meta-data
         android:name="com.google.android.geo.API_KEY"
         android:value="YOUR_API_KEY" />
     ```

4. **Configure Firebase (Optional)**:
   - Set up Firebase for sending push notifications.
   - Add the `google-services.json` file to your app project and configure Firebase services.

5. **Build and run the app**:
   - Connect your Android device or use an emulator.
   - Click the **Run** button in Android Studio to build and deploy the app.

## Usage

1. **Initial Setup**:
   - Add emergency contacts who will receive the alerts.
   - Enable location access for real-time tracking.
   
2. **Triggering Alerts**:
   - Users can press the **Quick Alert Button** on the main screen to send a notification instantly.
   - Alternatively, the user can use **Voice Input** to trigger an alert by saying a predefined command (e.g., "Help" or "Emergency").
   
3. **Notification**:
   - Once an alert is triggered, the app will automatically send the user's location along with a custom message or recorded voice note to the emergency contacts.
   
4. **Location Sharing**:
   - The user's real-time location is sent with the alert, enabling emergency contacts to track the person in need.

## Future Enhancements

- **Panic Mode**: Automatically trigger alerts when the phone is shaken rapidly or when a specific gesture is recognized.
- **Fake Call Feature**: Simulate a call to provide an excuse or deterrent in threatening situations.
- **Voice Recording**: Automatically record audio after the alert is triggered and save it securely for later use.
