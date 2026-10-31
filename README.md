# POTHOLE_ADAS
### AI-Powered Pothole Detection and Route-Aware Driver Assistance System

**POTHOLE_ADAS** is an AI-powered road-safety and driver-assistance application designed to detect potholes using computer vision and provide useful information to drivers during their journeys.

The project combines **Artificial Intelligence, Computer Vision, GPS-based location tracking, digital mapping, route generation, and driver-alert mechanisms** into a connected application.

Using a camera or road-video input, the system processes road images through a **YOLOv8-based pothole detection model** to identify potholes and generate detection results. These results can be associated with geographical location information and processed by the backend to support road-hazard awareness.

The application is developed with a **Flutter-based Android frontend** and a **Python backend**. The frontend provides the user interface for journey input, navigation information, detection results, and alerts, while the backend manages the core processing modules and communication between different services.

The project also incorporates **Firebase** for cloud-based data storage and uses the **Google Maps Platform** as its intended mapping and routing solution, including location geocoding and route generation.

Our goal is to bring road-hazard detection and navigation-related information together in one application, helping drivers become more aware of road conditions and make safer travel decisions.

**Core Concept:**

`SEE → UNDERSTAND → ASSESS → ALERT`

POTHOLE_ADAS aims to establish a foundation for intelligent road-hazard awareness by connecting AI-based perception, geographical information, backend processing, and driver assistance in a single system.


## 2. Motivation and Problem Statement

### 2.1 Problem Statement

Potholes are among the most common road-safety problems. They can appear unexpectedly on roads and create risks for both drivers and vehicles.

Some of the major problems caused by potholes include:

- **Vehicle Damage:** Potholes can damage tyres, wheels, suspension systems, and other vehicle components.
- **Sudden Braking and Steering:** Drivers may have to react suddenly to avoid potholes, potentially creating dangerous situations.
- **Loss of Vehicle Control:** Unexpected road defects can affect vehicle stability and handling.
- **Road Accidents:** Potholes can increase the possibility of accidents, particularly at higher speeds or in poor visibility.
- **Difficult Manual Monitoring:** Identifying and monitoring road conditions across large areas through manual inspection is time-consuming and difficult to scale.

Traditional pothole identification generally depends on manual road inspections or reports from road users. These methods may not always provide timely information about changing road conditions.

Therefore, an automated and intelligent approach is needed to identify potholes and provide useful information to drivers.

### 2.2 Motivation

The primary motivation behind POTHOLE_ADAS is to develop an AI-based pothole detection and driver-assistance system that can automatically identify road hazards from camera or video input.

Instead of depending entirely on drivers to notice potholes while driving, our system uses computer vision and artificial intelligence to analyse road information and detect potential potholes.

By combining visual detection with geographical location information and driver alerts, the project aims to make road-hazard awareness more accessible and useful during journeys.

The key motivations are:

- To reduce dependence on manual pothole identification.
- To use AI and computer vision for automated road-hazard detection.
- To associate detected potholes with their geographical locations.
- To provide drivers with timely and relevant hazard information.
- To connect road-hazard detection with navigation and driver-assistance functionality.
- To establish a foundation for a more intelligent and connected road-safety system.

### 2.3 Our Vision

Our vision is to develop a smart road-safety assistant that can perceive road conditions, understand detected hazards, assess their relevance, and provide useful information to drivers.

The fundamental concept of our system is:

**SEE → UNDERSTAND → ASSESS → ALERT**

Each stage represents an important part of the system:

1. **SEE:** Receive road information through a camera, live video, recorded road video, or image input.
2. **UNDERSTAND:** Analyse the visual input using the AI-based computer-vision model to identify whether a pothole is present.
3. **ASSESS:** Consider detection confidence, pothole position, possible severity or risk, and distance or proximity.
4. **ALERT:** Deliver the processed result to the frontend so that the driver can view relevant hazard information and warnings.

Through this approach, POTHOLE_ADAS aims to connect automated road perception with practical driver assistance.


## 3. Project Objectives and Key Features

### 3.1 Project Objectives

The primary objective of POTHOLE_ADAS is to develop an intelligent road-hazard detection and driver-assistance application that combines artificial intelligence, geographical information, and navigation-related services.

The major objectives are:

1. **Automated Pothole Detection:** Develop an AI-based system using the YOLOv8 object detection model to identify potholes from road images and video input.

2. **Road-Hazard Awareness:** Obtain useful information about detected potholes, including their location, detection confidence, and other relevant characteristics.

3. **GPS-Based Location Tracking:** Associate vehicle position and detected road hazards with geographical coordinates.

4. **Route Generation:** Provide navigation support by generating routes between a selected source and destination using mapping and routing services.

5. **Driver Assistance:** Present relevant hazard information through visual and voice-based alerts to improve driver awareness.

