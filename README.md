# 🏃 FitTrack - GPS Activity Tracker

A lightweight, privacy-focused web application for tracking and visualizing GPS activity routes. Built as a simple alternative to heavy fitness apps, FitTrack runs entirely offline with local data storage.

[![Java](https://img.shields.io/badge/Java-17+-orange.svg)](https://www.oracle.com/java/)
[![Javalin](https://img.shields.io/badge/Javalin-5.6-blue.svg)](https://javalin.io/)
[![SQLite](https://img.shields.io/badge/SQLite-3.44-green.svg)](https://www.sqlite.org/)
[![License](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

## ✨ Features

- 📍 **GPS Route Recording** - Track activities using browser geolocation API
- 🗺️ **Interactive Maps** - Visualize routes on OpenStreetMap with Leaflet.js
- 📊 **Statistics Dashboard** - View weekly/monthly distance, duration, and progress
- 🔒 **Privacy First** - All data stored locally in SQLite (no cloud sync)
- 🌐 **Offline Capable** - Works without internet after initial load
- 📱 **Responsive Design** - Desktop and tablet friendly

## 🎯 Target Users

- College students tracking daily walks/runs
- Casual fitness enthusiasts
- Privacy-conscious users avoiding cloud-based trackers
- Anyone wanting a simple, no-frills activity logger

## 🛠️ Tech Stack

| Component | Technology |
|-----------|-----------|
| **Backend** | Springboot |
| **Database** | SQLite (file-based, zero-config) |
| **Frontend** | HTML5, CSS3, Vanilla JavaScript |
| **Maps** | Leaflet.js + OpenStreetMap (free!) |
| **Charts** | Chart.js for statistics visualization |
| **Build** | Maven |

## 🚀 Quick Start

### Prerequisites
- Java 17 or higher
- Maven 3.6+

### Installation
```bash
# Clone the repository
git clone https://github.com/yourusername/fittrack.git
cd fittrack

# Install dependencies
mvn clean install

# Run the application
mvn exec:java -Dexec.mainClass="com.fittrack.Main"

# Or build and run JAR
mvn clean package
java -jar target/fittrack-1.0-SNAPSHOT.jar
```

Open your browser and navigate to `http://localhost:8080`

## 📸 Screenshots

[Add screenshots here of:
- Activity recording interface
- Map visualization
- Statistics dashboard
- Activity history list]

## 🏗️ Project Structure
```
fittrack/
├── src/main/java/com/fittrack/
│   ├── Main.java                   # Application entry point
│   ├── controllers/                # REST API endpoints
│   ├── services/                   # Business logic
│   ├── dao/                        # Data access layer
│   ├── models/                     # POJOs
│   └── utils/                      # Helpers (Haversine, etc.)
├── src/main/resources/public/
│   ├── *.html                      # Frontend pages
│   ├── css/                        # Stylesheets
│   └── js/                         # JavaScript modules
└── data/
    └── fittrack.db                 # SQLite database
```

## 📖 API Documentation

See [API_SPECIFICATION.md](docs/API_SPECIFICATION.md) for complete REST API documentation.

### Example Endpoints
```bash
POST   /api/auth/signup              # Create account
POST   /api/auth/login               # Login
GET    /api/activities               # Get activity history
POST   /api/activities               # Start new activity
POST   /api/activities/{id}/points   # Add GPS points
GET    /api/activities/{id}/points   # Get route data
GET    /api/stats/weekly             # Weekly statistics
GET    /api/export/{id}/csv          # Export to CSV
```

## 🗺️ How It Works

1. **Start Recording** → App captures GPS position every 5 seconds
2. **Save Points** → Coordinates stored in SQLite with timestamps
3. **Stop Recording** → Calculate total distance using Haversine formula
4. **Visualize** → Render route as polyline on Leaflet map
5. **Analyze** → View statistics and export data

## 🧪 Testing
```bash
# Run all tests
mvn test

# Run specific test
mvn test -Dtest=DistanceCalculatorTest
```

## 📚 Documentation

- [Product Requirements Document](docs/GPS_Activity_Tracker_PRD.md)
- [Quick Start Guide](docs/QUICK_START_GUIDE.md)
- [API Specification](docs/API_SPECIFICATION.md)

## 🛣️ Roadmap

### Phase 1 (Weeks 1-4) ✅
- [x] User authentication
- [x] Activity recording
- [x] GPS point storage

### Phase 2 (Weeks 5-8) 🚧
- [ ] Map visualization
- [ ] Statistics dashboard
- [ ] Responsive UI

### Phase 3 (Weeks 9-12) 📋
- [ ] CSV export/import
- [ ] Performance optimization
- [ ] Testing & documentation

### Future Enhancements 🔮
- Progressive Web App (PWA)
- Heart rate integration (wearables)
- Social features (share routes)
- Goal setting and achievements

## 🤝 Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- [Javalin](https://javalin.io/) - Lightweight Java web framework
- [Leaflet.js](https://leafletjs.com/) - Open-source mapping library
- [OpenStreetMap](https://www.openstreetmap.org/) - Free map data
- [Chart.js](https://www.chartjs.org/) - Simple yet flexible charting


**Made with ❤️ and Java**
```

---

## 🏷️ Repository Topics/Tags (for GitHub)

Add these tags to help people find your repo:
```
java
javalin
sqlite
gps-tracker
fitness-tracker
activity-tracker
leaflet
openstreetmap
web-application
rest-api
maven
offline-first
privacy
geolocation
haversine
chart-js
