# Anniversary App Specifications - claude.md

## Project Overview

Building a React-based interactive web presentation to celebrate parents' 40th wedding anniversary (July 27th, 1985 - July 27th, 2025). The app will tell their love story through 5 chapters with photos, animations, and background music.

**Target Audience**: Parents (Dad 70, Mom 63) and extended family  
**Primary Access**: Mobile devices (iPhone/Android)  
**Timeline**: Complete by July 27th, 2025 (12 days from July 15th)  
**Budget**: Free tools and libraries only

## Technical Requirements

### Core Tech Stack

- **React** (Create React App or Vite)
- **React Router DOM** - chapter navigation
- **Tailwind CSS** - mobile-first styling
- **Framer Motion** - smooth animations
- **React Image Gallery** - photo displays
- **Howler.js** - background music
- **React Use Gesture** - mobile touch interactions

### Key Features

1. **Password Protection** - family-only access
2. **5 Interactive Chapters** - story progression
3. **Mobile-Optimized** - primary mobile experience
4. **Background Music** - classical pieces (Debussy, Beethoven)
5. **Photo Galleries** - 25-35 total photos across chapters
6. **Touch Gestures** - swipe navigation between chapters
7. **Responsive Design** - works on phones, tablets, laptops

### Development Specifications

This project uses modular specifications stored in the `.claude/` directory:

- **[Code Analysis](.claude/code-analysis.md)** - Comprehensive code analysis with dependency mapping, quality metrics, and performance review
- **[Commit](.claude/commit.md)** - Conventional commits with emojis and structured process
- **[Create Docs](.claude/create-docs.md)** - Component and feature documentation templates
- **[Update Docs](.claude/update-docs.md)** - LLM-optimized documentation with concrete file references and systematic analysis
- **[Code Quality](.claude/code-quality.md)** - Formatting, linting, and quality assurance procedures
- **[Project Structure](.claude/project-structure.md)** - Maintainable folder organization and architectural principles

## Content Structure

### Chapter 1: "1985 - Two Hearts, One Journey" (4-6 photos)

- Wedding photos
- Early dating/engagement photos
- Young couple photos (first few years)
- **Story**: Met in grad school, engaged for 2 weeks, married after visiting Taiwan

### Chapter 2: "Building Our Family" (6-8 photos)

- Pregnancy photos
- Each daughter as baby/toddler with parents
- Early family photos
- **Story**: Three daughters - "their greatest achievements"

### Chapter 3: "Adventures Around the World" (6-8 photos)

- Travel photos by destination (France - favorite, cruises, Europe)
- Cultural events and concerts
- **Story**: Love for travel, classical music, shared adventures

### Chapter 4: "The Parents We're Blessed With" (6-8 photos)

- Graduation photos with each daughter
- Birthday celebrations and milestones
- Recent family gatherings
- **Story**: Supportive parents, always there for milestones

### Chapter 5: "Today & Tomorrow" (4-6 photos)

- Houston move photos (moved 2 weeks ago)
- Taichi class photos (new shared activity)
- Recent couple photos
- Sisters' engagement photos with parents
- **Story**: New chapter in Houston, still growing and loving

## User Experience Requirements

### Mobile-First Design

- **Touch-friendly** navigation (large tap targets)
- **Swipe gestures** between chapters
- **Vertical scrolling** within chapters
- **Fast loading** optimized images
- **Readable text** on small screens

### Accessibility Considerations

- **High contrast** text and backgrounds
- **Alt text** for all images
- **Large enough touch targets** (44px minimum)
- **Simple navigation** for older users

### Performance Requirements

- **Fast initial load** (< 3 seconds)
- **Smooth animations** (60fps)
- **Optimized images** (WebP format, lazy loading)
- **Efficient memory usage**

## Family Context (Important for UX)

### About the Parents

- **Technology comfort**: Prefer simple, intuitive interfaces
- **Interests**: Classical music (Debussy, Beethoven), travel, staying active
- **Current life**: New to Houston, taking taichi together, very close family

### About the Family

- **Three daughters**: One in Bay Area (developer), two in Houston
- **Close family**: Regular communication, shared experiences
- **Recent excitement**: Two daughters recently engaged
- **Family dog**: Parents have grown to love sister's dog

## Technical Implementation Guidelines

### Component Structure