6. **Cloud-Based Data Storage:** Store detection information and associated geographical data using Firebase for future retrieval and application functionality.

7. **Modular System Integration:** Connect the frontend, backend, detection model, GPS, routing, database, and alert modules into a unified application.

### 3.2 Key Features

#### 1. AI-Based Pothole Detection

- Uses the YOLOv8 object detection model.
- Processes road images and video frames.
- Identifies potholes through computer vision.
- Provides detection information, including bounding boxes and confidence values.

#### 2. GPS and Location Tracking

- Retrieves the current geographical position of the vehicle.
- Uses latitude and longitude coordinates.
- Connects location information with the backend.
- Supports geographical association of detected hazards.

#### 3. Map-Based Navigation and Routing

- Supports source and destination-based journey planning.
- Uses the Google Maps Platform as the intended mapping and routing solution.
- Uses the Geocoding API to convert location names into geographical coordinates.
- Uses the Routes API to generate driving routes.
- Provides a foundation for incorporating road-hazard information into route selection.

#### 4. Driver Assistance and Alerts

- Presents relevant pothole detection information to the user.
- Supports visual hazard notifications.
- Includes voice-based alert functionality.
- Aims to improve driver awareness of potentially hazardous road conditions.

#### 5. Firebase Integration

- Supports cloud-based storage of detection information.
- Stores relevant hazard-related data.
- Provides a data layer that can be accessed by connected backend services.

#### 6. Flutter-Based User Interface

- Provides an Android application developed using Flutter and Dart.
- Allows users to interact with the navigation and detection system.
- Displays relevant journey, location, and hazard information.
- Communicates with the Python backend through API requests.

#### 7. Modular Python Backend

- Organises the system into separate functional modules.
- Handles communication between the frontend and backend services.
- Integrates detection, GPS, routing, database, and alert functionality.
- Makes individual components easier to maintain, test, and extend.

### 3.3 Current Development Scope

POTHOLE_ADAS is being developed incrementally. The current project focuses primarily on establishing the pothole detection pipeline and connecting the major application components.

The YOLOv8-based pothole detection model, Flutter frontend, Python backend structure, GPS-related modules, Firebase integration, and voice-alert functionality form the foundation of the project.

Mapping and routing integration, along with deeper hazard-aware route optimisation, are being developed as part of the navigation component.

The project is structured so that these components can progressively work together as one road-safety and driver-assistance application.


## 4. System Architecture and Overall Design

### 4.1 Architecture Overview

POTHOLE_ADAS follows a modular client-server architecture in which the Flutter frontend communicates with a Python backend to access the system's core functionalities.

The architecture is divided into the following major layers:

1. **Frontend Layer:** Provides the Android application interface through which users interact with the system.
2. **Backend Layer:** Handles API requests, coordinates different services, and manages communication between application components.
3. **AI and Detection Layer:** Processes road images and video frames using the YOLOv8-based pothole detection model.
4. **Location and Navigation Layer:** Handles GPS information, geographical coordinates, location conversion, and route generation.
5. **Database Layer:** Uses Firebase for storing and retrieving relevant detection information.
6. **Driver Assistance Layer:** Processes relevant hazard information and provides visual or voice-based alerts.

Each layer has a specific responsibility, allowing the system to operate as a collection of connected modules rather than a single large application.

### 4.2 High-Level System Architecture

The overall architecture can be represented as follows:

```text
              ┌──────────────────────────┐
              │      USER / DRIVER       │
              └────────────┬─────────────┘
                           │
                           ▼
              ┌──────────────────────────┐
              │     FLUTTER FRONTEND     │
              │                          │
              │  • User Interface        │
              │  • Journey Input         │
              │  • Navigation Display    │
              │  • Detection Results     │
              │  • Alerts                │
              └────────────┬─────────────┘
                           │
                       API Requests
                       JSON Response
                           │
                           ▼
              ┌──────────────────────────┐
              │     PYTHON BACKEND       │
              │                          │
              │  • API Server            │
              │  • Request Processing    │
              │  • Module Coordination   │
              │  • Response Handling     │
              └────────────┬─────────────┘
                           │
          ┌────────────────┼─────────────────┐
          │                │                 │
          ▼                ▼                 ▼
   ┌─────────────┐  ┌─────────────┐  ┌────────────────┐
   │ AI DETECTION│  │ GPS MODULE  │  │ ROUTE MODULE   │
   │             │  │             │  │                │
   │ YOLOv8      │  │ Position    │  │ Geocoding API  │
   │ Camera      │  │ Coordinates │  │ Routes API     │
   └──────┬──────┘  └──────┬──────┘  └───────┬────────┘
          │                │                 │
          └────────────────┼─────────────────┘
                           │
                           ▼
              ┌──────────────────────────┐
              │     FIREBASE DATABASE    │
              │                          │
              │  • Detection Records      │
              │  • Location Information   │
              │  • Related Hazard Data    │
              └──────────────────────────┘
                           │
                           ▼
              ┌──────────────────────────┐
              │   DRIVER ASSISTANCE       │
              │                          │
              │  • Hazard Information    │
              │  • Visual Notifications  │
              │  • Voice Alerts          │
              └──────────────────────────┘
```

