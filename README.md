# Border Animated - Animated Border Component

A custom animated border component built with React and CSS. Features smooth animations, customizable styles, and interactive effects.

## Features

- Animated borders
- Smooth transitions
- Customizable colors
- Interactive hover effects
- Responsive design
- CSS-based animations
- Multiple animation styles
- Lightweight and fast

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/Jewel-190237/border-animated.git
   ```

2. Copy `animation.tsx` and `global.css` into your project

3. Import and use the component:
   ```tsx
   import AnimatedBorder from './animation';

   function App() {
     return (
       <AnimatedBorder>
         <div>Your content here</div>
       </AnimatedBorder>
     );
   }
   ```

## Usage

### Basic Usage
```tsx
import AnimatedBorder from './animation';

function App() {
  return (
    <AnimatedBorder>
      <div style={{ padding: '20px' }}>
        <h2>Animated Border Card</h2>
        <p>This card has an animated border effect</p>
      </div>
    </AnimatedBorder>
  );
}
```

### Different Animation Types
```tsx
// Gradient animation
<AnimatedBorder animation="gradient">
  <div>Gradient Border</div>
</AnimatedBorder>

// Pulse animation
<AnimatedBorder animation="pulse">
  <div>Pulse Border</div>
</AnimatedBorder>

// Rotate animation
<AnimatedBorder animation="rotate">
  <div>Rotate Border</div>
</AnimatedBorder>
```

### Custom Colors
```tsx
<AnimatedBorder
  color="#007bff"
  hoverColor="#0056b3"
  gradientColors={['#007bff', '#00ff88', '#007bff']}
>
  <div>Custom Colored Border</div>
</AnimatedBorder>
```

### Custom Styling
```css
/* Override default styles */
.animated-border {
  position: relative;
  border-radius: 12px;
  overflow: hidden;
}

.animated-border::before {
  content: '';
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  border: 2px solid transparent;
  border-radius: 12px;
  animation: borderRotate 3s linear infinite;
}

@keyframes borderRotate {
  0% {
    border-color: #007bff;
  }
  33% {
    border-color: #00ff88;
  }
  66% {
    border-color: #ff0088;
  }
  100% {
    border-color: #007bff;
  }
}
```

### Interactive Effects
```tsx
<AnimatedBorder
  interactive
  hoverScale={1.02}
  clickEffect
>
  <div>Interactive Border</div>
</AnimatedBorder>
```

## Props

| Prop | Type | Default | Description |
|------|------|---------|-------------|
| animation | string | 'gradient' | Animation type |
| color | string | '#007bff' | Default border color |
| hoverColor | string | - | Hover state color |
| gradientColors | array | ['#007bff', '#00ff88'] | Gradient colors |
| interactive | boolean | false | Enable interactive effects |
| hoverScale | number | 1 | Hover scale effect |
| clickEffect | boolean | false | Click animation |
| children | node | - | Content to wrap |

## Features in Detail

### Animation Types
- **Gradient**: Smooth color transitions
- **Pulse**: Pulsing border effect
- **Rotate**: Rotating border segments
- **Wave**: Wave-like border movement

### Interactive Effects
- Hover color changes
- Click animations
- Scale on hover
- Focus states

### Customization
- Any CSS color
- Custom animation durations
- Different border widths
- Various border styles

## Author

**Jewel-190237**
- GitHub: [Jewel-190237](https://github.com/Jewel-190237)
- Email: jewel190237@gmail.com

## Contributing

Feel free to fork this project and create pull requests for any improvements.

## License

This project is open source and available under the [MIT License](LICENSE).