```
src/
├── components/
│   ├── PasswordProtection.js
│   ├── ChapterNavigation.js
│   ├── PhotoGallery.js
│   ├── MusicPlayer.js
│   └── SwipeableChapter.js
├── pages/
│   ├── Chapter1.js (Love Story)
│   ├── Chapter2.js (Building Family)
│   ├── Chapter3.js (Adventures)
│   ├── Chapter4.js (Parents)
│   └── Chapter5.js (Today)
├── data/
│   └── photos.js
└── App.js
```

### Key Libraries to Install

```bash
npm install react-router-dom tailwindcss framer-motion react-image-gallery howler react-use-gesture react-swipeable react-icons @headlessui/react
```

### Photo Organization

- **Store in public/photos/** directory
- **Organize by chapter** (chapter1/, chapter2/, etc.)
- **Include thumbnails** for faster loading
- **Use WebP format** when possible
- **Max file size**: 500KB per photo

### Music Integration

- **3-4 classical pieces** rotating through chapters
- **Background volume**: ~30% (not overwhelming)
- **User controls**: Play/pause, volume
- **Suggested tracks**:
  - Debussy: "Clair de Lune", "Arabesque No. 1"
  - Beethoven: "Moonlight Sonata", "Für Elise"

### Password Protection

- **Simple client-side** validation
- **Family-friendly password** (anniversary date or meaningful phrase)
- **Session persistence** (remembered until browser closes)
- **Elegant landing page** with password input

## Development Approach

### Phase 1 (Days 1-2): Foundation

- Set up React project with required dependencies
- Implement password protection
- Create basic routing structure
- Organize and optimize photos

### Phase 2 (Days 3-4): Core Features

- Build photo galleries for each chapter
- Implement chapter navigation
- Add basic animations with Framer Motion
- Test mobile responsiveness

### Phase 3 (Days 5-6): Polish

- Add background music integration
- Implement swipe gestures
- Fine-tune animations and transitions
- Add personal messages from daughters

### Phase 4 (Days 7-8): Testing & Deployment

- Test across devices (iPhone, Android, tablets)
- Performance optimization
- Deploy to free hosting (Netlify/Vercel)
- Final family testing

## Design Principles

### Visual Style

- **Elegant and timeless** - not trendy
- **Warm color palette** - soft pinks, blues, creams
- **Classical typography** - serif fonts for elegance
- **Generous white space** - not cluttered
- **High-quality photography** as primary visual element

### Emotional Tone

- **Celebratory but reverent** - honoring their journey
- **Personal and intimate** - family-focused
- **Nostalgic warmth** - celebrating memories
- **Forward-looking hope** - acknowledging their future

### User Journey

1. **Password entry** - builds anticipation
2. **Chapter progression** - tells story chronologically
3. **Interactive exploration** - users control pace
4. **Emotional crescendo** - building to current happiness
5. **Celebration finale** - anniversary wishes and love

## Success Metrics

### Technical Success

- **Cross-device compatibility** - works on all family devices
- **Smooth performance** - no lag or crashes
- **Easy navigation** - intuitive for older users
- **Quick loading** - maintains engagement

### Emotional Success

- **Tears of joy** - emotionally resonant
- **Easy sharing** - family can share with others
- **Memorable experience** - something they'll return to
- **Family conversation** - sparks stories and memories

## Deployment & Sharing

### Hosting

- **Netlify** or **Vercel** (free tiers)
- **Custom domain** if desired (optional)
- **HTTPS enabled** for security
- **Mobile-optimized** hosting

### Access Method

- **Direct link** shared with family
- **Password protection** for privacy
- **"Add to Home Screen"** capability for app-like experience
- **Offline access** after initial load

## Important Notes for Implementation

### Family Sensitivities

- **Mom's recent anxiety** - avoid overwhelming interactions
- **Health considerations** - simple, stress-free experience
- **Technology comfort** - prioritize ease of use over advanced features
- **Cultural appreciation** - acknowledge their Asian heritage appropriately

### Quality Over Complexity

- **Focus on storytelling** over technical features
- **Prioritize emotional impact** over visual effects
- **Ensure reliability** over cutting-edge features
- **Optimize for their devices** over general compatibility

### Timeline Reality Check

- **12 days is achievable** with this scope
- **Start simple, enhance progressively**
- **Test early and often** with mobile devices
- **Have backup plan** (simpler version) ready

This specification balances technical achievability with emotional impact, ensuring a meaningful celebration that honors 40 years of love while being realistic about development timeline and family needs.
