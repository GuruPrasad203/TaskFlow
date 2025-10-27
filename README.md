# TaskFlow
Taskflow is an app used to build you daily tasks and challenging task into simple step by step procedure you can follow:
# 🚀 AI-Powered Goal Orchestrator

A full-stack application that transforms high-level goals into self-driving project plans using autonomous AI agents. The system consists of a Node.js/Express backend with MongoDB and a Flutter frontend that provides real-time visualization of AI agent execution.

## 🎯 Project Overview

This project demonstrates how AI agents can revolutionize productivity by automatically decomposing complex goals into actionable tasks and executing them autonomously. Users simply provide a high-level goal, and the AI agent handles the entire planning and execution process.

### Key Features

- **🤖 Autonomous AI Agent**: Automatically breaks down goals into tasks and executes them
- **📱 Real-time Visualization**: Live updates of agent progress and task completion
- **🔧 Tool Integration**: Simulates web search, API calls, and external services
- **📊 Progress Tracking**: Comprehensive analytics and execution statistics
- **🎨 Modern UI**: Beautiful Flutter interface with Material Design 3
- **🔐 Authentication**: Secure user management with JWT tokens
- **📡 Real-time Updates**: WebSocket support for live collaboration

## 🏗️ Architecture

### Backend (Node.js/Express)
- **Framework**: Express.js with ES6 modules
- **Database**: MongoDB with Mongoose ODM
- **Authentication**: JWT-based auth with bcrypt password hashing
- **AI Integration**: OpenAI API for goal decomposition
- **Real-time**: Socket.io for live updates
- **Testing**: Jest with Supertest for API testing

### Frontend (Flutter)
- **Framework**: Flutter 3.8.1+ with Dart
- **State Management**: Provider pattern for reactive updates
- **UI**: Material Design 3 with custom theming
- **Charts**: FL Chart for data visualization
- **HTTP**: HTTP client for API communication
- **Animations**: Smooth transitions and progress indicators

## 📁 Project Structure

```
├── Backend/                    # Node.js/Express API
│   ├── src/
│   │   ├── controllers/        # Route handlers
│   │   ├── models/            # Mongoose schemas
│   │   ├── routes/            # Express routers
│   │   ├── services/          # AI, email, external APIs
│   │   ├── middleware/        # Auth, error handling
│   │   └── utils/             # Helper functions
│   ├── tests/                 # Jest test suites
│   └── docs/                  # Postman collections
│
├── todooo/                    # Flutter mobile app
│   ├── lib/
│   │   ├── screens/           # UI screens
│   │   ├── services/          # AI agent, backend API
│   │   ├── providers/         # State management
│   │   ├── models/            # Data models
│   │   └── widgets/           # Reusable components
│   ├── android/               # Android configuration
│   ├── ios/                   # iOS configuration
│   └── web/                   # Web configuration
│
└── README.md                  # This file
```

## 🚀 Quick Start

### Prerequisites

- **Node.js** 18+ and npm
- **MongoDB** (local or cloud instance)
- **Flutter SDK** 3.8.1+
- **Dart SDK**
- **OpenAI API Key** (for goal decomposition)

### Backend Setup

1. **Navigate to backend directory**
   ```bash
   cd Backend
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Environment configuration**
   Create a `.env` file in the Backend directory:
   ```env
   # Database
   MONGO_URI=mongodb://localhost:27017/goal-orchestrator
   
   # JWT Configuration
   JWT_SECRET=your-super-secret-jwt-key
   JWT_EXPIRES_IN=7d
   
   # OpenAI Configuration
   OPENAI_API_KEY=your-openai-api-key
   
   # Server Configuration
   PORT=4000
   NODE_ENV=development
   
   # Optional: Socket.io
   SOCKET_IO_ENABLED=true
   
   # Optional: External APIs
   GOOGLE_SEARCH_API_KEY=your-google-search-key
   WEATHER_API_KEY=your-weather-api-key
   ```

4. **Start the server**
   ```bash
   # Development mode with auto-reload
   npm run dev
   
   # Production mode
   npm start
   ```

   The API will be available at `http://localhost:4000`

### Frontend Setup

1. **Navigate to Flutter app directory**
   ```bash
   cd todooo
   ```

2. **Install dependencies**
   ```bash
   flutter pub get
   ```

3. **Generate JSON serialization files**
   ```bash
   flutter packages pub run build_runner build
   ```

