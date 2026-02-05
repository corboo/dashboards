# IPAI Design System
*Apple/iOS-inspired • Glassmorphism • Silver→Gold Gradient*

## Brand Colors

```css
:root {
    /* Backgrounds */
    --bg-primary: #2d2d2d;      /* Main background */
    --bg-secondary: #3a3a3a;    /* Elevated surfaces */
    --bg-tertiary: #454545;     /* Highest elevation */
    
    /* Brand Gradient (from logo) */
    --silver: #a8a8a8;
    --silver-light: #c5c5c5;
    --gold: #d4af37;
    --gold-light: #e8c547;
    --gold-bright: #f5d742;
    
    /* Text */
    --text-primary: #ffffff;
    --text-secondary: rgba(255, 255, 255, 0.7);
    --text-tertiary: rgba(255, 255, 255, 0.5);
    
    /* Glass Effect */
    --glass-bg: rgba(255, 255, 255, 0.05);
    --glass-border: rgba(255, 255, 255, 0.1);
    --glass-hover: rgba(255, 255, 255, 0.08);
    
    /* Status Colors */
    --status-live: #34c759;     /* Green */
    --status-warning: #ff9f0a;  /* Orange */
    --status-error: #ff453a;    /* Red */
}
```

## Typography

- **Font Family:** Inter (fallback: -apple-system, BlinkMacSystemFont, SF Pro)
- **Font Smoothing:** antialiased
- **Letter Spacing:** Tight for headings (-0.02em to -0.03em)

### Scale
| Element | Size | Weight | Spacing |
|---------|------|--------|---------|
| H1 | 2.5-3rem | 700 | -0.03em |
| H2 | 1.375rem | 600 | -0.02em |
| Body | 0.875-1rem | 400 | normal |
| Caption | 0.75rem | 500 | 0.05em (uppercase) |
| Tag | 0.6875rem | 500 | normal |

## Components

### Glass Card
```css
.card {
    background: rgba(255, 255, 255, 0.05);
    backdrop-filter: blur(20px);
    -webkit-backdrop-filter: blur(20px);
    border-radius: 16px;
    border: 1px solid rgba(255, 255, 255, 0.1);
    padding: 24px;
    transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
}

.card:hover {
    background: rgba(255, 255, 255, 0.08);
    border-color: rgba(212, 175, 55, 0.3);
    transform: translateY(-4px);
    box-shadow: 0 20px 40px rgba(0, 0, 0, 0.3);
}
```

### Featured Card (Gold Accent)
```css
.card.featured {
    background: linear-gradient(135deg, rgba(212, 175, 55, 0.1) 0%, rgba(168, 168, 168, 0.05) 100%);
    border-color: rgba(212, 175, 55, 0.3);
}
```

### Gradient Text (Headings)
```css
.gradient-text {
    background: linear-gradient(180deg, #c5c5c5 0%, #d4af37 100%);
    -webkit-background-clip: text;
    -webkit-text-fill-color: transparent;
    background-clip: text;
}
```

### Status Indicator
```css
.status-dot {
    width: 8px;
    height: 8px;
    border-radius: 50%;
    background: #34c759;
    box-shadow: 0 0 8px rgba(52, 199, 89, 0.5);
}
```

### Background Gradient Overlay
```css
.bg-gradient {
    position: fixed;
    top: 0; left: 0; right: 0; bottom: 0;
    background: 
        radial-gradient(ellipse at 20% 20%, rgba(168, 168, 168, 0.08) 0%, transparent 50%),
        radial-gradient(ellipse at 80% 80%, rgba(212, 175, 55, 0.06) 0%, transparent 50%),
        #2d2d2d;
    z-index: -1;
}
```

## Spacing

- **Container max-width:** 1000-1200px
- **Section margin:** 40-56px
- **Card padding:** 20-24px
- **Card gap:** 12-16px
- **Border radius:** 14-16px (cards), 10-12px (icons), 4-6px (tags)

## Animation

- **Easing:** cubic-bezier(0.4, 0, 0.2, 1)
- **Duration:** 0.25-0.3s
- **Hover lift:** translateY(-2px) to translateY(-4px)

## Logo Usage

- Display at 72-80px in header
- Border radius: 16-18px
- Box shadow: 0 8px 32px rgba(0, 0, 0, 0.3)
- File: `ipai-logo.jpg`

## Dark Mode Only

This design system is dark mode by default. The charcoal background with silver→gold accents creates an elegant, premium feel that aligns with IPAI branding.

---

*Created by CB for Inception Point AI • February 2026*
