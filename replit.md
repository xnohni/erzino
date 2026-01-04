# Erzino - AI Video Translation Platform

## Overview

Erzino is a full-stack web application providing AI-powered professional translations for Video-On-Demand (VOD) content from platforms like YouTube, Vimeo, and Dailymotion. The platform features Smart Sync technology that ensures subtitles align perfectly with speech, custom caption styling, and a tiered pricing system for different user types (free, standard, and student tiers with academic email verification).

## User Preferences

Preferred communication style: Simple, everyday language.

## System Architecture

### Frontend Architecture
- **Framework**: React 18 with TypeScript
- **Routing**: Wouter (lightweight React router)
- **State Management**: TanStack React Query for server state
- **UI Components**: shadcn/ui component library built on Radix UI primitives
- **Styling**: Tailwind CSS with custom design tokens following a Spider-Man inspired color palette
- **Typography**: Outfit font family from Google Fonts
- **Theme**: Dark mode primary with light mode toggle support

### Backend Architecture
- **Runtime**: Node.js with Express
- **Language**: TypeScript with ESM modules
- **Build Tool**: esbuild for server bundling, Vite for client
- **API Pattern**: RESTful endpoints under `/api` prefix
- **Authentication**: Session-based with bcrypt password hashing

### Data Layer
- **ORM**: Drizzle ORM with PostgreSQL dialect
- **Schema Location**: `shared/schema.ts` (shared between client and server)
- **Validation**: Zod schemas with drizzle-zod integration
- **Database**: PostgreSQL (configured via DATABASE_URL environment variable)

### Key Design Patterns
- **Monorepo Structure**: Client code in `client/`, server in `server/`, shared types in `shared/`
- **Path Aliases**: `@/` for client source, `@shared/` for shared modules
- **Component Organization**: UI primitives in `components/ui/`, feature components organized by domain
- **Storage Abstraction**: `server/storage.ts` provides interface for all database operations

### Video Processing Pipeline
The application implements a multi-step processing workflow:
1. Audio extraction from video URL
2. Speech-to-text transcription (GPT-4o-Transcribe)
3. Translation to target language (GPT-4o-Mini)
4. Smart Sync caption generation with timing alignment

### Pricing System
- Dynamic pricing based on minutes with admin-configurable API costs
- Three user tiers: Free (30 minutes), Standard, and Student (17% discount)
- Student verification via academic email domain validation

## External Dependencies

### AI Services
- **OpenAI GPT-4o-Transcribe**: Audio transcription ($0.0062/minute default)
- **OpenAI GPT-4o-Mini**: Translation and student email verification ($0.00053/minute default)

### Video Platforms
- YouTube, Vimeo, and Dailymotion URL parsing and video metadata extraction

### Database
- PostgreSQL with connection pooling via `pg` package
- Session storage with `connect-pg-simple`

### Payment Processing
- Stripe integration for minute purchases (configured via environment)

### Development Tools
- Vite dev server with HMR
- Replit-specific plugins for development (cartographer, dev-banner, runtime-error-modal)