# Companion

An elegant iOS companion application for 42 School students with user profiles, friend management, and project tracking, showcasing modern Swift development practices.

## 📖 About

Companion is a native iOS application that provides comprehensive access to 42 School's student ecosystem. Built with Swift and featuring intuitive user interfaces, secure token storage, and real-time data synchronization with the 42 API.

## 🚀 Features

- **User Profile Management**: Complete 42 student profile visualization with skills, projects, and achievements
- **Friend System**: Add, manage, and track friends within the 42 ecosystem
- **Project Tracking**: View detailed project information, skills progression, and academic level
- **Real-time Data**: Live student data from 42 School's official API
- **Smart Search**: Comprehensive student database with real-time filtering
- **Secure Authentication**: OAuth token management with local storage
- **Loading States**: Smooth loading screens and user feedback
- **Responsive Design**: Adaptive layouts for different screen sizes and orientations
- **42/Pool Switcher**: Toggle between 42 School and Piscine project views
- **Last Location Tracking**: View users' last known campus locations

## 🔧 Build Instructions

### Prerequisites

- iOS 12.0+
- Xcode 11.0+
- Swift 5.0+
- CocoaPods dependency manager

### Setup

```bash
# Clone the repository
git clone https://github.com/danil-kozyr/Companion.git
cd Companion

# Install dependencies
pod install

# Open workspace in Xcode
open swiftCompanion.xcworkspace
```

### API Configuration

The app uses 42 School's official API for student data:

```swift
// NetworkService.swift
private let baseURL = "https://api.intra.42.fr"
private let oauthURL = "https://api.intra.42.fr/oauth/token"
```

## 📝 Usage

### Access the Application

1. Build and run the project in Xcode or iOS Simulator
2. Authenticate using 42 School credentials
3. Grant necessary permissions for data access

### Student Exploration Process

1. Launch the application and authenticate
2. Search for students by login name
3. View detailed user profiles with:
   - Personal information and avatar
   - Skills progression and levels
   - Project history and grades
   - Campus location and coalition
4. Add users to friends list for quick access
5. Switch between 42 School and Piscine views
6. Track friends' progress and locations

## 🎬 Demonstration

<p align="center">
<img src="https://github.com/danilkozyr/iOS-Portfolio/blob/master/gifs/companion.gif" height=600>
</p>

## 🔍 Implementation Details

### Architecture

- **Pattern**: Model-View-Presenter (MVP) with View State management
- **Language**: Swift 5.0
- **Framework**: UIKit with custom UI components
- **Networking**: Asynchronous API calls with completion handlers
- **Storage**: Local token storage with Realm database
- **UI**: Custom cells, rounded views, and smooth animations

### Key Components

- **SearchViewController**: Main search interface with real-time filtering
- **UserViewController**: Detailed user profile display with sections
- **FriendsViewController**: Friend management and quick access
- **LoadingViewController**: Elegant loading states during API calls
- **NetworkService**: Service layer for 42 API communication
- **FetcherService**: Data fetching and caching management
- **Storage**: Local data persistence for friends and tokens

## 🔗 Dependencies

### Third-party Libraries

- **Alamofire**: HTTP networking for 42 School API integration
- **RealmSwift**: Local database for friend management and caching
- **BrightFutures**: Asynchronous programming and promise handling
- **AppCenter**: Analytics and crash reporting for app monitoring

### System Frameworks

- **UIKit**: User interface framework
- **Foundation**: Core system functionality
- **Network**: Network connectivity and reachability
- **LocalAuthentication**: Secure token storage

## 🏗️ Project Structure

```
swiftCompanion/
├── Application/          # App delegate and core configuration
├── MainScreen/           # Search and main interface
├── UserScreen/           # User profile display
├── FriendsScreen/        # Friend management
├── LoadingScreen/        # Loading states
├── Network/              # API services and networking
├── Storage/              # Local data management
└── Constants+Extensions/ # Utilities and extensions
```

---

_Native iOS application demonstrating advanced API integration, local data management, user interface design, and modern iOS development architecture for educational platforms._
