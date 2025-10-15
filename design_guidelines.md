# Design Guidelines: B.Tech Learning Platform

## Design Approach
**Reference-Based**: Drawing inspiration from Scaler, Coursera, and Linear to create a modern, student-friendly educational platform. The design balances professional credibility with youthful energy, making complex learning paths feel accessible and achievable.

## Core Design Elements

### A. Color Palette

**Light Mode:**
- Primary: 250 85% 50% (Vibrant indigo/blue - conveys trust and intelligence)
- Secondary: 220 90% 96% (Soft blue-gray for backgrounds)
- Accent: 160 75% 45% (Teal for success states, achievements)
- Text: 220 20% 20% (Deep charcoal)
- Surface: 0 0% 100% (Pure white cards)

**Dark Mode:**
- Primary: 250 80% 60% (Brighter indigo for contrast)
- Secondary: 220 15% 15% (Rich dark gray)
- Accent: 160 70% 55% (Brighter teal)
- Text: 220 10% 95% (Off-white)
- Surface: 220 15% 12% (Elevated dark cards)

### B. Typography
- **Primary Font**: 'Inter' (Google Fonts) - clean, modern, excellent readability
- **Display Font**: 'Poppins' (Google Fonts) - for headlines and hero text
- **Monospace**: 'JetBrains Mono' (for code snippets in resources)

**Scale:**
- Hero: text-5xl to text-7xl (Poppins, font-bold)
- Section Headers: text-3xl to text-4xl (Poppins, font-semibold)
- Subsections: text-xl to text-2xl (Inter, font-semibold)
- Body: text-base (Inter, font-normal)
- Captions: text-sm (Inter, font-medium)

### C. Layout System
**Spacing Units**: Consistently use 4, 6, 8, 12, 16, 20, 24 for Tailwind spacing (p-4, m-8, gap-6, etc.)

**Container Strategy:**
- Full-width sections with inner max-w-7xl container
- Content-heavy sections: max-w-6xl
- Reading content: max-w-4xl
- Cards and grids: Use the full container width with responsive gaps

### D. Component Library

**Navigation:**
- Sticky header with logo, main nav links, search bar, user profile
- Transparent on hero, solid background on scroll
- Mobile: Hamburger menu with slide-in drawer

**Hero Section:**
- Large impactful image showing diverse students collaborating/coding (80vh height)
- Overlay gradient (from primary color at 60% opacity to transparent)
- Bold headline: "Launch Your Tech Career" or similar inspiring message
- Subheading explaining the platform's value
- Primary CTA button + Secondary "Explore Courses" button (outline variant with backdrop-blur)

**Course Cards:**
- Elevated cards (shadow-lg) with course thumbnail/icon at top
- Course title, brief description, difficulty badge
- Tech stack tags (small rounded pills)
- Progress bar for enrolled courses
- Hover: Subtle lift effect (scale-105 transform)
- Grid: 1 column mobile, 2 tablet, 3-4 desktop

**Roadmap Visualization:**
- Interactive timeline/flowchart design
- Nodes for each learning milestone with connecting lines
- Color-coded by track (Web Dev, Data Science, AI/ML, etc.)
- Completed steps: Accent color, Current: Primary, Upcoming: Muted
- Click to expand details in modal/side panel

**Company Showcase:**
- Logo grid with hover effects revealing company details
- Filter by industry, package range, hiring frequency
- Company cards showing: Logo, roles hired, average package, selection rate

**Resource Cards:**
- Categorized tabs: Interview Prep, DSA, System Design, Aptitude
- Clean list view with resource type icons (video, article, practice)
- Difficulty and estimated time indicators
- Bookmark functionality

**Dashboard (For logged-in users):**
- Progress overview with circular progress indicators
- Upcoming deadlines/milestones
- Recommended next steps
- Recent activity feed

### E. Interactions & Animations
**Minimal, purposeful animations:**
- Smooth page transitions (150ms)
- Card hover: Subtle scale (1.02) and shadow increase
- Button: Scale down on click (0.98)
- Navigation: Fade-in menu items with stagger
- Progress indicators: Animated fills on view
- Loading states: Skeleton screens, NOT spinners

## Page Structure

**Homepage:**
1. Hero with inspiring imagery and clear value proposition
2. Featured Courses (3-4 cards)
3. Learning Paths Overview (3 columns: Web, Data, Core CS)
4. Placement Stats (companies + success metrics)
5. Student Success Stories (2-3 testimonial cards)
6. CTA Section for sign-up

**Courses Page:**
- Filter sidebar (department, difficulty, duration)
- Grid layout with search and sort
- Each course shows: Image, title, instructor, rating, duration, enrollment count

**Roadmap Page:**
- Department selector tabs at top
- Interactive visual roadmap
- Sidebar with detailed view of selected milestone
- Download roadmap option

**Placement Section:**
- Company directory with advanced filters
- Interview experiences (anonymized student stories)
- Preparation checklist for each company

**Resources Hub:**
- Categorized tabs (DSA, System Design, Aptitude, Coding Practice)
- Search with filters
- Curated collections/playlists
- External resource links with descriptions

## Images

**Hero Image:** Full-width, high-quality photo showing diverse B.Tech students coding together or celebrating achievement. Should feel energetic and aspirational. Position: Behind gradient overlay at top of homepage.

**Course Thumbnails:** Tech-themed abstract illustrations or relevant technology logos for each course. Clean, modern style matching brand colors.

**Company Logos:** High-resolution company logos in their brand colors, displayed on subtle background cards.

**Success Story Photos:** Authentic student photos (headshots) in circular frames with subtle border in accent color.

**Roadmap Visuals:** Custom illustrated icons for each learning milestone - books, code brackets, certificates, etc.

## Accessibility & Responsiveness
- All interactive elements minimum 44x44px touch targets
- WCAG AA contrast ratios maintained in both modes
- Semantic HTML with proper ARIA labels
- Keyboard navigation fully supported
- Mobile-first responsive: Stack columns on mobile, expand to multi-column on tablet/desktop
- Form inputs with consistent dark mode styling (borders, backgrounds)

This design creates a professional yet approachable platform that motivates B.Tech students while providing clear, organized access to all learning resources.