### 4.3 Frontend Architecture

The frontend is developed using Flutter and Dart.

It acts as the main interaction layer between the user and the application. It provides the interface for entering journey information, accessing navigation features, viewing detection results, and receiving relevant alerts.

The frontend communicates with the Python backend through API requests and displays the processed responses.

### 4.4 Backend Architecture

The backend is developed using Python and is responsible for coordinating the application's main processing modules.

The backend contains separate functional components for:

- **Detection:** Processes image and video input through the YOLOv8 model.
- **Camera:** Handles camera-related input and image acquisition.
- **GPS:** Retrieves and processes geographical location information.
- **Route:** Handles source and destination processing and route generation.
- **ADAS:** Supports driver-assistance and decision-related functionality.
- **Alerts:** Handles hazard-related notification and voice-alert functionality.
- **Firebase Integration:** Connects application services with cloud-based data storage.
- **GPS Bridge:** Provides communication with the GPS data source.

The modular backend structure makes it easier to maintain individual services and integrate additional functionality without redesigning the complete application.

### 4.5 External Services and Integrations

POTHOLE_ADAS connects with external services to support its navigation and data-management requirements.

**Google Maps Platform**

The project uses the Google Maps Platform as its intended mapping and routing solution.

Its relevant services include:

- **Geocoding API:** Converts textual location information into geographical coordinates.
- **Routes API:** Generates driving routes between source and destination locations.
- **Google Maps SDK for Flutter:** Supports map display and navigation-related visualisation in the mobile application.

**Firebase**

Firebase provides cloud-based data storage for relevant application information, including pothole detection records and associated geographical information.

**GPS Data Source**

The GPS bridge and GPS processing modules provide geographical coordinates that can be used by the backend and other application components.

### 4.6 Communication Between Components

The major communication flow follows a request-processing-response model.

1. The user interacts with the Flutter application.
2. The frontend sends the required information to the Python backend through an API request.
3. The backend identifies the relevant operation and communicates with the appropriate module.
4. The selected module performs the required processing, such as pothole detection, GPS handling, or route generation.
5. Relevant information is stored in or retrieved from Firebase when required.
6. The backend prepares a structured response, generally in JSON format.
7. The Flutter application receives the response and presents the information to the user.

This architecture establishes a connection between road perception, geographical information, navigation services, cloud storage, and driver assistance.

### 4.7 Architectural Design Principles

The system follows several important design principles:

- **Modularity:** Each major functionality is maintained in a separate module.
- **Separation of Responsibilities:** The frontend focuses on user interaction, while the backend manages processing and service integration.
- **Scalability:** Individual modules can be extended as the application develops.
- **Maintainability:** Separate components make debugging and modification easier.
- **Integration:** Different technologies and services communicate through defined interfaces.
- **Data Reusability:** Geographical and detection information can be stored and retrieved for relevant application operations.

Overall, this architecture provides the foundation for integrating AI-based pothole detection with GPS, digital mapping, route generation, and driver-assistance functionality in one connected application.


## 5. Complete Working Workflow and End-to-End Data Flow

### 5.1 Workflow Overview

POTHOLE_ADAS follows an interconnected workflow in which the frontend, backend, AI detection module, GPS services, routing services, and Firebase work together to provide road-hazard information and driver assistance.

The complete workflow can be divided into two major processes:

1. **Navigation Workflow:** Handles journey input, location processing, and route generation.
2. **Road-Hazard Detection Workflow:** Handles camera input, pothole detection, geographical association, data storage, and driver alerts.

Both processes are coordinated through the Python backend.

### 5.2 Navigation Workflow

The navigation process begins when the user enters a source and destination in the Flutter application.

The following steps describe the process:

**Step 1 – Journey Input**

The user enters the starting location and destination through the application interface.

**Step 2 – Frontend Request**

The Flutter application sends the source and destination information to the Python backend through an API request.

**Step 3 – Geocoding**

The backend uses the Google Geocoding API to convert textual location information into geographical coordinates, consisting of latitude and longitude.

**Step 4 – Route Generation**

The backend communicates with the Google Routes API to generate a driving route between the selected locations.

**Step 5 – Route Response**

The generated route information is returned to the backend, which prepares a structured response for the frontend.

**Step 6 – Navigation Display**

The Flutter application receives the route information and displays the relevant navigation details through its map interface.

