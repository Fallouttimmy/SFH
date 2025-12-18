# Design Guidelines: Searchforhelp - Dutch Helpline Directory

## Project Context
This is a **Vercel-compatible migration** of the Searchforhelp (Crisis Navigator) website. The design has been preserved exactly from the original implementation.

## Design System

### Color Palette
The design uses a teal/cyan primary color scheme (hue 198) with:
- **Primary**: `198 88% 35%` (light) / `198 88% 45%` (dark) - A professional teal color
- **Destructive**: `0 84% 42%` - Used for emergency alerts and warnings
- **Neutral grays** for backgrounds, cards, and text

### Typography
- **Font Family**: Inter (sans-serif)
- **Hierarchy**: 
  - H1: `text-3xl md:text-4xl font-semibold`
  - H2: `text-2xl font-semibold`
  - H3: `text-lg font-medium`
  - Body: Default text
  - Muted: `text-muted-foreground`

### Spacing
- Container max-width: `max-w-6xl`
- Standard padding: `px-4 py-8` or `px-4 py-12`
- Card padding: `p-6`
- Gaps: `gap-4` for grids, `gap-2` for inline elements

### Components Used
1. **EmergencyBanner** - Fixed red banner at top with emergency numbers
2. **Header** - Sticky navigation with search, logo, and navigation links
3. **HeroSection** - Blue primary-colored hero with search
4. **CategoryCard** - Cards with icons for each category
5. **HelplineCard** - Cards displaying helpline details with call buttons
6. **Footer** - Three-column footer with links and contact info
7. **MobileEmergencyBar** - Fixed bottom bar on mobile with emergency buttons

### Dark Mode
Fully implemented with:
- Class-based toggle (`darkMode: ["class"]`)
- ThemeProvider with localStorage persistence
- System preference detection
- Smooth transitions

### Emergency Design Elements
- Red banner always visible at top
- Mobile fixed emergency bar at bottom
- Emergency helplines marked with "Noodlijn" badge
- Direct tel: links for one-tap calling

## Vercel Deployment Configuration
- `vercel.json` configured for serverless functions
- API routes in `/api` directory
- Static frontend served from build output
- Rewrites for client-side routing

## Key Features Preserved
1. Dutch language interface (Nederlands)
2. All 8 helpline categories
3. 27+ helplines with contact details
4. Search functionality
5. Dark/light mode toggle
6. Responsive design
7. Emergency call buttons
8. Category navigation
