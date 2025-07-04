# Article Reader Animation Demo

A minimal HTML reference demonstrating article reader slide-up animations and bottom navigation transitions for newspaper/content applications.

## Features

### Main Views
- **Newspaper Module** - Grid layout with article cards
- **Article Reader** - Full-screen article view with reading controls
- **Bottom Navigation** - Context-sensitive controls for each view

### Animation Behavior

**Article reader slides up from bottom** with a fast 0.2-second animation.

**Animation Specifications:**
- **Duration**: 0.2 seconds
- **Easing**: `cubic-bezier(0.25, 0.46, 0.45, 0.94)` (smooth ease-out)
- **Transform**: `translateY(100%)` to `translateY(0)`
- **Background**: Scales to 95% and dims during article reading
- **Z-Index**: Article reader (1000) above overlay (500) above newspaper (base)

#### Opening Article
- Click any article card in newspaper view
- Background scales down (95%) and dims
- Semi-transparent overlay appears
- Article reader slides up from bottom edge
- Newspaper bottom nav slides down and hides
- Article bottom nav slides up after article appears

#### Article Reader Layout
- Sticky header with back button and action controls
- Full-screen scrollable article content
- Context-sensitive bottom navigation
- Professional typography and spacing

### Bottom Navigation

**Newspaper Navigation:**
- **Location** - "Bengaluru City ⌄" (city/edition selector)
- **Pages** - "01 Front Page ⌄" (page navigation)
- **Date** - "4 Jul 📅" (date picker)

**Article Navigation:**
- **A-** - Decrease text size
- **A+** - Increase text size  
- **🗋** - Print article
- **🔊** - Listen (text-to-speech)
- **📤** - Share article

### Interaction

**Opening Articles:**
- Click any article card in the newspaper grid

**Closing Articles:**
- Click back button (← Back) in article header
- Click close button (✕) in article header
- Click outside article (on dark overlay)
- Press Escape key

**Within Articles:**
- Scroll to read full content
- Use bottom navigation for text controls, print, listen, share
- Sticky header remains accessible while scrolling

### Visual Design
- **Smooth transitions** between newspaper and article views
- **Context-aware navigation** that switches based on current view
- **Professional typography** optimized for reading
- **Mobile-first design** with touch-friendly controls
- **Overlay dimming** to focus attention on article content
- **Responsive layout** that works across screen sizes

### Technical Details
- **No external dependencies** - Pure HTML, CSS, and JavaScript
- **Smooth animations** using CSS transforms and transitions
- **Event handling** for multiple interaction methods
- **Content management** with JavaScript article data structure
- **Visual feedback** on all interactive elements

---

*This demo serves as an animation reference for implementing article reader functionality in news, blog, or content management applications.*