### 5.3 Road-Hazard Detection Workflow

The detection process focuses on identifying potholes from road images or video input.

**Step 1 – Camera Input**

The camera module receives road images or video frames for processing.

**Step 2 – Image Processing**

The incoming image is prepared for the detection model. This may include resizing and other preprocessing operations required by the model.

**Step 3 – YOLOv8 Detection**

The processed image is passed to the YOLOv8-based object detection model.

The model analyses the image and identifies potential potholes, producing detection information such as:

- Detected object or hazard class.
- Bounding-box coordinates.
- Detection confidence.

**Step 4 – GPS Association**

The GPS module provides the current geographical position of the vehicle.

The available location information can be associated with the corresponding detection record.

**Step 5 – Backend Processing**

The detection results and associated location information are handled by the Python backend.

**Step 6 – Firebase Storage**

Relevant detection records can be stored in Firebase along with associated information such as geographical coordinates, image references, severity, and timestamps.

**Step 7 – Driver Notification**

The backend and alert modules prepare relevant detection information for presentation to the user.

**Step 8 – Frontend Display**

The Flutter application displays the available detection results and relevant driver alerts.

### 5.4 Frontend–Backend Communication

Communication between the Flutter frontend and Python backend follows an API-based request-response structure.

The frontend sends requests containing the required information, while the backend processes them and returns structured responses, generally in JSON format.

The documented API operations include:

| API Endpoint | Purpose |
|---|---|
| `/api/detect` | Receives image input and returns pothole detection results. |
| `/api/route` | Processes source and destination information and returns route information. |
| `/api/geocode` | Converts textual locations into geographical coordinates. |
| `/api/location` | Receives GPS location information. |
| `/api/history` | Retrieves previously stored detection records. |

These endpoints provide a communication interface between the application and its backend services.

### 5.5 Complete System Flow

The overall data flow can be summarised as follows:

```text
                  USER OPENS APPLICATION
                           |
                           v
                  FLUTTER FRONTEND
                           |
              +------------+------------+
              |                         |
              v                         v
       NAVIGATION INPUT            CAMERA INPUT
       Source/Destination          Road Images/Video
              |                         |
              v                         v
        PYTHON BACKEND             PYTHON BACKEND
              |                         |
              v                         v
        GEOCODING API               IMAGE PROCESSING
              |                         |
              v                         v
         GOOGLE ROUTES               YOLOv8 MODEL
              API                       |
              |                         v
              v                   POTHOLE DETECTION
        ROUTE RESPONSE                  |
              |                         v
              |                    GPS ASSOCIATION
              |                         |
              |                         v
              |                    FIREBASE
              |                         |
              +------------+------------+
                           |
                           v
                   BACKEND RESPONSE
                           |
                           v
                   FLUTTER FRONTEND
                           |
                           v
             ROUTE / DETECTION / ALERTS
                           |
                           v
                    USER / DRIVER
```

### 5.6 Data Management and Response Handling

Firebase acts as the cloud-based storage layer for relevant detection information.

A detection record may contain:

- Hazard type.
- Geographical latitude and longitude.
- Detection confidence.
- Severity information, where available.
- Image or image reference.
- Detection timestamp.

The backend manages the relevant storage and retrieval operations.

When the frontend requests information, the backend prepares the appropriate response so that the application can display the available results.

### 5.7 Overall Workflow Summary

The complete concept of POTHOLE_ADAS can be expressed through the following sequence:

**USER INPUT → FRONTEND REQUEST → BACKEND PROCESSING → AI DETECTION / GPS / ROUTING → FIREBASE INTEGRATION → RESPONSE GENERATION → FRONTEND DISPLAY → DRIVER ASSISTANCE**

By connecting these processes, POTHOLE_ADAS establishes a unified workflow that combines navigation-related services with AI-based pothole detection and geographical road-hazard information.


## 6. Technology Stack and Tools Used

POTHOLE_ADAS combines mobile application development, artificial intelligence, backend programming, geographical services, and cloud-based data management.

The following technologies form the foundation of the project.

### 6.1 Programming Languages

| Technology | Purpose |
|---|---|
| Python | Backend development, AI processing, GPS handling, routing integration, and application logic. |
| Dart | Flutter frontend development and mobile application functionality. |

### 6.2 Frontend Technologies

| Technology | Purpose |
|---|---|
| Flutter | Cross-platform application development and user interface. |
| Dart | Programming language used for Flutter application development. |
| Android SDK | Android application development and execution environment. |
| Google Maps SDK for Flutter | Map display, geographical visualisation, and navigation-related interface integration. |

### 6.3 Backend Technologies

