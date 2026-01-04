# Erzino - Design Guidelines

## Design Approach
**Reference-Based Approach:** Drawing inspiration from modern SaaS platforms like Linear (typography and spacing), Stripe (restraint and clarity), and Netflix (cinematic dark aesthetics) while incorporating Spider-Man color palette for brand distinction.

## Visual Theme & Color Strategy

**Spider-Man Color Palette** (https://www.schemecolor.com/spiderman.php)
- Primary: Deep crimson reds and bold blues
- Accent: Vibrant web-pattern inspired highlights
- Neutrals: Dark charcoal backgrounds with lighter gray text
- Glassmorphism overlays with subtle color tints

**Dark Mode Primary** with optional light mode toggle throughout application

## Typography

**Font Family:** Outfit (Google Fonts)
- Hero Headings: Outfit Bold, 48-72px desktop / 32-48px mobile
- Section Headings: Outfit SemiBold, 32-40px desktop / 24-32px mobile
- Subheadings: Outfit Medium, 20-24px
- Body Text: Outfit Regular, 16-18px
- Captions/Labels: Outfit Regular, 14px
- Buttons: Outfit SemiBold, 16px

## Layout System

**Spacing Primitives:** Tailwind units of 2, 4, 6, 8, 12, 16, 20, 24
- Component padding: p-4, p-6, p-8
- Section spacing: py-16, py-20, py-24
- Grid gaps: gap-4, gap-6, gap-8
- Card spacing: p-6, p-8

**Container Strategy:**
- Max-width: max-w-7xl for content sections
- Full-width backgrounds with contained content
- Responsive breakpoints: sm (640px), md (768px), lg (1024px), xl (1280px)

## Component Library

### Navigation
- Sticky header with glassmorphism backdrop blur
- Logo left, navigation center, auth/profile right
- Mobile: Hamburger menu with slide-out drawer
- Active state: Subtle underline or highlighted background

### Hero Section
- Full-width cinematic background with video preview or abstract gradient animation
- Large hero image showing video translation interface in action
- Centered heading with supporting subtext
- Primary CTA: "Start Translating Free" with blurred background when over image
- Secondary CTA: "View Pricing"
- Trust indicators: "30 Minutes Free • No Credit Card Required"

### Pricing Cards
- Three-column grid (desktop) / stacked (mobile)
- Glassmorphic card design with subtle borders
- Tier badges: "Free", "Standard", "Student" with color-coded accents
- Interactive slider for minute selection (Standard/Student tiers)
- Real-time price calculation display
- Feature comparison checkmarks
- Prominent CTA button per tier

### Video Player Interface
- Dark theme video player with custom controls
- Smart Sync subtitle overlay with styling controls (paid tiers)
- Timeline scrubber with subtitle markers
- Caption customization panel: font size, color, background opacity (paid)
- Download buttons for .srt/.vtt formats (paid)

### Dashboard
- Sidebar navigation (desktop) / bottom tabs (mobile)
- Video history grid with thumbnail previews (paid)
- Processing status indicators with real-time WebSocket updates
- Analytics cards with glassmorphic backgrounds
- Shared link management table (paid)

### Forms & Inputs
- Floating labels with smooth transitions
- Glassmorphic input backgrounds
- 6-digit verification code input with auto-focus progression
- Clear validation states: success (green accent), error (red accent), loading (animated)
- Password strength indicator
- Checkbox/radio with custom Spider-Man inspired accent colors

### Buttons
- Primary: Bold background with Spider-Man red/blue gradient
- Secondary: Outlined with hover fill
- Tertiary: Text-only with underline on hover
- Glass buttons on images: backdrop-blur-md with semi-transparent backgrounds
- Consistent padding: px-6 py-3 for standard, px-8 py-4 for hero CTAs
- Rounded corners: rounded-lg

### Data Display
- Admin tables: Striped rows, sortable columns, pagination
- Stats cards: Large numbers with trend indicators
- Invoice records: Expandable rows with download options
- Analytics charts: Dark-themed with Spider-Man accent colors

### Overlays & Modals
- Glassmorphic modal backgrounds with backdrop blur
- Centered content with smooth fade-in animation
- Close button (top-right) with hover state
- Student verification modal with step progression
- Payment confirmation overlays

### Onboarding & Tooltips
- Contextual tooltips with arrow pointers
- Step-by-step onboarding overlay for first-time users
- Dismiss and "Don't show again" options
- Positioned to avoid covering critical UI elements

## Animations & Micro-interactions

**Use Sparingly:**
- Hero section: Subtle gradient animation or video background
- Button hovers: Scale transform (1.02) and shadow increase
- Card hovers: Slight lift with shadow depth change
- Loading states: Spinner or skeleton screens (no full-page blockers)
- Success/error: Brief toast notifications (bottom-right)
- Page transitions: Smooth fade between routes

**Avoid:**
- Excessive scroll-triggered animations
- Auto-playing video with sound
- Distracting parallax effects

## Responsive Behavior

**Desktop (lg+):**
- Multi-column layouts for pricing, features, video history
- Persistent sidebar navigation
- Expanded video player with full controls

**Tablet (md):**
- Two-column grids collapse where appropriate
- Maintained spacing hierarchy
- Slide-out navigation drawer

**Mobile (base):**
- Single-column layouts throughout
- Bottom navigation for dashboard
- Simplified video controls with expandable options
- Touch-optimized button sizes (min 44x44px)

## Images

**Hero Section:**
- Large hero image (1920x1080): Screenshot or mockup of Erzino video player interface with Smart Sync subtitles active, showing translation in action
- Alternative: Abstract cinematic gradient background with floating UI elements

**Feature Sections:**
- Smart Sync demonstration: Side-by-side video frames with synchronized subtitle overlays
- Platform logos: YouTube, Vimeo, Dailymotion icons
- Student verification: University building or study environment
- Dashboard preview: Analytics and video history interface mockup

**Pricing Section:**
- No images, focus on glassmorphic card design

**Footer:**
- Minimal background texture or gradient continuation from hero