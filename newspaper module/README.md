# Newspaper Module Animation Demo

A minimal HTML reference demonstrating popup animations for a newspaper module interface.

## Features

### Bottom Navigation
- **Location** (left) - Select newspaper edition/city
- **Pages** (center) - Browse through newspaper pages  
- **Calendar** (right) - Pick a publication date

### Animation Behavior

**All menus slide up from behind the bottom navigation bar** with a smooth 0.3-second animation.

**Animation Specifications:**
- **Duration**: 0.3 seconds
- **Easing**: `cubic-bezier(0.25, 0.46, 0.45, 0.94)` (smooth ease-out)
- **Transform**: `translateY(100%)` to `translateY(-60px)`
- **Initial State**: Hidden below screen edge
- **Active State**: Visible 60px above bottom navigation
- **Z-Index**: Menus (350) slide behind bottom nav (400), above overlay (200)

#### Location Menu
- Slides from behind left side of bottom nav
- Displays list of available cities/editions
- Hover effects on menu items

#### Pages Menu  
- Slides from behind center of bottom nav
- Horizontal scrollable page thumbnails
- Left/right arrow navigation
- Page labels below thumbnails

#### Calendar Menu
- Slides from behind right side of bottom nav  
- Standard calendar grid layout
- Current date highlighted

### Interaction

**Opening Menus:**
- Click any bottom navigation button

**Closing Menus:**
- Click outside menu (on dark overlay)
- Click on empty bottom navigation area
- Click on different navigation button
- Press Escape key
- Click close button (X)

**Within Menus:**
- **Pages**: Use arrow buttons or scroll horizontally
- **Location**: Click any city to select
- **Calendar**: Click any date to select

### Visual Design
- Semi-transparent dark overlay when menus are open
- Rounded top corners on all popups
- Smooth slide animations from bottom edge
- Active button highlighting (red background)

---

*This demo serves as an animation reference for implementing similar popup behaviors in newspaper/content modules.*