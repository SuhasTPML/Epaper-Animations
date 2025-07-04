# Sticky Bottom Bar Animation - Feature Documentation

## Overview
A responsive sticky bottom bar that slides in from the bottom of the screen when a user selects a subscription plan. This provides a persistent call-to-action while maintaining the current page context.

## Feature Behavior

### Trigger Conditions
- **Plan Selection**: Bar automatically slides in when user clicks on any subscription plan card
- **Manual Toggle**: Demo button provided for testing the animation
- **State Persistence**: Bar remains visible until dismissed or page reload

### Animation Characteristics
- **Duration**: 0.3 seconds
- **Easing**: `ease-in-out` for smooth acceleration and deceleration
- **Direction**: Slides up from bottom (translateY: 100% → 0%)
- **Initial State**: Hidden below viewport (`transform: translateY(100%)`)
- **Active State**: Fully visible at bottom of screen (`transform: translateY(0)`)

### Visual Behavior
- **Positioning**: Fixed to bottom of viewport, spans full width
- **Z-index**: 1000 (appears above other content)
- **Shadow**: Subtle drop shadow for depth (`box-shadow: 0 -2px 10px rgba(0,0,0,0.1)`)
- **Background**: White with subtle shadow separation from content

## Content Updates
- **Dynamic Text**: Plan name and pricing update based on selection
- **Selection Feedback**: Selected plan card highlights with green border and background
- **Action Button**: "Review & Pay" button remains consistent

## Technical Implementation

### CSS Classes
- `.sticky-bottom-bar` - Base styling and hidden state
- `.sticky-bottom-bar.show` - Visible state with transform animation
- `.plan-card.selected` - Visual feedback for selected plan

### JavaScript Functions
- `selectPlan(element)` - Handles plan selection and bar activation
- `toggleStickyBar()` - Manual toggle for demonstration purposes

### Browser Compatibility
- Uses CSS transforms and transitions (IE10+)
- Flexbox layout for content arrangement
- Fixed positioning for sticky behavior

## Usage Instructions

### Testing the Animation
1. Open `sticky-bar-animation.html` in a web browser
2. Click on any subscription plan card to trigger the slide-in
3. Use "Toggle Plan Selection" button to manually show/hide
4. Observe smooth 0.3s animation timing

### Integration Notes
- Ensure adequate bottom padding on main content (100px recommended)
- Consider mobile viewport height when positioning
- Test with varying content lengths to ensure no overlap

## Customization Options

### Animation Timing
```css
transition: transform 0.3s ease-in-out;
```
- Adjust `0.3s` for different speeds
- Change easing function for different feel (`ease`, `linear`, `cubic-bezier()`)

### Visual Styling
- Modify `box-shadow` for different depth effects
- Adjust `background` color for brand consistency
- Update `padding` for different content spacing

### Trigger Behavior
- Add additional trigger conditions in JavaScript
- Implement auto-hide functionality based on scroll position
- Add dismiss button functionality

## Performance Considerations
- Uses CSS transforms for hardware acceleration
- Minimal JavaScript for state management
- Lightweight implementation with no external dependencies

## Related Documentation
- **Main Overview**: See `README.md` for project overview and comparison
- **Bottom Sheet**: See `README-bottom-sheet.md` for modal alternative