| Technology | Purpose |
|---|---|
| Python | Main backend programming language. |
| Flask | Lightweight web framework used to develop the backend API server. |
| REST API | Communication between the Flutter frontend and Python backend. |
| JSON | Structured data exchange between application components. |
| Requests | HTTP communication with external services and APIs. |
| Python-dotenv | Loading configuration values and environment variables from the `.env` file. |

### 6.4 Artificial Intelligence and Computer Vision

| Technology | Purpose |
|---|---|
| YOLOv8 | Object detection model used for pothole identification. |
| OpenCV | Image and video processing support. |
| PyTorch | Deep learning framework supporting model development and inference. |
| Ultralytics | YOLO model framework and associated tools. |

The detection pipeline uses computer vision to analyse road images and identify potholes through object detection.

### 6.5 Mapping, Geocoding and Routing Services

POTHOLE_ADAS uses the Google Maps Platform as its mapping and routing technology.

| API / Service | Purpose |
|---|---|
| Google Maps SDK for Flutter | Displays maps and geographical information in the mobile application. |
| Google Geocoding API | Converts textual addresses and place names into geographical coordinates. |
| Google Routes API | Generates driving routes between selected source and destination locations. |
| Google Roads API | Provides road-related geographical services for applicable road-mapping functionality. |

These services provide the geographical and routing foundation for connecting navigation with road-hazard information.

### 6.6 GPS and Location Technologies

| Component | Purpose |
|---|---|
| GPS | Provides the geographical position of the vehicle. |
| GPS Bridge | Receives and exposes GPS information for the backend. |
| NMEA Data | Standard GPS data format used by compatible GPS receivers. |
| Latitude and Longitude | Represent geographical positions and associate detections with locations. |

The GPS module allows the system to connect detected road hazards with geographical information.

### 6.7 Database and Cloud Technologies

| Technology | Purpose |
|---|---|
| Firebase | Cloud-based backend services and data management. |
| Cloud Firestore | Document-based database for storing and retrieving relevant application and detection information. |
| Firebase Admin SDK | Backend-side Firebase integration and database operations. |

Firebase provides a centralised data layer for managing pothole detection records and associated geographical information.

### 6.8 Driver Assistance and Alert Technologies

| Technology | Purpose |
|---|---|
| Python-based ADAS Module | Handles driver-assistance-related processing and decision logic. |
| Voice Alert Module | Provides audio-based hazard notifications. |
| Flutter Text-to-Speech | Supports spoken notifications through the mobile application. |

These components help communicate relevant hazard information to the driver through visual and audio feedback.

### 6.9 Development Tools and Environment

| Tool | Purpose |
|---|---|
| Android Studio | Flutter application development, Android configuration, and emulator testing. |
| PyCharm / Python IDE | Python backend development and debugging. |
| Git | Source-code version control. |
| GitHub | Collaborative development, code hosting, and project documentation. |
| Android Emulator | Testing the Flutter application in a virtual Android environment. |
| Visual Studio Code (optional) | Code editing and project inspection. |

### 6.10 Technology Stack Summary

The major technology choices can be summarised as follows:

- **Frontend:** Flutter and Dart.
- **Backend:** Python and Flask.
- **AI Model:** YOLOv8.
- **Computer Vision:** OpenCV.
- **Deep Learning:** PyTorch.
- **Database:** Firebase Cloud Firestore.
- **Maps:** Google Maps Platform.
- **Geocoding:** Google Geocoding API.
- **Routing:** Google Routes API.
- **Location:** GPS and GPS Bridge.
- **Communication:** REST API and JSON.
- **Development:** Android Studio, Python IDE, Git and GitHub.

Together, these technologies provide the foundation for an integrated application combining AI-based pothole detection, geographical location tracking, navigation services, cloud storage, and driver assistance.


## 7. Project Directory Structure

### 7.1 Repository Overview

POTHOLE_ADAS is organised into two major development areas:

- **Frontend:** Contains the Flutter-based Android application.
- **Backend:** Contains the Python API server, GPS bridge, and individual processing modules.

The project follows a modular structure to keep the mobile application and backend processing components organised separately.

### 7.2 Main Project Structure

The following tree represents the main folders and files visible in the current project:

```text
pothole_adas_frontend/
│
├── android/
│   └── Android application configuration
│
├── backend/
│   │
│   ├── .venv/
│   ├── .venv_linux/
│   ├── output/
│   ├── uploads/
│   │
│   ├── api_server.py
│   ├── gps_bridge.py
│   │
│   └── Pothole_ADAS/
│       │
│       ├── .idea/
│       ├── .venv/
│       ├── __pycache__/
│       │
│       ├── Pothole_ADAS/
│       │   ├── adas/
│       │   ├── alerts/
│       │   ├── backend/
│       │   ├── camera/
│       │   ├── detection/
│       │   ├── gps/
│       │   ├── gui/
│       │   ├── mobile_app/
│       │   ├── output/
│       │   ├── radar/
│       │   ├── route/
│       │   └── test_images/
│       │
│       └── .gitignore
│
├── lib/
│   ├── config/
│   ├── models/
│   ├── screens/
│   ├── services/
│   ├── widgets/
│   ├── gps_service.dart
│   └── main.dart
│
├── .dart_tool/
├── .idea/
├── .venv/
├── build/
│
├── pubspec.yaml
├── pubspec.lock
├── analysis_options.yaml
├── .gitignore
└── README.md
```

