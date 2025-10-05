# Sentinel Email Guardian

An AI-powered email security system designed specifically for elderly users and non-tech-savvy individuals. Sentinel protects users from malware, organizes junk mail, and sends warnings to suspicious senders.

## 🏗️ Project Structure

```
Sentinel/
├── backend/                 # Java Spring Boot API
│   ├── src/main/java/com/sentinel/
│   │   ├── controller/      # REST API endpoints
│   │   ├── service/         # Business logic
│   │   ├── model/           # Data models
│   │   ├── config/          # Configuration
│   │   └── repository/      # Database access
│   └── pom.xml             # Maven dependencies
├── frontend/               # React JavaScript UI
│   ├── src/
│   │   ├── components/     # Reusable UI components
│   │   ├── pages/          # Main application screens
│   │   ├── services/       # API communication
│   │   └── styles/         # Elderly-friendly CSS
│   └── package.json        # NPM dependencies
└── docker-compose.yml      # Full deployment setup
```

## 🚀 Quick Start

### Prerequisites
- Java 17+
- Node.js 18+
- Maven 3.6+
- Docker (optional)

### Running the Application

#### Method 1: Local Development

**Backend (Java):**
```bash
cd backend
mvn spring-boot:run
```
The API will be available at http://localhost:8080

**Frontend (React):**
```bash
cd frontend
npm install
npm start
```
The UI will be available at http://localhost:3000

#### Method 2: Docker
```bash
docker-compose up --build
```

## 🎯 Key Features

### For Users
- **Large, clear buttons** - Easy navigation for elderly users
- **Simple language** - No technical jargon
- **One-click email scanning** - Automatic malware detection
- **Junk mail organization** - Smart filtering with user consent
- **Warning system** - Automatic replies to suspicious senders

### Technical Features
- **Email Integration** - IMAP/POP3 support for major providers
- **Malware Detection** - File analysis using Apache Tika + VirusTotal
- **AI-Powered Filtering** - Natural language processing for threat detection
- **Secure Architecture** - Spring Security with encrypted communication
- **Responsive Design** - Works on desktop, tablet, and mobile

## 🔧 Configuration

### Email Setup
Configure email credentials in `backend/src/main/resources/application.properties`:

```properties
spring.mail.username=your-email@gmail.com
spring.mail.password=your-app-password
```

### VirusTotal API
Get a free API key from [VirusTotal](https://www.virustotal.com/gui/join-us) and set:

```properties
app.virustotal.api-key=your-api-key
```

## 📱 User Interface Design

The interface is specifically designed for elderly users:

- **Minimum 60px button height**
- **18px+ font sizes**
- **High contrast colors**
- **Clear visual feedback**
- **Simple navigation flow**

## 🧪 Testing

**Backend Tests:**
```bash
cd backend
mvn test
```

**Frontend Tests:**
```bash
cd frontend
npm test
```

## 📦 Deployment

### Production Build
```bash
# Frontend
cd frontend
npm run build

# Backend
cd backend
mvn clean package
```

### Docker Production
```bash
docker-compose -f docker-compose.prod.yml up --build
```

## 🔐 Security

- Spring Security for authentication
- Encrypted email communication
- Secure file analysis sandbox
- No storage of email credentials
- Regular security dependency updates

## 🤝 Contributing

1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly with elderly user scenarios
5. Submit a pull request

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 💡 Design Philosophy

Sentinel is built with the principle that cybersecurity should be accessible to everyone, regardless of technical expertise. Every design decision prioritizes clarity, simplicity, and user confidence.