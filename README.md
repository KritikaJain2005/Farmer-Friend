🌾 Farmer Friend

AI-powered Android application for farmers that combines crop disease detection, weather information, treatment recommendations, market information, labour assistance, and a farmer-friendly profile system in one mobile platform.

📱 Project Overview

Farmer Friend is an Android application designed to provide practical, technology-driven assistance to farmers.

The application uses Machine Learning, Generative AI, Firebase, REST APIs, and Android technologies to help users identify crop diseases and receive actionable information about possible treatments. It also brings useful farming services such as weather, market information, and labour hiring into a single application.

The project was developed as an end-to-end Android application with an emphasis on accessibility, modular features, and real-world agricultural use cases.

✨ Key Features

🔐 1. User Authentication

Firebase Authentication

User registration and login

Secure user session handling

Logout functionality

User-specific profile information

🏠 2. Home Dashboard

The home screen provides quick access to the major Farmer Friend services.

Weather information

Crop detection

Remedies

Market information

Labour hiring

Profile

🌦️ 3. Weather Information

Provides weather-related information to help farmers make better day-to-day decisions.

Possible use cases include:

Checking current weather conditions

Planning irrigation

Planning agricultural activities

Understanding upcoming weather conditions

🌱 4. AI-Based Crop Disease Detection

One of the core features of Farmer Friend is crop disease detection.

The application supports:

Image → AI Analysis → Disease Information → Recommended Remedies

Detection pipeline

Crop Image
    ↓
Android Application
    ↓
Image Processing
    ↓
On-device TFLite Model
    ↓
AI/Backend Analysis
    ↓
Disease Identification
    ↓
Treatment & Remedy Information

The project uses TensorFlow Lite (TFLite) for on-device machine-learning inference and also integrates a backend AI pipeline for more detailed analysis.

🤖 5. AI-Powered Detailed Crop Analysis

For detailed crop analysis, the Android application communicates with a backend service.

Backend technology includes:

Python

Flask

AI/LLM integration

Gemini API

Important API endpoints include:

/analyzeCrop
/analyzeWithDetails

The detailed analysis can provide information such as:

Detected crop/disease

Disease explanation

Possible causes

Recommended actions

Treatment suggestions

Preventive information

💊 6. Remedy System

Farmer Friend provides different types of treatment/remedy information.

The remedy system is organized into categories such as:

🧪 Chemical remedies

🌿 Ayurvedic remedies

🌱 Organic remedies

🦠 Biological remedies

This gives farmers multiple approaches instead of presenting only a single treatment option.

Note: Treatment information in the application should be used as informational guidance. Farmers should verify chemical usage, dosage, crop suitability, and local agricultural recommendations with qualified agricultural professionals or product labels.

📈 7. Market Module

The Market module is designed to help farmers access market-related information.

The navigation structure includes:

State
  ↓
City
  ↓
Market
  ↓
Market Information

This module can be extended with live market-price APIs and additional agricultural commodity information.

👷 8. Labour Hiring Module

The Labour module connects farmers with agricultural labour requirements.

It is designed around the idea of:

Farmer
   ↓
Labour Requirement
   ↓
Labour Information
   ↓
Hiring / Contact

This feature can be expanded with location-based matching, availability, ratings, and booking functionality.

👤 9. Profile

The profile section provides a central place for user information and account actions.

Features include:

User information

Firebase account information

Profile management

Logout

🏗️ System Architecture

                    ┌─────────────────────┐
                    │     Android App     │
                    │   Kotlin / Java     │
                    └──────────┬──────────┘
                               │
             ┌─────────────────┼─────────────────┐
             │                 │                 │
             ▼                 ▼                 ▼
       Firebase Auth      TFLite Model      REST APIs
             │                 │                 │
             │                 │                 ▼
             │                 │          ┌──────────────┐
             │                 │          │ Flask Backend│
             │                 │          └──────┬───────┘
             │                 │                 │
             │                 │                 ▼
             │                 │          ┌──────────────┐
             │                 │          │ Gemini / AI  │
             │                 │          └──────────────┘
             │                 │
             └─────────────────┴─────────────────┐
                                                 │
                                                 ▼
                                      Agricultural Information

