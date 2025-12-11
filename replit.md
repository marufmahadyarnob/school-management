# EduManage - School Management System

## Overview
A comprehensive school management software designed for small to medium schools with approximately 500 students and 2-3 teachers. The system provides tools for managing students, teachers, classes, attendance, and grades.

## Current State
- **Status**: MVP Complete
- **Authentication**: Replit Auth (OpenID Connect)
- **Database**: PostgreSQL with Drizzle ORM
- **Frontend**: React with Shadcn UI components
- **Styling**: Tailwind CSS with Inter font

## Features
1. **Dashboard** - Overview with key metrics (total students, teachers, classes, today's attendance)
2. **Student Management** - Full CRUD with class assignment, guardian info, enrollment tracking
3. **Teacher Management** - Full CRUD with subject specialization
4. **Class Management** - Create classes, assign teachers, track student count
5. **Attendance Tracking** - Mark daily attendance by class with status (present, absent, late, excused)
6. **Grade Management** - Record grades by subject and exam type with percentage/letter grade display

## Tech Stack
- **Frontend**: React, Tailwind CSS, Shadcn UI, TanStack Query, Wouter
- **Backend**: Express.js, Node.js
- **Database**: PostgreSQL with Drizzle ORM
- **Auth**: Replit Auth (OpenID Connect)

## Project Structure
```
├── client/src/
│   ├── components/     # UI components (AppSidebar, ThemeToggle)
│   ├── hooks/          # Custom hooks (useAuth, useTheme)
│   ├── lib/            # Utilities (queryClient, authUtils)
│   └── pages/          # Page components (Dashboard, Students, Teachers, etc.)
├── server/
│   ├── db.ts           # Database connection
│   ├── routes.ts       # API endpoints
│   ├── storage.ts      # Database operations
│   └── replitAuth.ts   # Authentication setup
└── shared/
    └── schema.ts       # Database schema and types
```

## API Endpoints
- `GET/POST /api/students` - List/Create students
- `GET/PATCH/DELETE /api/students/:id` - Student operations
- `GET/POST /api/teachers` - List/Create teachers
- `GET/PATCH/DELETE /api/teachers/:id` - Teacher operations
- `GET/POST /api/classes` - List/Create classes
- `GET/PATCH/DELETE /api/classes/:id` - Class operations
- `GET /api/attendance?classId=&date=` - Get attendance for class/date
- `POST /api/attendance/bulk` - Save multiple attendance records
- `GET/POST /api/grades` - List/Create grades
- `GET/PATCH/DELETE /api/grades/:id` - Grade operations
- `GET /api/dashboard/stats` - Dashboard statistics

## Database Tables
- `users` - Authenticated users (Replit Auth)
- `sessions` - Session storage
- `students` - Student records
- `teachers` - Teacher records
- `classes` - Class/course records
- `attendance` - Daily attendance records
- `grades` - Student grades

## Design Guidelines
- Font: Inter
- Primary color: Blue (#2563eb)
- Uses Material Design principles for data-heavy interfaces
- Sidebar navigation with collapsible menu
- Responsive design for all screen sizes

## Running the Application
```bash
npm run dev
```
The application runs on port 5000.

## User Preferences
- Clean, professional UI
- Data tables for list views
- Modal dialogs for add/edit forms
- Status badges for visual indicators
