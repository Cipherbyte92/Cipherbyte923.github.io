# Replit.md

## Overview

This is a full-stack web application built with React on the frontend and Express.js on the backend. The application features Discord OAuth authentication with advanced user access control (whitelist/blacklist functionality) and an admin panel for user management. It uses a PostgreSQL database with Drizzle ORM for data persistence and includes a comprehensive UI component library built with Tailwind CSS and Radix UI.

## System Architecture

### Frontend Architecture
- **Framework**: React 18 with TypeScript
- **Build Tool**: Vite for development and bundling
- **Routing**: Wouter for client-side routing
- **State Management**: TanStack Query (React Query) for server state
- **Styling**: Tailwind CSS with custom design system
- **UI Components**: Comprehensive component library using Radix UI primitives
- **Form Handling**: React Hook Form with Zod schema validation

### Backend Architecture
- **Framework**: Express.js with TypeScript
- **Authentication**: OpenID Connect (OIDC) with Passport.js for Discord OAuth
- **Session Management**: Express sessions with PostgreSQL store
- **Database**: PostgreSQL with Drizzle ORM
- **API**: RESTful API with JSON responses
- **Security**: Session-based authentication with access control middleware

### Database Schema
- **Users Table**: Stores user profiles with admin/whitelist/blacklist flags
- **Sessions Table**: Manages user sessions (required for Replit Auth)
- **User Access Logs Table**: Tracks user authentication attempts and access patterns

## Key Components

### Authentication System
- **Discord OAuth Integration**: Full OAuth2 flow with Discord as identity provider
- **Access Control**: Three-tier system (admin, whitelisted, blacklisted users)
- **Session Management**: Secure session handling with PostgreSQL storage
- **Access Logging**: Comprehensive logging of authentication events

### Admin Panel
- **User Management**: View and manage all registered users
- **Access Control**: Toggle whitelist/blacklist status for users
- **Statistics Dashboard**: User metrics and system overview
- **Activity Monitoring**: Access logs and user activity tracking

### UI Component System
- **Design System**: Consistent styling with CSS variables and Tailwind
- **Responsive Design**: Mobile-first approach with adaptive layouts
- **Accessibility**: ARIA-compliant components using Radix UI
- **Theme Support**: Light/dark mode capability built into the design system

## Data Flow

1. **User Authentication**: Users authenticate via Discord OAuth, creating/updating user records
2. **Access Control Check**: System validates user whitelist/blacklist status before granting access
3. **Session Management**: Valid users receive secure sessions stored in PostgreSQL
4. **API Requests**: Frontend makes authenticated requests to backend APIs
5. **Admin Operations**: Admins can modify user access controls and view system statistics
6. **Logging**: All authentication events are logged for monitoring and audit purposes

## External Dependencies

### Core Dependencies
- **@neondatabase/serverless**: PostgreSQL connection pooling
- **drizzle-orm**: Type-safe ORM for database operations
- **passport**: Authentication middleware framework
- **openid-client**: OpenID Connect client for OAuth flows
- **@tanstack/react-query**: Server state management
- **@radix-ui/***: Headless UI component primitives

### Development Tools
- **Vite**: Frontend build tool and development server
- **TypeScript**: Type safety across the entire stack
- **Tailwind CSS**: Utility-first CSS framework
- **ESBuild**: Backend bundling for production

## Deployment Strategy

### Development Environment
- **Hot Reload**: Vite development server with HMR
- **Database**: PostgreSQL instance with automatic migrations
- **Port Configuration**: Frontend on port 5000, backend integrated

### Production Build
- **Frontend**: Vite builds static assets to `dist/public`
- **Backend**: ESBuild bundles server code to `dist/index.js`
- **Database Migrations**: Drizzle manages schema changes
- **Environment Variables**: Secure configuration for OAuth and database

### Replit Integration
- **Auto-deployment**: Configured for Replit's autoscale deployment
- **Module Requirements**: Node.js 20, Web, and PostgreSQL 16
- **Session Storage**: Uses Replit-compatible session management

## Changelog

```
Changelog:
- June 23, 2025. Initial setup
```

## User Preferences

```
Preferred communication style: Simple, everyday language.
```