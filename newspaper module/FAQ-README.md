# FAQ Expand/Collapse Animation

A clean, interactive FAQ component with smooth expand/collapse animations for newspaper applications.

## Features

### Animation Behavior

**Smooth height transitions** with a 0.3-second animation for expanding and collapsing FAQ items.

**Animation Specifications:**
- **Duration**: 0.3 seconds
- **Easing**: `ease` (default CSS easing)
- **Property**: `max-height` transition from 0 to content height
- **Visual Feedback**: Background color change on active items
- **Icon Rotation**: Plus/minus icon transitions

### Interaction

**Expanding FAQ Items:**
- Click any question to expand its answer
- Smooth animation reveals content
- Question background changes to blue
- Plus icon changes to minus

**Collapsing FAQ Items:**
- Click the expanded question again to collapse
- Click a different question to switch to that FAQ (accordion behavior)
- Smooth animation hides content
- Background returns to original color
- Minus icon changes to plus

### Visual Design
- Clean, modern interface with subtle shadows
- Blue highlight for active FAQ items
- Plus/minus icons for visual indication
- Proper spacing and typography for readability
- Responsive design that works on all screen sizes
- Hover effects on questions for better UX

### Technical Details
- **No external dependencies** - Pure HTML, CSS, and JavaScript
- **Accordion behavior** - Only one FAQ item open at a time
- **Accessible** - Proper semantic HTML structure
- **Efficient** - Uses CSS transitions for optimal performance
- **Cross-browser compatible** - Works on all modern browsers

## Usage Instructions

1. **Adding New FAQ Items**:
   ```html
   <div class="faq-item">
       <div class="faq-question">Your question here</div>
       <div class="faq-answer">
           <div class="faq-answer-content">
               <p>Your answer content here</p>
           </div>
       </div>
   </div>
   ```

2. **Customizing Styles**:
   - Modify colors in the CSS variables section
   - Adjust timing by changing the `transition` durations
   - Update spacing by modifying padding/margin values

3. **JavaScript Behavior**:
   - The script automatically handles all interaction
   - To allow multiple FAQs open simultaneously, remove the loop that closes other items
   - To change the animation speed, update both the CSS and JS timing values

## Customization Options

### Colors
```css
.faq-question:hover {
    background: #e9ecef; /* Hover background */
}

.faq-item.active .faq-question {
    background: #3498db; /* Active background */
    color: white;        /* Active text color */
}
```

### Animation Timing
```css
.faq-answer {
    transition: max-height 0.3s ease, padding 0.3s ease;
}
```

### Spacing
```css
.faq-question {
    padding: 15px 20px; /* Question padding */
}

.faq-answer-content {
    padding: 0 20px 0 20px; /* Answer padding */
}

.faq-item.active .faq-answer {
    padding: 10px 0 20px 0; /* Expanded answer padding */
}
```