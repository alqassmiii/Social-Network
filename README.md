# 🌐 Gigabit Social Network

<div align="center">

![Gigabit Landing Page](docs/homepage.png)

**A next-generation social networking platform built for real-time interaction and community building**

[![Go](https://img.shields.io/badge/Go-1.23+-00ADD8?style=for-the-badge&logo=go&logoColor=white)](https://golang.org/)
[![Next.js](https://img.shields.io/badge/Next.js-15-black?style=for-the-badge&logo=next.js&logoColor=white)](https://nextjs.org/)
[![TypeScript](https://img.shields.io/badge/TypeScript-5-blue?style=for-the-badge&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![SQLite](https://img.shields.io/badge/SQLite-3-003B57?style=for-the-badge&logo=sqlite&logoColor=white)](https://www.sqlite.org/)
[![Docker](https://img.shields.io/badge/Docker-Ready-2496ED?style=for-the-badge&logo=docker&logoColor=white)](https://www.docker.com/)

[Features](#-features) • [Tech Stack](#-tech-stack) • [Screenshots](#-screenshots) • [Getting Started](#-getting-started) • [Architecture](#-architecture) • [License](#-license)

</div>

---

## 🎯 Overview

**Gigabit** is a full-stack social networking platform that combines the power of **Go** for high-performance backend services with **Next.js** for a responsive, modern frontend. Built with scalability and user experience in mind, Gigabit offers everything users expect from a contemporary social platform: real-time messaging, community groups, event management, and granular privacy controls.

### 🌟 Why Gigabit?

- **⚡ Real-Time Performance**: WebSocket-based architecture for instant updates and live interactions
- **🎨 Modern UX**: Beautiful, responsive interface built with Next.js 15 and Tailwind CSS
- **🔒 Privacy-First**: Granular privacy controls for posts, profiles, and personal information
- **📱 Responsive Design**: Seamless experience across desktop, tablet, and mobile devices
- **🚀 Production-Ready**: Docker support with health checks and monitoring

---

## ✨ Features

### 👥 Social Networking

- **Dynamic Feed**: Personalized content stream with multiple filter options (All, Friends, Following)
- **Follow System**: Follow users, manage friend requests with pending/accepted states
- **User Profiles**: Customizable profiles with avatars, bios, and privacy settings
- **Profile Privacy**: Control who can see your profile and posts
- **Activity Tracking**: View your posts, comments, likes, and bookmarks in one place

### 💬 Real-Time Communication

- **Instant Messaging**: 
  - One-on-one private chats with real-time delivery
  - Group conversations with multiple participants
  - Typing indicators and online status
  - Message read receipts
  - Rich media support (images, emojis)
  
- **Live Updates**: 
  - WebSocket-powered notifications
  - Real-time feed updates
  - Instant message delivery

### 👥 Groups & Communities

- **Group Management**:
  - Create public or private groups
  - Role-based permissions (Admin, Member)
  - Group invitations and join requests
  - Dedicated group feeds and discussions
  
- **Group Features**:
  - Group-specific posts and comments
  - Member management
  - Group conversations
  - Event organization within groups

### 📅 Events

- **Event Creation**: Schedule events with detailed information
- **RSVP System**: Track attendance with Going/Not Going options
- **Event Discovery**: Browse upcoming events from your groups
- **Calendar Integration**: Visual calendar with event markers
- **Notifications**: Get notified about upcoming events

### 📝 Posts & Content

- **Rich Posts**: 
  - Text posts with formatting
  - Image uploads and galleries
  - Polls with multiple options
  - Post privacy controls (Public, Private, Friends Only, Custom)
  
- **Engagement**:
  - Like and bookmark posts
  - Threaded comments
  - Share posts with your network
  - Vote on polls with real-time results

### 🔔 Notifications

- **Real-Time Alerts**: Instant notifications for:
  - New messages
  - Friend requests
  - Post interactions (likes, comments, shares)
  - Group invitations
  - Event updates
  - Poll votes

### 🔍 Search & Discovery

- **Universal Search**: Search across users, groups, and posts
- **Smart Filters**: Refine results by type and relevance
- **User Discovery**: Find and connect with new people

---

## 🛠 Tech Stack

### Backend

| Technology | Purpose | Version |
|------------|---------|---------|
| **Go** | High-performance server | 1.23+ |
| **Gorilla WebSocket** | Real-time bidirectional communication | Latest |
| **SQLite** | Lightweight database | 3.x |
| **golang-migrate** | Database migrations | v4 |
| **bcrypt** | Password hashing | Latest |
| **UUID** | Unique identifiers | v4 |

### Frontend

| Technology | Purpose | Version |
|------------|---------|---------|
| **Next.js** | React framework with App Router | 15.5+ |
| **React** | UI library | 19.1 |
| **TypeScript** | Type-safe development | 5.x |
| **Tailwind CSS** | Utility-first styling | 4.x |
| **Material-UI** | Component library | 7.x |
| **Emotion** | CSS-in-JS styling | 11.x |
| **SWR** | Data fetching and caching | 2.x |
| **Framer Motion** | Animations | Latest |

### DevOps

- **Docker**: Containerization
- **Docker Compose**: Multi-container orchestration
- **Health Checks**: Automated service monitoring

---

## 📸 Screenshots

### Landing Page
![Landing Page](docs/homepage.png)
*Modern landing page with feature highlights and call-to-action*

### Authentication
<div style="display: flex; gap: 10px;">

![Login](docs/login-page.png)
*Secure login with JWT authentication*

![Register](docs/register-page.png)
*User registration with avatar selection*

</div>

### Main Application

![Feed](docs/feed-page.png)
*Dynamic feed with posts, polls, and real-time updates*

![Profile](docs/profile-page.png)
*User profile with posts, followers, and calendar widget*

![Chats](docs/chats-page.png)
*Real-time messaging with groups and direct messages*

![Events](docs/events-page.png)
*Event management and RSVP system*

---

## 🚀 Getting Started

### Prerequisites

- **Go** 1.23 or higher
- **Node.js** 20+ and npm
- **Docker** (optional, for containerized deployment)

### Option 1: Local Development

1. **Clone the repository**
    ```bash
   git clone https://github.com/yourusername/gigabit-social-network.git
   cd gigabit-social-network
   ```

2. **Start the backend**
   ```bash
   cd Backend
   go mod download
   go run . --mock --clear  # Load mock data for testing
   ```
   The backend will start on `http://localhost:8080`

3. **Start the frontend** (in a new terminal)
   ```bash
   cd Frontend
   npm install
   npm run dev
   ```
   The frontend will start on `http://localhost:3000`

4. **Access the application**
   - Open `http://localhost:3000` in your browser
   - Use demo credentials:
     - Email: `john.doe@example.com`
     - Password: `Aa123456`

### Option 2: Docker Deployment

1. **Build and start services**
    ```bash
    ./build.sh
   ```
   
   Or manually:
   ```bash
   docker compose build
   docker compose up -d
   ```

2. **Access the application**
   - Frontend: `http://localhost:3000`
   - Backend API: `http://localhost:8080`
   - Health Check: `http://localhost:8080/health`

3. **View logs**
   ```bash
   docker compose logs -f
   ```

4. **Stop services**
   ```bash
   docker compose down
   ```

### Using the Run Script

The project includes a unified `run.sh` script for common tasks:

```bash
# Development
./run.sh dev          # Start both frontend and backend

# Production
./run.sh build        # Build production artifacts
./run.sh start        # Start production servers

# Docker
./run.sh docker:build    # Build Docker images
./run.sh docker:up       # Start containers
./run.sh docker:down     # Stop containers
./run.sh docker:logs     # View logs
./run.sh docker:status   # Check container health

# Utilities
./run.sh test         # Run tests
./run.sh lint         # Run linters
./run.sh clean        # Clean build artifacts
```

---

## 🏗 Architecture

### System Architecture

```
┌─────────────────┐         ┌─────────────────┐         ┌─────────────────┐
│                 │         │                 │         │                 │
│  Next.js        │◄────────┤  Go Backend     │◄────────┤  SQLite         │
│  Frontend       │         │  (REST + WS)    │         │  Database       │
│                 │         │                 │         │                 │
└─────────────────┘         └─────────────────┘         └─────────────────┘
        │                           │
        │                           │
        ├───── HTTP/HTTPS ──────────┤
        │                           │
        └───── WebSocket ───────────┘
```

### Backend Structure

```
Backend/
├── handlers/           # HTTP request handlers
│   ├── auth.go        # Authentication & sessions
│   ├── post.go        # Post management
│   ├── chat_handler.go# Chat endpoints
│   ├── group.go       # Group management
│   ├── event.go       # Event handling
│   └── ...
├── services/          # Business logic layer
│   ├── post_service.go
│   ├── chat_service.go
│   ├── group_service.go
│   └── ...
├── models/            # Data structures
│   ├── user.go
│   ├── post.go
│   ├── message.go
│   └── ...
├── websocket/         # Real-time communication
│   ├── hub.go         # WebSocket hub
│   ├── client.go      # Client connections
│   ├── handlers.go    # Message handlers
│   └── types.go       # Message types
├── middleware/        # HTTP middleware
│   ├── auth.go        # JWT validation
│   └── error.go       # Error handling
├── pkg/db/            # Database layer
│   ├── migrations/    # SQL migrations
│   └── sqlite/        # SQLite utilities
└── mockdata/          # Sample data for testing
```

### Frontend Structure

```
Frontend/
├── app/               # Next.js App Router
│   ├── feed/         # Feed pages
│   ├── chats/        # Chat interface
│   ├── profile/      # User profiles
│   ├── events/       # Event pages
│   └── ...
├── components/        # React components
│   ├── chat/         # Chat components
│   ├── posts/        # Post components
│   ├── groups/       # Group components
│   ├── events/       # Event components
│   ├── layout/       # Layout components
│   └── ui/           # Reusable UI components
├── context/           # React Context providers
│   ├── AuthContext.tsx
│   ├── WebSocketContext.tsx
│   └── ToastContext.tsx
├── hooks/             # Custom React hooks
│   ├── useAuth.ts
│   ├── useWebSocket.ts
│   ├── usePosts.ts
│   └── ...
├── lib/               # Utilities and API clients
│   ├── api/          # API service layer
│   └── api.ts        # Base API client
└── types/             # TypeScript type definitions
```

### Key Design Patterns

- **RESTful API**: Standard HTTP endpoints for CRUD operations
- **WebSocket Hub**: Central hub for managing real-time connections
- **Service Layer**: Business logic separated from HTTP handlers
- **Repository Pattern**: Database operations abstracted in services
- **JWT Authentication**: Stateless authentication with secure tokens
- **Context API**: Global state management in React
- **Custom Hooks**: Reusable logic for data fetching and state

---

## 🔌 API Documentation

### Authentication

| Endpoint | Method | Description |
|----------|--------|-------------|
| `/api/register` | POST | Create a new user account |
| `/api/login` | POST | Authenticate and receive JWT token |
| `/api/logout` | POST | Invalidate session |

### Posts

| Endpoint | Method | Description |
|----------|--------|-------------|
| `/api/posts` | GET | Fetch posts (feed) |
| `/api/posts` | POST | Create a new post |
| `/api/posts/{id}` | GET | Get specific post |
| `/api/posts/{id}/like` | POST | Like/unlike a post |
| `/api/posts/{id}/comment` | POST | Comment on a post |
| `/api/posts/{id}/bookmark` | POST | Bookmark a post |
| `/api/posts/{id}/share` | POST | Share a post |

### Groups

| Endpoint | Method | Description |
|----------|--------|-------------|
| `/api/groups` | GET | List all groups |
| `/api/groups` | POST | Create a new group |
| `/api/groups/{id}` | GET | Get group details |
| `/api/groups/{id}/join` | POST | Join a group |
| `/api/groups/{id}/leave` | POST | Leave a group |
| `/api/groups/{id}/posts` | GET | Get group posts |

### Messages

| Endpoint | Method | Description |
|----------|--------|-------------|
| `/api/conversations` | GET | List conversations |
| `/api/conversations/{id}/messages` | GET | Get messages |
| `/api/messages` | POST | Send a message |

### Events

| Endpoint | Method | Description |
|----------|--------|-------------|
| `/api/events` | GET | List events |
| `/api/events` | POST | Create an event |
| `/api/events/{id}` | GET | Get event details |
| `/api/events/{id}/rsvp` | POST | RSVP to event |

### WebSocket

Connect to `/ws` for real-time updates:
- Message notifications
- Post updates
- Online status
- Typing indicators

---

## 🔐 Security Features

- **Password Hashing**: bcrypt with salt
- **JWT Tokens**: Secure, stateless authentication
- **CORS Protection**: Configured for production
- **SQL Injection Prevention**: Prepared statements
- **XSS Protection**: Input sanitization
- **Privacy Controls**: Granular permissions for posts and profiles

---

## 🎨 UI/UX Highlights

- **Responsive Design**: Mobile-first approach with breakpoints for all devices
- **Dark Theme**: Eye-friendly color scheme throughout
- **Smooth Animations**: Framer Motion for delightful interactions
- **Accessibility**: ARIA labels and keyboard navigation
- **Loading States**: Skeletons and spinners for better UX
- **Error Handling**: User-friendly error messages and retry mechanisms
- **Toast Notifications**: Non-intrusive feedback for user actions

---

## 📦 Database Schema

The application uses SQLite with 50+ migration files covering:

- **Users**: Profiles, authentication, privacy settings
- **Posts**: Content, privacy, likes, bookmarks
- **Comments**: Threaded discussions
- **Messages**: Private and group conversations
- **Groups**: Communities with memberships
- **Events**: Event details and RSVPs
- **Polls**: Poll options and votes
- **Notifications**: Activity tracking
- **Sessions**: JWT session management
- **Follows**: User relationships

---

## 🧪 Testing

The project includes mock data for easy testing:

```bash
# Start backend with mock data
cd Backend
go run . --mock --clear
```

This loads:
- 30+ test users
- Sample posts with images and polls
- Group conversations
- Events and RSVPs
- Friend connections
- Messages and notifications

**Demo Credentials:**
- Email: `john.doe@example.com`
- Password: `Aa123456`

All test users use the same password for convenience.

---

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request. For major changes, please open an issue first to discuss what you would like to change.

### Development Guidelines

1. Follow the existing code structure
2. Write clear commit messages
3. Add tests for new features
4. Update documentation as needed
5. Ensure all tests pass before submitting PR

---

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE.md) file for details.

---

## 👨‍💻 Author

**Your Name**

- GitHub: [@yourusername](https://github.com/yourusername)
- LinkedIn: [Your LinkedIn](https://linkedin.com/in/yourusername)

---

## 🙏 Acknowledgments

- Next.js team for the amazing React framework
- Go community for excellent tooling and libraries
- Material-UI for beautiful components
- All open-source contributors whose libraries made this project possible

---

<div align="center">

**⭐ Star this repo if you find it useful!**

Made with ❤️ and lots of ☕

</div>
