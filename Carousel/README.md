# DH Carousel Component

A responsive, touch-enabled carousel component showcasing "Why Choose DH?" value propositions with autoscroll functionality.

## 📁 Files

- `why choose dh.html` - Main carousel implementation
- `index.html` - Alternative version (without autoscroll)
- `README.md` - This documentation

## 🎯 Features

### Core Functionality
- **Responsive Design**: 3 cards visible on desktop, 1 card on mobile
- **One-by-One Navigation**: Smooth transitions showing adjacent cards
- **Touch/Swipe Support**: Native mobile gesture navigation
- **Keyboard Navigation**: Arrow keys for accessibility
- **Hover Effects**: Cards scale and enhance shadows on hover
- **Pagination Dots**: Visual indicators with pill-shaped active state

### Autoscroll System
- **Toggle Control**: Start/pause autoscroll with visual button
- **Timer Display**: Real-time countdown showing next transition
- **Smart Pausing**: Auto-pauses on hover (desktop) and touch (mobile)
- **Manual Override**: User interactions reset the timer
- **Seamless Integration**: Works with all existing navigation methods

## 🖥️ Desktop Behavior

### Navigation
- **Arrow Buttons**: Left/right navigation arrows visible
- **3 Cards Visible**: Shows cards in groups of three
- **4 Slide Positions**: 
  - Position 1: Cards 1, 2, 3
  - Position 2: Cards 2, 3, 4
  - Position 3: Cards 3, 4, 5
  - Position 4: Cards 4, 5, 6

### Autoscroll
- **Hover-Pause**: Autoscroll pauses when mouse hovers over carousel
- **Auto-Resume**: Resumes when mouse leaves carousel area
- **Manual Reset**: Arrow clicks or dot clicks reset 5-second timer

## 📱 Mobile Behavior

### Navigation
- **No Arrow Buttons**: Hidden for cleaner mobile interface
- **Swipe Gestures**: Left/right swipes navigate cards
- **1 Card Visible**: Full-width single card display
- **6 Slide Positions**: One position per card

### Touch-Pause System
- **Touch to Pause**: Autoscroll pauses immediately when user touches carousel
- **Smart Resume**: 
  - **Swipe detected**: Navigate + reset timer
  - **Just tap**: Resume autoscroll when finger lifts
- **Interruption Handling**: Properly handles calls, notifications, etc.

## 🎛️ Controls Reference

### Autoscroll Toggle Button
```
▶ Start Auto-scroll  (Blue - Ready to start)
⏸ Pause Auto-scroll  (Red - Currently running)
```

### Timer Display
```
Next: 5s  (Countdown when running)
Auto-scroll: OFF  (When stopped)
```

### Navigation Methods
1. **Arrow Buttons** (Desktop only)
2. **Pagination Dots** (All devices)
3. **Swipe Gestures** (Mobile)
4. **Keyboard Arrows** (Desktop)
5. **Autoscroll** (All devices)