*Note: Virtual environments, generated folders, and IDE configuration directories are shown for orientation but are generally excluded from source-code documentation and version control.*

### 7.3 Frontend Directory

The Flutter frontend is located in the `lib/` directory.

Its main organisation is:

| Directory / File | Responsibility |
|---|---|
| `lib/main.dart` | Application entry point. |
| `lib/config/` | Application configuration. |
| `lib/models/` | Data models used by the application. |
| `lib/screens/` | Main application screens and user interfaces. |
| `lib/services/` | API communication, GPS, and other application services. |
| `lib/widgets/` | Reusable interface components. |
| `pubspec.yaml` | Flutter project configuration and package dependencies. |

The frontend is responsible for user interaction, journey input, navigation presentation, and displaying available detection results and alerts.

### 7.4 Backend Directory

The main backend directory contains the Python API server and GPS bridge.

| File / Directory | Responsibility |
|---|---|
| `api_server.py` | Main backend API server and request handling. |
| `gps_bridge.py` | GPS data communication bridge. |
| `uploads/` | Stores uploaded files when required. |
| `output/` | Stores generated output files. |
| `Pothole_ADAS/` | Contains the main Python project package and its functional modules. |

The backend acts as the central processing and integration layer between the frontend and the individual project services.

### 7.5 Core Python Modules

The main `Pothole_ADAS/` package contains separate modules for different system responsibilities.

#### `adas/`

Contains driver-assistance-related processing and decision logic.

#### `alerts/`

Handles alert-related functionality, including voice-based notifications.

#### `backend/`

Contains backend integration components, including database-related functionality.

#### `camera/`

Responsible for camera input and image acquisition.

#### `detection/`

Contains the AI-based pothole detection implementation using YOLOv8.

#### `gps/`

Handles GPS-related processing and geographical location information.

#### `gui/`

Contains graphical user interface-related components.

#### `mobile_app/`

Contains mobile application-related supporting components.

#### `output/`

Used for storing generated processing outputs.

#### `radar/`

Provides a separate location for radar-related components.

#### `route/`

Contains route-generation and navigation-related functionality.

#### `test_images/`

Contains images used for testing and evaluating the detection pipeline.

### 7.6 Project Organisation and Modularity

The separation of the frontend, API server, GPS bridge, and Python processing modules helps maintain a clear division of responsibilities.

The major components can be developed and tested independently:

- The Flutter frontend manages application interaction.
- The Python API server handles frontend requests.
- The detection module processes road images.
- The GPS module manages geographical information.
- The route module handles navigation-related processing.
- The ADAS and alerts modules support driver-assistance functionality.
- The backend database integration manages relevant application data.

This modular organisation makes the project easier to understand, maintain, debug, and extend as additional functionality is integrated.


## 8. Frontend Architecture (Flutter Application)

### 8.1 Overview

The frontend of POTHOLE_ADAS is developed using **Flutter and Dart**, providing an Android-based mobile application through which users can interact with the pothole detection and driver-assistance system.

The frontend acts as the user interaction layer. It allows users to provide journey information, access location-related functionality, view navigation information, and receive available pothole detection results and alerts.

The application communicates with the Python backend through API services, keeping the user interface separate from the backend's core processing operations.

### 8.2 Frontend Technologies

The frontend uses the following technologies:

- **Flutter:** Framework used to develop the mobile application.
- **Dart:** Programming language used for application logic and interface development.
- **Android SDK:** Provides the Android application environment.
- **HTTP and JSON:** Support communication with the Python backend.
- **Google Maps Platform:** Intended to provide map visualisation and navigation-related functionality.

### 8.3 Frontend Directory Structure

The main Flutter application is organised inside the `lib/` directory.

```text
lib/
│
├── config/
│   └── Application configuration
│
├── models/
│   ├── gps_position.dart
│   ├── route_model.dart
│   └── pothole.dart
│
├── screens/
│   ├── splash_screen.dart
│   ├── home_screen.dart
│   ├── navigation_screen.dart
│   └── history_screen.dart
│
├── services/
│   ├── api_service.dart
│   ├── gps_service.dart
│   └── voice_service.dart
│
├── widgets/
│   ├── gps_status_card.dart
│   ├── pothole_card.dart
│   └── navigation_info.dart
│
├── gps_service.dart
│
└── main.dart
```

