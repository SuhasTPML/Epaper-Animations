# Bottom Sheet Animation - Feature Documentation

## Overview
A modal bottom sheet that slides up from the bottom of the screen when a user selects a subscription plan. This provides a detailed view of the selected plan with full plan information while maintaining an overlay that dims the background content.

## Feature Behavior

### Trigger Conditions
- **Plan Selection**: Sheet automatically slides up when user clicks "Select Plan" on any subscription plan card
- **Manual Toggle**: Demo button provided for testing the animation
- **Modal Behavior**: Operates as a modal overlay requiring explicit dismissal

### Dismissal Methods
- **Close Button**: X button in top-right corner of sheet
- **Overlay Click**: Clicking on the dimmed background area
- **Escape Key**: Pressing ESC key on keyboard
- **Programmatic**: JavaScript function call

### Animation Characteristics
- **Duration**: 0.3 seconds
- **Easing**: `ease-in-out` for smooth acceleration and deceleration
- **Direction**: Slides up from bottom (translateY: 100% → 0%)
- **Initial State**: Hidden below viewport (`transform: translateY(100%)`)
- **Active State**: Visible as modal sheet (`transform: translateY(0)`)
- **Overlay Fade**: Semi-transparent backdrop fades in simultaneously

### Visual Behavior
- **Positioning**: Fixed to bottom of viewport, spans full width
- **Z-index**: 1000 (sheet above overlay at 999)
- **Background**: White with rounded top corners (16px border-radius)
- **Shadow**: Prominent drop shadow for depth (`box-shadow: 0 -4px 20px rgba(0,0,0,0.1)`)
- **Max Height**: 70vh to prevent full-screen takeover
- **Backdrop**: Semi-transparent dark overlay (rgba(0,0,0,0.5))

## Content Updates
- **Dynamic Text**: Plan name, subtitle, and pricing update based on selection
- **Plan Details**: Shows comprehensive plan information and features
- **Action Button**: "Review & Pay" button for proceeding with selection
- **Feature List**: Displays plan benefits with checkmark styling

## Technical Implementation

### CSS Classes
- `.bottom-sheet` - Base styling and hidden state
- `.bottom-sheet.show` - Visible state with transform animation
- `.overlay` - Semi-transparent backdrop
- `.overlay.show` - Visible overlay state

### JavaScript Functions
- `openBottomSheet(planName, price, subtitle)` - Shows sheet with plan details
- `closeBottomSheet()` - Hides sheet and overlay
- `toggleBottomSheet()` - Manual toggle for demonstration purposes

### User Experience Features
- **Scroll Prevention**: Disables body scrolling when sheet is open
- **Keyboard Navigation**: ESC key support for accessibility
- **Touch-Friendly**: Large close button and overlay click area
- **Content Overflow**: Scrollable content if exceeds max-height

### Browser Compatibility
- Uses CSS transforms and transitions (IE10+)
- Flexbox layout for content arrangement
- Fixed positioning for modal behavior
- Backdrop-filter not used for broader compatibility

## Usage Instructions

### Testing the Animation
1. Open `bottom-sheet-animation.html` in a web browser
2. Click "Select Plan" on any subscription plan card to trigger the sheet
3. Use "Toggle Bottom Sheet" button to manually show/hide
4. Test dismissal methods: close button, overlay click, ESC key
5. Observe smooth 0.3s animation timing and backdrop dimming

### Integration Notes
- Ensure proper z-index hierarchy for overlay layers
- Test with varying content lengths for scroll behavior
- Consider mobile viewport height for sheet sizing
- Implement proper focus management for accessibility

## Customization Options

### Animation Timing
```css
transition: transform 0.3s ease-in-out;
```
- Adjust `0.3s` for different speeds
- Change easing function for different feel (`ease`, `linear`, `cubic-bezier()`)

### Visual Styling
- Modify `max-height: 70vh` for different sheet sizes
- Adjust `border-radius: 16px 16px 0 0` for corner styling
- Update overlay opacity `rgba(0,0,0,0.5)` for backdrop intensity
- Customize `box-shadow` for different depth effects

### Content Layout
- Modify `.sheet-header` for different header arrangements
- Adjust `.features` styling for different list presentations
- Update button styling for brand consistency

### Dismissal Behavior
- Add swipe-down gesture support
- Implement auto-dismiss on outside interaction
- Add confirmation dialogs for accidental dismissal

## Accessibility Considerations
- **Keyboard Navigation**: ESC key support included
- **Focus Management**: Consider trapping focus within sheet
- **Screen Readers**: Ensure proper ARIA labels and roles
- **Reduced Motion**: Consider `prefers-reduced-motion` media query

## Performance Considerations
- Uses CSS transforms for hardware acceleration
- Minimal JavaScript for state management
- Efficient overlay implementation with single DOM element
- No external dependencies for lightweight implementation
