# TechCareer - B.Tech Learning Platform

## Overview

TechCareer is a comprehensive educational platform designed for B.Tech students across all engineering departments. The platform provides curated courses, placement preparation resources, career roadmaps, interview materials, and department-specific syllabus content. It aims to bridge the gap between academic learning and industry requirements by offering a modern, student-friendly interface inspired by platforms like Scaler, Coursera, and Linear.

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture

**Framework & Tooling**
- React with TypeScript for type-safe component development
- Vite as the build tool and development server
- Wouter for lightweight client-side routing
- TanStack Query (React Query) for server state management and caching

**UI Component System**
- Shadcn/ui component library with Radix UI primitives for accessible, headless components
- Tailwind CSS for utility-first styling with custom design tokens
- Class Variance Authority (CVA) for type-safe component variants
- Theme system supporting light/dark mode with localStorage persistence

**Design System**
- Custom color palette with HSL-based theming (primary: indigo/blue, accent: teal)
- Typography hierarchy using Inter (body), Poppins (display), and JetBrains Mono (code)
- Consistent spacing system based on 4px grid
- Responsive layout with mobile-first approach

**State Management Strategy**
- React Query handles all server state with infinite stale time (data doesn't auto-refetch)
- Local component state via React hooks
- Theme state persisted to localStorage
- Form state managed through React Hook Form with Zod validation

### Backend Architecture

**Server Framework**
- Express.js with TypeScript for the REST API
- ESM module system throughout the codebase
- Custom request logging middleware for API monitoring
- Error handling middleware with standardized error responses

**API Design Pattern**
- RESTful endpoints following resource-based naming
- Consistent response format with proper HTTP status codes
- Validation using Zod schemas shared between client and server
- CRUD operations for: Courses, Companies, Roadmaps, Resources, and Syllabus

**Storage Layer**
- In-memory storage implementation (MemStorage class) for development
- Interface-based design (IStorage) allowing easy swap to database implementation
- UUID-based identifiers for all entities
- Type-safe data models using Drizzle ORM schemas

### Data Architecture

**Database Schema (Drizzle ORM with PostgreSQL)**
- **Courses**: Educational content with department categorization, difficulty levels, instructor details, and enrollment tracking
- **Companies**: Placement partner information including hiring patterns, salary data, and interview processes
- **Roadmaps**: Career path guidance with structured steps and milestones
- **Resources**: Learning materials categorized by type (video, article, practice) and topic
- **Syllabus**: Department and semester-specific curriculum content

**Schema Design Principles**
- UUID primary keys for all tables
- Array fields for flexible multi-value data (tags, roles)
- Text fields for rich content storage
- Integer fields for metrics (enrollment counts)
- Drizzle Zod integration for automatic schema validation

### Development Tooling

**Build & Development**
- Vite with HMR for fast development feedback
- TSX for running TypeScript server code in development
- Separate build processes for client (Vite) and server (esbuild)
- Path aliases (@/, @shared/) for clean imports

**Code Quality**
- TypeScript strict mode enabled
- ESLint and type checking via tsc
- Consistent module resolution (bundler strategy)

**Development Environment**
- Replit-specific plugins for error handling and debugging
- Custom Vite middleware for development features
- Environment-based configuration (NODE_ENV)

## External Dependencies

### Third-Party UI Libraries
- **Radix UI**: Comprehensive set of unstyled, accessible components (@radix-ui/react-*)
  - Dialog, Dropdown, Popover, Toast, Tabs, Select, and 20+ other primitives
  - Handles accessibility, keyboard navigation, and screen reader support
- **Embla Carousel**: Performant carousel/slider functionality
- **cmdk**: Command palette/search interface component
- **Lucide React**: Icon library for consistent iconography
- **Vaul**: Drawer/bottom sheet component for mobile interfaces

### Data & State Management
- **TanStack Query v5**: Server state management with caching, refetching, and optimistic updates
- **React Hook Form**: Form state management with performance optimization
- **Zod**: Schema validation for forms and API data
- **Drizzle Zod**: Bridge between Drizzle ORM and Zod validation

### Database & ORM
- **Drizzle ORM**: Type-safe SQL query builder and schema management
- **@neondatabase/serverless**: Serverless PostgreSQL driver for Neon database
- **Drizzle Kit**: CLI tool for migrations and schema pushing

### Styling & Utilities
- **Tailwind CSS**: Utility-first CSS framework with custom configuration
- **Class Variance Authority**: Utility for creating variant-based component APIs
- **clsx & tailwind-merge**: Conditional class name utilities
- **date-fns**: Date manipulation and formatting

### Development & Build Tools
- **Vite**: Frontend build tool and dev server
- **esbuild**: Fast bundler for server-side code
- **TypeScript**: Type system and compiler
- **@replit/vite-plugin-***: Replit-specific development enhancements
  - Runtime error modal overlay
  - Cartographer for code navigation
  - Development banner

### Session & Storage
- **connect-pg-simple**: PostgreSQL session store for Express (suggests future authentication implementation)
- **express-session**: Session middleware (implied by connect-pg-simple presence)

### Fonts (Google Fonts CDN)
- Inter: Primary body text font
- Poppins: Display and headline font
- JetBrains Mono: Monospace font for code snippets