### 8.4 Main Frontend Components

#### 1. Main Application Entry Point

**File:** `main.dart`

The `main.dart` file acts as the entry point of the Flutter application.

It is responsible for initialising the application and launching the main interface.

#### 2. Configuration

**Directory:** `config/`

Contains application configuration and related settings required by the frontend.

#### 3. Data Models

**Directory:** `models/`

The models define the data structures used to represent information received from the backend and other application services.

Important models include:

- **gps_position.dart:** Represents GPS position information, including geographical coordinates.
- **route_model.dart:** Represents route-related information received by the application.
- **pothole.dart:** Represents pothole detection information and its associated attributes.

These models help maintain a structured format for application data.

#### 4. Application Screens

**Directory:** `screens/`

Contains the main user-facing screens of the mobile application.

- **splash_screen.dart:** Provides the initial application screen.
- **home_screen.dart:** Acts as the main application interface.
- **navigation_screen.dart:** Provides the navigation-related interface and journey information.
- **history_screen.dart:** Provides access to previously available detection or activity records.

#### 5. Application Services

**Directory:** `services/`

Contains service components responsible for communication with external systems and application functionality.

- **api_service.dart:** Handles communication between the Flutter frontend and Python backend.
- **gps_service.dart:** Manages GPS-related functionality and location information.
- **voice_service.dart:** Supports voice-based notifications and spoken alerts.

The service layer helps separate application logic from the visual interface.

#### 6. Reusable Widgets

**Directory:** `widgets/`

Contains reusable interface components used across different application screens.

- **gps_status_card.dart:** Displays GPS status and related location information.
- **pothole_card.dart:** Presents pothole detection information.
- **navigation_info.dart:** Displays relevant navigation details.

Reusable widgets help maintain a consistent interface and reduce duplication.

### 8.5 User Interaction Workflow

The general frontend interaction follows this sequence:

1. The user launches the POTHOLE_ADAS mobile application.
2. The home screen provides access to the main application functionality.
3. The user enters the required journey information.
4. The frontend communicates with the backend through the API service.
5. The application receives the processed route or detection information.
6. Relevant information is presented through the navigation interface and reusable widgets.
7. The user can access available detection information, history, and voice-based alerts.

### 8.6 Frontend–Backend Communication

The Flutter frontend does not directly execute the Python-based YOLOv8 detection model or backend route-processing logic.

Instead, it communicates with the Python backend through HTTP-based API requests and receives structured responses.

The API service acts as the communication layer between the mobile application and the backend.

This separation provides several advantages:

- Keeps the mobile interface independent of backend processing.
- Makes communication between components easier to manage.
- Allows backend modules to be updated without redesigning the entire frontend.
- Supports future expansion of navigation and driver-assistance features.

### 8.7 Frontend Design Approach

The frontend follows a modular design approach in which screens, data models, services, and reusable widgets are maintained separately.

This organisation improves:

- Code readability and maintainability.
- Reusability of interface components.
- Separation of application responsibilities.
- Integration with backend services.
- Future development and testing.

Overall, the Flutter frontend provides the user-facing foundation of POTHOLE_ADAS, connecting the driver with the application's detection, location, navigation, and alert functionalities.


## 9. Backend Architecture (Python and Flask)

### 9.1 Backend Overview

The backend of POTHOLE_ADAS is developed using **Python**, with **Flask** serving as the web framework for API-based communication.

It acts as the central processing and integration layer of the application, connecting the Flutter frontend with the AI detection model, GPS services, routing functionality, database integration, and driver-assistance modules.

The backend is responsible for receiving application requests, processing the required information, communicating with the appropriate modules, and returning structured responses to the frontend.

Its modular design allows different functionalities to operate as separate components while contributing to the overall system.

### 9.2 Backend Directory Structure

The Python backend is organised into an outer backend project directory and an inner `Pothole_ADAS` package.

The main structure is:

```text
backend/
│
├── api_server.py
├── gps_bridge.py
│
├── uploads/
├── output/
│
└── Pothole_ADAS/
    │
    └── Pothole_ADAS/
        │
        ├── adas/
        ├── alerts/
        ├── backend/
        ├── camera/
        ├── detection/
        ├── gps/
        ├── gui/
        ├── mobile_app/
        ├── output/
        ├── radar/
        ├── route/
        └── test_images/
```

### 9.3 Main Backend Entry Points

#### 1. API Server

**File:** `api_server.py`

The API server provides the communication interface between the Flutter frontend and the Python backend.

Its responsibilities include:

- Receiving HTTP requests from the frontend.
- Processing application inputs.
- Connecting requests with the required backend functionality.
- Returning processed information in a structured response.
- Supporting communication between the mobile application and backend services.

