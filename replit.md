# AquaGuard: The Groundwater Hero - Educational Game

## Overview

AquaGuard is a cross-platform educational game designed to teach students and the general public about groundwater conservation and sustainable water management. The application combines interactive storytelling, 3D simulations, mini-games, and quizzes to create an engaging learning experience about environmental conservation.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

The application follows a modern full-stack architecture with a clear separation between client and server components:

### Frontend Architecture
- **Framework**: React 18 with TypeScript for type safety
- **Build Tool**: Vite for fast development and optimized production builds
- **3D Graphics**: Three.js with React Three Fiber for immersive 3D water cycle visualizations
- **UI Framework**: Radix UI components with Tailwind CSS for responsive, accessible design
- **State Management**: Zustand for lightweight, reactive state management
- **Styling**: Tailwind CSS with custom color scheme optimized for educational content

### Backend Architecture
- **Runtime**: Node.js with Express.js framework
- **Database**: PostgreSQL with Drizzle ORM for type-safe database operations
- **Session Management**: In-memory storage with provisions for PostgreSQL sessions
- **API Design**: RESTful API structure with `/api` prefix routing

## Key Components

### Game Engine Components
1. **GameScene**: Main 3D environment using Three.js for water cycle visualization
2. **Tutorial System**: Step-by-step educational content delivery
3. **Story Mode**: Interactive scenarios with decision-based learning
4. **Mini-Games**: Canvas-based interactive activities (well drilling, water filtering, pipe connections)
5. **Quiz System**: Timed question-answer sessions with progress tracking
6. **Water Physics Engine**: Custom physics simulation for realistic water behavior

### UI Components
1. **WaterDropMascot**: Animated character providing guidance and feedback
2. **Progress Tracking**: Visual indicators for learning progression
3. **Audio Management**: Background music and sound effects control
4. **Responsive Interface**: Mobile-first design with touch controls

### Data Management
1. **Game Progress Store**: Tracks user advancement through phases
2. **Audio Store**: Manages sound settings and playback
3. **Local Storage**: Persists user preferences and progress

## Data Flow

### Game Progression Flow
1. **Tutorial Phase**: Introduction to water cycle concepts
2. **Story Mode**: Problem-solving scenarios in different environments
3. **Mini-Games**: Hands-on interactive learning activities
4. **Quiz System**: Knowledge assessment and reinforcement
5. **3D Simulation**: Advanced water management simulation

### User Progress Tracking
- Phase completion status stored locally
- Score accumulation across different activities
- Unlocking system for progressive content access

### Audio System
- Background music management with mute controls
- Sound effects for user interactions
- Accessibility-focused audio design

## External Dependencies

### Core Dependencies
- **@react-three/fiber**: 3D scene management and rendering
- **@react-three/drei**: Three.js utilities and helpers
- **@tanstack/react-query**: Server state management
- **@neondatabase/serverless**: PostgreSQL database connectivity
- **drizzle-orm**: Type-safe database operations
- **date-fns**: Date manipulation utilities

### UI and Styling
- **@radix-ui/***: Accessible UI components
- **tailwindcss**: Utility-first CSS framework
- **clsx**: Conditional class name utility
- **class-variance-authority**: Component variant management

### Development Tools
- **vite**: Build tool and development server
- **tsx**: TypeScript execution for server
- **drizzle-kit**: Database migration and management

## Deployment Strategy

### Development Environment
- Vite development server with HMR for frontend
- Express server with TypeScript compilation via tsx
- Database migrations managed through Drizzle Kit

### Production Build
- Frontend: Vite optimized build with code splitting
- Backend: ESBuild compilation for Node.js deployment
- Database: PostgreSQL with environment-based configuration

### Environment Configuration
- Database URL configuration through environment variables
- Separate client and server build processes
- Asset optimization for 3D models and audio files

### Recent Updates

**January 19, 2025**: Enhanced User Experience and Accessibility
- Added comprehensive Welcome Screen providing direct access to all game modes
- Unlocked all game phases from start to allow users to explore any content immediately  
- Enhanced mini-games with improved collision detection and audio feedback
- Added home navigation button throughout application for seamless phase switching
- Improved game completion logic with proper scoring and progression tracking

### Key Architectural Decisions

1. **Client-Server Separation**: Clean separation allows for independent scaling and deployment of frontend and backend components.

2. **3D Web Graphics**: Three.js integration provides immersive educational experiences without requiring additional plugins or software installation.

3. **TypeScript Throughout**: End-to-end type safety reduces bugs and improves developer experience.

4. **Component-Based Architecture**: Modular design enables easy maintenance and feature additions.

5. **Progressive Enhancement**: Game phases unlock sequentially to ensure proper learning progression (now with optional direct access).

6. **Local-First Data**: User progress stored locally with provisions for future server synchronization.

7. **Accessibility-First Design**: All game modes accessible immediately with clear navigation and audio feedback.

The architecture prioritizes educational effectiveness, accessibility, and cross-platform compatibility while maintaining high performance and user engagement.