4. **Run the application**
   ```bash
   # For development
   flutter run
   
   # For specific platform
   flutter run -d chrome    # Web
   flutter run -d android   # Android
   flutter run -d ios       # iOS
   ```

## 🎯 Demo Scenarios

### 1. Travel Planning
**Goal**: "Plan a weekend trip to a beach near Chennai for two people"

**AI Agent Process**:
1. **Goal Analysis**: Identifies travel planning requirements
2. **Task Decomposition**: Creates tasks for destination research, accommodation, budget, and itinerary
3. **Autonomous Execution**: Simulates web search for beaches, hotels, and activities
4. **Dynamic Updates**: Real-time progress with detailed results

### 2. Business Proposal
**Goal**: "Research and create a business proposal for a new mobile app"

**AI Agent Process**:
1. **Goal Analysis**: Identifies business development requirements
2. **Task Decomposition**: Creates tasks for market research, requirements analysis, timeline, and presentation
3. **Autonomous Execution**: Simulates market research and competitive analysis
4. **Dynamic Updates**: Generates comprehensive business insights

### 3. Event Planning
**Goal**: "Organize a team building event for 20 people"

**AI Agent Process**:
1. **Goal Analysis**: Identifies event planning requirements
2. **Task Decomposition**: Creates tasks for venue research, activity planning, budget, and logistics
3. **Autonomous Execution**: Simulates venue search and activity research
4. **Dynamic Updates**: Provides detailed event planning results

## 🔧 API Documentation

### Authentication Endpoints
- `POST /api/auth/signup` - User registration
- `POST /api/auth/login` - User login
- `POST /api/auth/verify-otp` - OTP verification

### Goal Management
- `GET /api/goals` - Get user goals
- `POST /api/goals` - Create new goal
- `GET /api/goals/:id` - Get specific goal
- `PUT /api/goals/:id` - Update goal
- `DELETE /api/goals/:id` - Delete goal

### Task Management
- `GET /api/goals/:goalId/tasks` - Get goal tasks
- `POST /api/goals/:goalId/tasks` - Create task
- `PUT /api/tasks/:id` - Update task
- `DELETE /api/tasks/:id` - Delete task

### AI Agent
- `POST /api/goals/:id/agent/run` - Execute AI agent for goal

### Dashboard
- `GET /api/dashboard/stats` - Get user statistics

## 🧪 Testing

### Backend Testing
```bash
cd Backend
npm test
```

Tests cover:
- Authentication flows
- Goal CRUD operations
- Task management
- AI agent execution
- API error handling

### Frontend Testing
```bash
cd todooo
flutter test
```

## 📱 Screenshots

The app features a modern, intuitive interface with:

- **Dashboard**: Overview with AI Agent promotion
- **Goal Input**: Simple dialog for entering high-level goals
- **Real-time Execution**: Live progress visualization
- **Task Management**: Detailed task breakdown and results
- **Action Timeline**: Complete transparency into agent operations
- **Analytics**: Performance metrics and statistics

## 🛠️ Development

### Backend Development
- Uses ES6 modules with `"type": "module"`
- MongoDB with Mongoose for data persistence
- JWT authentication with bcrypt password hashing
- OpenAI integration for intelligent goal decomposition
- Socket.io for real-time updates
- Comprehensive error handling and validation

### Frontend Development
- Flutter with Material Design 3
- Provider pattern for state management
- Reactive UI with real-time updates
- Custom animations and transitions
- Responsive design for multiple screen sizes
- Clean architecture with separation of concerns

## 🔮 Future Enhancements

- **Real API Integration**: Connect to actual web search, booking, and business APIs
- **Machine Learning**: Improve goal understanding with ML models
- **Multi-language Support**: Internationalization for global users
- **Team Collaboration**: Multi-user goal sharing and collaboration
- **Advanced Analytics**: Detailed insights and performance metrics
- **Voice Interface**: Voice input and output capabilities
- **Calendar Integration**: Sync with Google Calendar, Outlook
- **Email Integration**: Automated email notifications and updates

## 🤝 Contributing

This project was created for educational and demonstration purposes. Contributions are welcome:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🙏 Acknowledgments

- **OpenAI** for providing the AI capabilities
- **Flutter Team** for the amazing cross-platform framework
- **MongoDB** for the flexible database solution
- **Express.js** for the robust backend framework

## 📞 Support

For support, email your-email@example.com or create an issue in the repository.

---

**Built with ❤️ using Flutter, Node.js, and AI Agent principles**

*Transform your goals into reality with the power of AI agents!*