🛠️ Technology Stack

Android

Kotlin

Java

Android Studio

Android XML layouts

Activities

Adapters

Retrofit

AI / Machine Learning

TensorFlow Lite

Gemini API

Generative AI

Image-based crop analysis

Backend

Python

Flask

REST APIs

Authentication & Cloud

Firebase Authentication

Firebase services

Networking

Retrofit

REST API communication

JSON-based responses

📂 Project Structure

A simplified structure of the Android project:

Farmer-Friend/
│
├── app/
│   └── src/
│       └── main/
│           ├── java/
│           │   └── com/
│           │       └── example/
│           │           └── farmingfriend/
│           │               ├── ApiService
│           │               ├── CropResponse
│           │               ├── CustomSpinnerAdapter
│           │               ├── Home
│           │               ├── LoginActivity
│           │               ├── MainActivity
│           │               ├── Market
│           │               ├── Profile
│           │               └── ...
│           │
│           ├── res/
│           │   ├── layout/
│           │   ├── drawable/
│           │   ├── mipmap/
│           │   └── values/
│           │
│           └── AndroidManifest.xml
│
├── gradle/
├── build.gradle
├── settings.gradle
└── README.md

🔄 Crop Detection Workflow

1. User opens Crop Detection
            ↓
2. User selects/captures crop image
            ↓
3. Image is processed
            ↓
4. TFLite model performs local analysis
            ↓
5. Backend can perform detailed AI analysis
            ↓
6. Result is returned to Android app
            ↓
7. Disease information is displayed
            ↓
8. User can view suitable remedy information

🔌 API Communication

The Android application uses Retrofit for communication with the backend.

Example API operations include:

POST /analyzeCrop
POST /analyzeWithDetails

The backend receives the crop image/data, processes the request, performs AI analysis where required, and returns structured information to the Android application.

🎯 Project Objectives

The main objectives of Farmer Friend are:

Make agricultural technology more accessible

Assist farmers in identifying crop diseases

Provide understandable disease information

Provide multiple remedy categories

Bring farming-related services into one application

Reduce the complexity of accessing agricultural information

Build a foundation for future AI-powered agricultural services

🚀 Future Enhancements

The project can be extended with:

📊 Live agricultural market prices

🌤️ More detailed weather forecasting

🗺️ Location-based services

👨‍🌾 Farmer-to-expert communication

👷 Location-based labour matching

⭐ Labour ratings and reviews

🌾 More crop and disease classes

📱 Offline-first crop detection

🌐 Multi-language support

🗣️ Voice-based agricultural assistant

📈 Crop price prediction

🧠 More advanced AI-based crop diagnosis

🔔 Weather and crop-disease alerts

🎥 Project Demo

A project demonstration video can be added here:

▶️ Watch Farmer Friend Demo

The demo can showcase:

User registration/login

Home dashboard

Weather

Crop image selection

AI crop disease detection

Detailed analysis

Remedy recommendations

Market module

Labour module

Profile and logout

📸 Screenshots

Add application screenshots here to demonstrate the UI.

Example:

screenshots/
├── login.png
├── home.png
├── crop-detection.png
├── disease-result.png
├── remedies.png
├── market.png
├── labour.png
└── profile.png

Then they can be displayed in the README using:

![Home Screen](screenshots/home.png)
![Crop Detection](screenshots/crop-detection.png)
![Disease Result](screenshots/disease-result.png)

🔒 Security Note

Do not commit private credentials, API keys, Firebase configuration files, passwords, or other secrets to a public repository.

Recommended files to keep out of Git:

google-services.json
local.properties
.env
API keys
private credentials

Use environment variables or secure configuration mechanisms for sensitive information.

👨‍💻 Project

Project: Farmer FriendPlatform: AndroidDomain: Agriculture + Artificial IntelligencePrimary Technologies: Kotlin, Java, TensorFlow Lite, Firebase, Flask, Gemini API, Retrofit

⭐ Contributing

Contributions and suggestions are welcome.

If you would like to improve Farmer Friend:

Fork the repository

Create a feature branch

Make your changes

Commit your changes

Create a Pull Request