Flask provides the web application framework for handling these API operations.

#### 2. GPS Bridge

**File:** `gps_bridge.py`

The GPS bridge provides a communication layer for geographical location information.

Its responsibilities include:

- Receiving GPS-related information.
- Making the current position available to the backend.
- Supporting communication between the GPS data source and application modules.
- Providing location information for geographical processing.

The GPS bridge works alongside the GPS package to support location-related functionality.

### 9.4 Core Backend Modules

The inner `Pothole_ADAS` package contains separate modules for the major functionalities of the system.

#### 1. ADAS Module

**Directory:** `adas/`

The ADAS module contains driver-assistance-related processing and decision logic.

It supports the evaluation of relevant hazard information and the generation of driver-assistance responses.

#### 2. Alerts Module

**Directory:** `alerts/`

The alerts module handles notification-related functionality.

It supports the communication of relevant pothole and road-hazard information through alert mechanisms, including voice-based notifications.

#### 3. Camera Module

**Directory:** `camera/`

The camera module handles image and video input required by the detection pipeline.

It provides the visual input used for road-condition analysis and pothole detection.

#### 4. Detection Module

**Directory:** `detection/`

The detection module contains the AI-based pothole detection functionality.

It uses the **YOLOv8 object detection model** to analyse road images and identify potholes.

The detection process can produce information such as:

- Detected object class.
- Bounding-box coordinates.
- Detection confidence.
- Relevant image-processing results.

This module forms the core computer-vision component of POTHOLE_ADAS.

#### 5. GPS Module

**Directory:** `gps/`

The GPS module handles geographical location-related processing.

It works with latitude and longitude information and supports the association of detected road hazards with their geographical positions.

#### 6. Backend Integration Module

**Directory:** `backend/`

This package contains backend integration components, including the Firebase-related functionality used for database communication.

It supports the interaction between application processing modules and cloud-based data storage.

#### 7. Route Module

**Directory:** `route/`

The route module is responsible for navigation-related processing.

Its intended functionality includes:

- Processing source and destination information.
- Converting textual locations into geographical coordinates through geocoding.
- Communicating with the Google Routes API.
- Obtaining route information for the application.
- Preparing route-related results for frontend display.

Google Maps Platform is the selected mapping and routing technology for this component.

#### 8. GUI Module

**Directory:** `gui/`

Contains graphical user interface-related components within the Python project.

#### 9. Mobile Application Support Module

**Directory:** `mobile_app/`

Contains mobile-application-related supporting components within the Python project.

The primary Android application itself is maintained separately in the Flutter frontend.

#### 10. Output Directory

**Directory:** `output/`

Used for storing generated results and other processing outputs.

#### 11. Test Images

**Directory:** `test_images/`

Contains image data used for testing and evaluating the pothole detection functionality.

#### 12. Radar Directory

**Directory:** `radar/`

Provides a separate location for radar-related components in the project structure.

The presence of this directory does not imply that radar-based sensing is currently integrated into the working detection pipeline.

### 9.5 Backend Processing Responsibilities

The backend coordinates several important operations:

| Processing Area | Backend Responsibility |
|---|---|
| API Communication | Receives requests and returns responses to the Flutter application. |
| AI Detection | Processes image input through the YOLOv8 detection module. |
| Camera Input | Handles visual data required for detection. |
| GPS Processing | Handles geographical coordinates and location information. |
| Route Processing | Connects navigation requests with geocoding and route services. |
| Database Integration | Communicates with Firebase for relevant data storage and retrieval. |
| ADAS Processing | Handles driver-assistance-related decision logic. |
| Alerts | Supports visual and voice-based notification functionality. |

### 9.6 Backend and Frontend Integration

The Python backend communicates with the Flutter frontend through API-based requests and responses.

The general communication process is:

1. The Flutter application sends a request to the backend.
2. The Flask API server receives the request.
3. The backend identifies the required operation.
4. The relevant Python module processes the information.
5. The backend prepares the result in a structured format.
6. The response is returned to the Flutter application.
7. The frontend displays the available information to the user.

This approach keeps the backend processing independent of the mobile interface.

### 9.7 Backend Design Approach

The backend follows a modular development approach with separate components for detection, camera input, GPS, routing, database integration, ADAS, and alerts.

The major advantages include:

- **Modularity:** Each functionality is maintained separately.
- **Maintainability:** Individual components can be modified and tested independently.
- **Integration:** Different services communicate through the backend.
- **Reusability:** Common processing components can support multiple application operations.
- **Extensibility:** Additional functionality can be incorporated without redesigning the entire backend.

Overall, the Python backend acts as the central processing layer of POTHOLE_ADAS, connecting the AI-based detection system with geographical information, navigation services, cloud storage, and driver-assistance functionality.

