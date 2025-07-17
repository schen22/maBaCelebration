# PRD: Anniversary App for Ma, Ba

## Problem alignment

Problem Alignment

### The Problem

**Problem**: Our family wants to celebrate my parents' 40th anniversary in a meaningful way that brings our family together. Family members are spread across different states with conflicting schedules and limited time to coordinate.
**Goal**:Celebrating this milestone properly would show how much we value their 40+ years of dedication to building our family and supporting us through major life transitions.
**Why now**: Without coordinated planning, we'll miss this once-in-a-lifetime opportunity.

## High-level Approach

Build a React-based interactive web presentation to celebrate parents' 40th wedding anniversary for parents and family to easily access and view via mobile. This will be delivered in the next two weeks to celebrate on 7/29/2025.

### Goals

**Success metrics**: Bring family together and have people cry (happy tears). :D

1. Feelings:

- Enable parents to feel loved, cared for, and celebrated/appreciated for all their dedication and love for our family.
- Reminisce on memories, and preview how much there is to look forward to

2. Does it work: Store memories and well wishes
3. Longevity: Can loved ones return at any time to view
4. Performance: Responsive interactions, low latency, can be viewed offline after loading once.
5. Usability/Apperance: UI is welcoming, simple, but engaging. Easy to use/read/navigate for people who need larger text, basic smartphone users as measured by time spent, click through rate, number of visits, drop off rate.

#### Non-goals

1. We aren't enabling people to share, comment
2. We will not need to build on this in the future. Should be a one-time dev thing.
3. We will not be building an photo/video editing tool, upload media, complex storage model, or rebuilding online tools we can take advantage of

## Solution Alignment

### Key Features / Plan of record

P0's are must haves. Everything else are nice to haves.

- P0: Showcase family photos/moments for parents to relive: start small with maybe 25-35 total photos
- P0: Compile daughters' congratulatory letters for daughters to convey love/appreciation
- P0: Maintain privacy via simple password protection
- P0: Allow creator (i.e. myself) to edit/add/update as needed (either via code or cross-collaboration). Focus on optimal path in terms of dev + maintenance cost.
- Photo management:

  - **P0: Image Optimization:** Automatic resizing, lazy loading, compression needs
  - **P0: Storage:** Serve photos via Github, or wherever can store for free. (Was thinking netlify + github)
  - **P2: Upload Process:** Enable any daughter to upload photos and edit/add letters
  - **P2: Photo Metadata:** Captions, dates, location info. This would be great if we could auto-label, or make it easier to enable collaboration to add caption/dates.

- Easily navigate between moments to bring family together to reminisce and remark on loving each other.
- Responsive design: works on phones, tablets, laptops but optimizes for mobile experience and low dev cost/maintenance
- Gestures - swipe navigation between chapters
- Animation + Background music - simple animation that doesn't distract from experience, which classical pieces playing in the background (Debussy, Beethoven)

#### Emotional Design Goals

**Tone:** Warm, elegant, celebratory, intimate
**Visual Style:** Family scrapbook feel - warm and fuzzy vibes
**Music/Sound:** Background music: Beethoven or non classical like Don McClean and Carpenters. Kinderszenen, Op 15: Traumerei by Schumann.

#### To be decided

- How to organize photos. Current options:
  - Chronological timeline
  - Life stages (wedding, kids, traveling, present, every day moments)
  - By family member/relationship
  - Random/mixed presentation
- Estimated phopto count: Roughly 20-50 photos, but want to make sure there's an easy to build layout before adding intricacies. Decrease photos/media to support if this adds more complexity to handle/maintain.
- Length of letters and letter format from daughters. Current options:
  - Full text letters
  - Short messages/notes
  - Video messages with text
  - Audio recordings wiht photos
  - Mix of formats

### Key Flows

1. Family enters via provided website domain (https)
2. On entering password, family can view website
3. Viewer will scroll, navigate, read/listen, reminisce
4. Viewer can tap to view, zoom in, scroll back; replay media if needed. Extra: tap to save

### Key Milestones

| Target date | Milestone | Description |
| 7/18/2025 | Alignment | Complete spec and choose mock to implement with CC |
| 7/24/2025 | Beta | Early cohort (i.e. daughters) |
| 7/26/2025 | Early Access | Expand to significant others i guess |
| 7/29/2025 | Launch | Show/measure/monitor with family! |

## Constraints

### Technical Constraints

**Development Time:** 12 days - 2 days of planning, 8 days of building, 2 days of testing/refining.
**Technical Skill Level:** I'm coding in conjunction with Claude Code. Would be great to pair program, where I drive architecture, review code/layout, polishes needed, and Claude Code implements.
**Hosting/Domain:** Keep it simple. I was thinking to re-use Netlify.
**Budget for Tools:** \$0.

### Technical Success

- **Cross-device compatibility** - works on all family devices
- **Smooth performance** - no lag or crashes
- **Easy navigation** - intuitive for older users
- **Quick loading** - maintains engagement
- **Responsive** - Smooth scroll, responsive taps, responsive interactions
- **Layout** - zooming, large fonts display without affecting ability to read/view content
- **Maintenance** - low maintenance cost. Code is simple, straightforward, modularized to encourage abstraction and reuse.
- **Technology comfort** - simplicity is best. prioritize ease of use over advanced features

## Technical Requirements

### Core Tech Stack

- **React** (Create React App or Vite)
- **React Router DOM** - chapter navigation
- **Tailwind CSS** - mobile-first styling
- **Framer Motion** - smooth animations
- **React Image Gallery** - photo displays
- **Howler.js** - background music
- **React Use Gesture** - mobile touch interactions

## Deliverables Needed from Claude Code

### Design Phase

- [ ] 3-5 different UX/UI concepts for the app layout and flow
- [ ] Design options for photo presentation (gallery, slideshow, timeline, etc.)
- [ ] Letter integration approaches (separate section, mixed with photos, etc.)
- [ ] Mobile interface mockups
- [ ] Typography and color scheme options

### Development Phase

- [ ] Complete functional web app
- [ ] Photo upload and management system
- [ ] Letter input and display system
- [ ] Responsive design implementation
- [ ] Testing across devices

### Deployment Phase

- [ ] Hosting setup and domain configuration
- [ ] Backup and maintenance plan

## Questions for Claude Code to Explore

1. **Photo Organization:** What are the most engaging ways to present 40 years of photos on mobile?
2. **Letter Integration:** How should daughters' letters be woven into the photo experience?
3. **Surprise vs. Participation:** Should parents discover content gradually or see everything at once?
4. **Technical Approach:** What's the simplest tech stack that meets our needs, low dev cost, easy to maintain, and encourages componentization and reusability? Ensure designs are aligned on prior to coding.
5. **Content Display:** What's the most appealing way to present and showcase memories + letters in a way that's heartwarming, clean, modern, fluid, and easy to build/consume/use on mobile? Is it possible to help add captions - what are needed for you to help provide a first draft narration, or provide guiding questions for each daughter to answer.

## Additional Context

## Important Notes for Implementation

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
