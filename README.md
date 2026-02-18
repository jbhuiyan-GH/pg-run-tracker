# 🎯 PG Run Tracker v6.0

**Field Service Management System with GPS Tracking**

A comprehensive web-based solution for managing field service operations, tracking PG (Power Generator) sessions, and monitoring site activities in real-time.

---

## ✨ Features

### 🗺️ GPS Tracking
- Real-time location capture with high accuracy
- Start/End location tracking for each session
- Distance calculation between locations
- Google Maps integration for visualization
- Accuracy indicators (High/Medium/Low)

### ⏱️ Session Management
- Start new PG run sessions
- Resume existing sessions
- Complete sessions with detailed reports
- Session history with filtering
- Live countdown timers for active sessions

### 📊 Alarm Correlation
- Automatic alarm detection during PG runs
- Cross-day alarm processing
- Alarm history correlation
- Real-time alarm notifications
- Validation status tracking

### 📈 Reporting & Analytics
- Session duration tracking
- Cost calculation per session
- Site-wise performance reports
- Export to Excel functionality
- WhatsApp report generation

### 🔐 User Authentication
- Secure login system
- Role-based access control
- Session management
- Activity logging

---

## 🛠️ Technologies Used

### Frontend
- **HTML5** - Semantic markup
- **CSS3** - Modern styling with gradients
- **JavaScript** - Interactive features
- **Bootstrap 5.3** - Responsive framework
- **jQuery 3.7.0** - DOM manipulation
- **AJAX** - Asynchronous data loading

### Backend
- **PHP 8.0+** - Server-side logic
- **PDO** - Database abstraction
- **RESTful API** - Clean architecture
- **Session Management** - Secure authentication

### Database
- **Azure SQL Server** - Cloud database
- **SQL Server** - On-premise alternative
- **Optimized queries** - High performance
- **Transaction support** - Data integrity

### APIs & Services
- **Google Maps JavaScript API** - Location services
- **Geolocation API** - GPS coordinates
- **Chart.js** - Data visualization

---

## 📸 Screenshots

### Dashboard
![Dashboard](screenshots/dashboard.png)
*Main dashboard showing active sessions and statistics*

### Start PG Run
![Start Session](screenshots/start-session.png)
*GPS-enabled session start interface*

### Session History
![History](screenshots/history.png)
*Complete session history with filtering*

### Alarm Correlation
![Alarms](screenshots/alarms.png)
*Real-time alarm monitoring and correlation*

---

## 🚀 Installation

### Prerequisites
```bash
- PHP 8.0 or higher
- SQL Server / Azure SQL Database
- Web server (Apache/Nginx)
- Modern web browser with GPS support
- Google Maps API key
```

### Step 1: Clone Repository
```bash
git clone https://github.com/jbhuiyan-GH/pg-run-tracker.git
cd pg-run-tracker
```

### Step 2: Database Setup
```sql
-- Import the database schema
-- File: database/schema.sql

-- Update connection settings in config.php
$serverName = "your-server.database.windows.net";
$database = "your-database";
$username = "your-username";
$password = "your-password";
```

### Step 3: Configure Google Maps API
```javascript
// Update in index.php
const GOOGLE_MAPS_API_KEY = 'your-api-key-here';
```

### Step 4: Launch Application
```bash
# For development
php -S localhost:8000

# For production
# Deploy to your web server
```

### Step 5: Access Application
```
http://localhost:8000
or
https://your-domain.com
```

---

## 📋 Usage

### Starting a PG Run Session

1. **Navigate to Dashboard**
   - Click "Start PG Run" button

2. **Select Site**
   - Choose from dropdown list
   - System captures GPS location automatically

3. **Fill Details**
   - Ticket ID (optional)
   - Event number
   - Remarks

4. **Start Session**
   - Click "Start Session"
   - GPS coordinates captured
   - Session begins tracking

### Completing a Session

1. **Navigate to Active Sessions**
2. **Click "Complete" on running session**
3. **Fill End Details**
   - End time (auto-filled)
   - Final remarks
   - Cost information
4. **Submit**
   - GPS end location captured
   - Duration calculated
   - Report generated

---

## 🗄️ Database Schema

### Main Tables

#### `pg_run_tracker`
- Session management
- GPS coordinates
- Duration tracking
- Cost calculation

#### `tickets`
- Ticket information
- Site details
- Category mapping

#### `alarm_data`
- Alarm records
- Correlation data
- Processing status

#### `users`
- User authentication
- Role management
- Session tracking

---

## 🔧 Configuration

### Database Connection
```php
// config.php
$connectionOptions = [
    "Database" => "your_database",
    "Uid" => "your_username",
    "PWD" => "your_password",
    "CharacterSet" => "UTF-8",
    "TrustServerCertificate" => true
];
```

### Google Maps API
```javascript
// Get your API key from:
// https://console.cloud.google.com/
const GOOGLE_MAPS_API_KEY = 'your-api-key';
```

---

## 📊 Features in Detail

### GPS Accuracy Levels
- **High (0-10m)**: Green indicator
- **Medium (10-50m)**: Yellow indicator
- **Low (50m+)**: Red indicator

### Session Types
- **NEW**: Start fresh session
- **RESUME**: Continue existing session
- **COMPLETE**: End session

### Alarm Correlation
- Automatic detection during session
- Cross-day processing
- Multiple alarm types support
- Real-time updates

---

## 🔐 Security Features

- ✅ SQL injection prevention (prepared statements)
- ✅ XSS protection (input sanitization)
- ✅ CSRF tokens
- ✅ Secure password hashing
- ✅ Session management
- ✅ Input validation
- ✅ Error logging

---

## 📈 Performance Optimization

- ✅ Indexed database queries
- ✅ AJAX for async operations
- ✅ Lazy loading of data
- ✅ Caching strategies
- ✅ Optimized SQL queries
- ✅ Minimal HTTP requests

---

## 🐛 Known Issues

- GPS accuracy depends on device hardware
- Requires HTTPS for GPS in production
- Internet connection required for maps

---

## 🔄 Version History

### v6.0 (Current)
- ✅ Enhanced GPS tracking
- ✅ Alarm correlation system
- ✅ Improved UI/UX
- ✅ Session resume functionality
- ✅ Advanced reporting
- ✅ Live countdown timers
- ✅ WhatsApp report generation

### v5.0
- ✅ Basic GPS tracking
- ✅ Session management
- ✅ User authentication

---

## 📝 License

MIT License - see [LICENSE](LICENSE) file for details

---

## 👤 Author

**MJ Bhuiyan**
- GitHub: [@jbhuiyan-GH](https://github.com/jbhuiyan-GH)
- Location: Dhaka, Bangladesh
- Specialization: Full-Stack Web Development, Azure SQL, GPS Integration

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 💬 Support

For support, create an issue in this repository or contact via GitHub.

---

## ⭐ Show Your Support

Give a ⭐️ if this project helped you!

---

## 📸 More Screenshots

### Mobile View
![Mobile](screenshots/mobile.png)
*Responsive mobile interface*

### Reports
![Reports](screenshots/reports.png)
*Comprehensive reporting dashboard*

### Settings
![Settings](screenshots/settings.png)
*Configuration and settings panel*

---

**Built with ❤️ using PHP, Azure SQL, Bootstrap, and Google Maps API**

---

## 🏷️ Tags

`php` `gps-tracking` `field-service-management` `azure-sql` `bootstrap5` `javascript` `web-application` `real-time-tracking` `google-maps` `session-management`
