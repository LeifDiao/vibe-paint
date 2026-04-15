# vibe-paint — Complete Style Token Reference

This file contains the complete design token data for all 30 vibe-paint styles.
When applying a style, find the matching section below and use its tokens as the replacement values.

## Table of Contents

- [Clean Minimal](#clean-minimal)
- [Corporate Professional](#corporate-professional)
- [Dashboard Data Dense](#dashboard-data-dense)
- [Ecommerce Modern](#ecommerce-modern)
- [Mobile First Gesture](#mobile-first-gesture)
- [Glassmorphism](#glassmorphism)
- [Neumorphism](#neumorphism)
- [Claymorphism](#claymorphism)
- [Aurora Gradient](#aurora-gradient)
- [Bento Grid](#bento-grid)
- [Neo Brutalism](#neo-brutalism)
- [Cyberpunk Neon](#cyberpunk-neon)
- [Swiss Typography](#swiss-typography)
- [Art Deco](#art-deco)
- [Isometric Playful](#isometric-playful)
- [Editorial Monochrome](#editorial-monochrome)
- [Y2k Futurism](#y2k-futurism)
- [Vaporwave](#vaporwave)
- [Synthwave](#synthwave)
- [Pixel Retro](#pixel-retro)
- [Skeuomorphic](#skeuomorphic)
- [Terminal Hacker](#terminal-hacker)
- [Warm Soft](#warm-soft)
- [Organic Earth](#organic-earth)
- [Zen Wabi Sabi](#zen-wabi-sabi)
- [Dark Premium](#dark-premium)
- [Candy Pop](#candy-pop)
- [Anime Gacha](#anime-gacha)
- [Grunge Underground](#grunge-underground)
- [Holographic Futurism](#holographic-futurism)

---

## Clean Minimal

**Slug:** `clean-minimal` | **Category:** Professional & Functional | **Font:** Inter

### Colors
| Token | Value |
|-------|-------|
| `--color-white` | `#ffffff` |
| `--color-surface-light` | `#f9fafb` |
| `--color-surface` | `#f3f4f6` |
| `--color-text` | `#111827` |
| `--color-text-secondary` | `#6b7280` |
| `--color-text-tertiary` | `#9ca3af` |
| `--color-primary` | `#6366f1` |
| `--color-primary-light` | `#eef2ff` |
| `--color-primary-dark` | `#4f46e5` |
| `--color-secondary` | `#64748b` |
| `--color-secondary-light` | `#f1f5f9` |
| `--color-border` | `#e5e7eb` |
| `--color-border-light` | `#f3f4f6` |
| `--color-success` | `#22c55e` |
| `--color-warning` | `#f59e0b` |
| `--color-error` | `#ef4444` |
| `--color-info` | `#3b82f6` |

### Typography
| Token | Value |
|-------|-------|
| `--font-family` | `'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif` |
| `--transition` | `all 150ms ease-in-out` |

### Border Radius
| Token | Value |
|-------|-------|
| `--radius-xs` | `2px` |
| `--radius-sm` | `4px` |
| `--radius-default` | `6px` |
| `--radius-md` | `8px` |
| `--radius-lg` | `12px` |
| `--radius-full` | `9999px` |

### Shadows
| Token | Value |
|-------|-------|
| `--shadow-xs` | `0 1px 2px rgba(0, 0, 0, 0.05)` |
| `--shadow-sm` | `0 1px 3px rgba(0, 0, 0, 0.08)` |
| `--shadow-md` | `0 4px 6px rgba(0, 0, 0, 0.1)` |
| `--shadow-lg` | `0 8px 12px rgba(0, 0, 0, 0.08), 0 12px 20px rgba(0, 0, 0, 0.1), 0 16px 32px rgba(0, 0, 0, 0.08)` |
| `--shadow-xl` | `0 12px 24px rgba(0, 0, 0, 0.1), 0 20px 40px rgba(0, 0, 0, 0.12), 0 28px 60px rgba(0, 0, 0, 0.1)` |

### CSS Variables (copy-paste ready)
```css
:root {
  --color-white: #ffffff;
  --color-surface-light: #f9fafb;
  --color-surface: #f3f4f6;
  --color-text: #111827;
  --color-text-secondary: #6b7280;
  --color-text-tertiary: #9ca3af;
  --color-primary: #6366f1;
  --color-primary-light: #eef2ff;
  --color-primary-dark: #4f46e5;
  --color-secondary: #64748b;
  --color-secondary-light: #f1f5f9;
  --color-border: #e5e7eb;
  --color-border-light: #f3f4f6;
  --color-success: #22c55e;
  --color-warning: #f59e0b;
  --color-error: #ef4444;
  --color-info: #3b82f6;
  --transition: all 150ms ease-in-out;
  --font: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
  --radius-xs: 2px;
  --radius-sm: 4px;
  --radius-default: 6px;
  --radius-md: 8px;
  --radius-lg: 12px;
  --radius-full: 9999px;
  --shadow-xs: 0 1px 2px rgba(0, 0, 0, 0.05);
  --shadow-sm: 0 1px 3px rgba(0, 0, 0, 0.08);
  --shadow-md: 0 4px 6px rgba(0, 0, 0, 0.1);
  --shadow-lg: 0 8px 12px rgba(0, 0, 0, 0.08), 0 12px 20px rgba(0, 0, 0, 0.1), 0 16px 32px rgba(0, 0, 0, 0.08);
  --shadow-xl: 0 12px 24px rgba(0, 0, 0, 0.1), 0 20px 40px rgba(0, 0, 0, 0.12), 0 28px 60px rgba(0, 0, 0, 0.1);
}
```

### Tailwind Config
```js
// tailwind.config.js theme.extend
{
  colors: {
    'white': '#ffffff',
    'surface-light': '#f9fafb',
    'surface': '#f3f4f6',
    'text': '#111827',
    'text-secondary': '#6b7280',
    'text-tertiary': '#9ca3af',
    'primary': '#6366f1',
    'primary-light': '#eef2ff',
    'primary-dark': '#4f46e5',
    'secondary': '#64748b',
    'secondary-light': '#f1f5f9',
    'border': '#e5e7eb',
    'border-light': '#f3f4f6',
    'success': '#22c55e',
    'warning': '#f59e0b',
    'error': '#ef4444',
    'info': '#3b82f6',
  },
  borderRadius: {
    'xs': '2px',
    'sm': '4px',
    'default': '6px',
    'md': '8px',
    'lg': '12px',
    'full': '9999px',
  },
  boxShadow: {
    'xs': '0 1px 2px rgba(0, 0, 0, 0.05)',
    'sm': '0 1px 3px rgba(0, 0, 0, 0.08)',
    'md': '0 4px 6px rgba(0, 0, 0, 0.1)',
    'lg': '0 8px 12px rgba(0, 0, 0, 0.08), 0 12px 20px rgba(0, 0, 0, 0.1), 0 16px 32px rgba(0, 0, 0, 0.08)',
    'xl': '0 12px 24px rgba(0, 0, 0, 0.1), 0 20px 40px rgba(0, 0, 0, 0.12), 0 28px 60px rgba(0, 0, 0, 0.1)',
  },
  fontFamily: {
    sans: ['Inter', 'system-ui', 'sans-serif'],
  },
}
```

---

## Corporate Professional

**Slug:** `corporate-professional` | **Category:** Professional & Functional | **Font:** Source Sans Pro

### Colors
| Token | Value |
|-------|-------|
| `--color-white` | `#ffffff` |
| `--color-surface-light` | `#f5f7fa` |
| `--color-surface` | `#eef2f7` |
| `--color-text` | `#0f1419` |
| `--color-text-secondary` | `#3d4555` |
| `--color-text-tertiary` | `#6b7684` |
| `--color-primary` | `#1B5E9E` |
| `--color-primary-light` | `#e6f0f7` |
| `--color-primary-dark` | `#0d3a5e` |
| `--color-secondary` | `#2C3E50` |
| `--color-secondary-light` | `#e8ecf2` |
| `--color-border` | `#c5cbd4` |
| `--color-border-light` | `#dfe3ec` |
| `--color-success` | `#059669` |
| `--color-warning` | `#d97706` |
| `--color-error` | `#dc2626` |
| `--color-info` | `#2563eb` |
| `--color-accent` | `#E67E22` |

### Typography
| Token | Value |
|-------|-------|
| `--font-family` | `'Source Sans Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif` |
| `--transition` | `all 150ms ease-in-out` |

### Border Radius
| Token | Value |
|-------|-------|
| `--radius-xs` | `2px` |
| `--radius-sm` | `3px` |
| `--radius-default` | `3px` |
| `--radius-md` | `4px` |
| `--radius-lg` | `4px` |
| `--radius-full` | `9999px` |

### Shadows
| Token | Value |
|-------|-------|
| `--shadow-xs` | `0 1px 2px rgba(0, 0, 0, 0.04)` |
| `--shadow-sm` | `0 1px 2px rgba(0, 0, 0, 0.08)` |
| `--shadow-md` | `0 2px 4px rgba(0, 0, 0, 0.1)` |
| `--shadow-lg` | `0 4px 8px rgba(0, 0, 0, 0.12)` |
| `--shadow-xl` | `0 8px 12px rgba(0, 0, 0, 0.14)` |

### CSS Variables (copy-paste ready)
```css
:root {
  --color-white: #ffffff;
  --color-surface-light: #f5f7fa;
  --color-surface: #eef2f7;
  --color-text: #0f1419;
  --color-text-secondary: #3d4555;
  --color-text-tertiary: #6b7684;
  --color-primary: #1B5E9E;
  --color-primary-light: #e6f0f7;
  --color-primary-dark: #0d3a5e;
  --color-secondary: #2C3E50;
  --color-secondary-light: #e8ecf2;
  --color-border: #c5cbd4;
  --color-border-light: #dfe3ec;
  --color-success: #059669;
  --color-warning: #d97706;
  --color-error: #dc2626;
  --color-info: #2563eb;
  --color-accent: #E67E22;
  --transition: all 150ms ease-in-out;
  --font: 'Source Sans Pro', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
  --radius-xs: 2px;
  --radius-sm: 3px;
  --radius-default: 3px;
  --radius-md: 4px;
  --radius-lg: 4px;
  --radius-full: 9999px;
  --shadow-xs: 0 1px 2px rgba(0, 0, 0, 0.04);
  --shadow-sm: 0 1px 2px rgba(0, 0, 0, 0.08);
  --shadow-md: 0 2px 4px rgba(0, 0, 0, 0.1);
  --shadow-lg: 0 4px 8px rgba(0, 0, 0, 0.12);
  --shadow-xl: 0 8px 12px rgba(0, 0, 0, 0.14);
}
```

### Tailwind Config
```js
// tailwind.config.js theme.extend
{
  colors: {
    'white': '#ffffff',
    'surface-light': '#f5f7fa',
    'surface': '#eef2f7',
    'text': '#0f1419',
    'text-secondary': '#3d4555',
    'text-tertiary': '#6b7684',
    'primary': '#1B5E9E',
    'primary-light': '#e6f0f7',
    'primary-dark': '#0d3a5e',
    'secondary': '#2C3E50',
    'secondary-light': '#e8ecf2',
    'border': '#c5cbd4',
    'border-light': '#dfe3ec',
    'success': '#059669',
    'warning': '#d97706',
    'error': '#dc2626',
    'info': '#2563eb',
    'accent': '#E67E22',
  },
  borderRadius: {
    'xs': '2px',
    'sm': '3px',
    'default': '3px',
    'md': '4px',
    'lg': '4px',
    'full': '9999px',
  },
  boxShadow: {
    'xs': '0 1px 2px rgba(0, 0, 0, 0.04)',
    'sm': '0 1px 2px rgba(0, 0, 0, 0.08)',
    'md': '0 2px 4px rgba(0, 0, 0, 0.1)',
    'lg': '0 4px 8px rgba(0, 0, 0, 0.12)',
    'xl': '0 8px 12px rgba(0, 0, 0, 0.14)',
  },
  fontFamily: {
    sans: ['Source Sans Pro', 'system-ui', 'sans-serif'],
  },
}
```

---

## Dashboard Data Dense

**Slug:** `dashboard-data-dense` | **Category:** Professional & Functional | **Font:** Inter

### Colors
| Token | Value |
|-------|-------|
| `--color-white` | `#0F1019` |
| `--color-surface-light` | `#13141F` |
| `--color-surface` | `#1A1B2E` |
| `--color-text` | `#E2E8F0` |
| `--color-text-secondary` | `#9CA3AF` |
| `--color-text-tertiary` | `#6B7280` |
| `--color-primary` | `#7C3AED` |
| `--color-primary-light` | `rgba(124,58,237,0.1)` |
| `--color-primary-dark` | `#5d2bb3` |
| `--color-secondary` | `#3B82F6` |
| `--color-secondary-light` | `rgba(59,130,246,0.1)` |
| `--color-border` | `rgba(255,255,255,0.06)` |
| `--color-border-light` | `rgba(255,255,255,0.03)` |
| `--color-success` | `#22C55E` |
| `--color-warning` | `#F59E0B` |
| `--color-error` | `#EF4444` |
| `--color-info` | `#3B82F6` |

### Typography
| Token | Value |
|-------|-------|
| `--font-family` | `'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif` |
| `--transition` | `all 100ms ease-in-out` |

### Border Radius
| Token | Value |
|-------|-------|
| `--radius-xs` | `2px` |
| `--radius-sm` | `4px` |
| `--radius-default` | `4px` |
| `--radius-md` | `8px` |
| `--radius-lg` | `8px` |
| `--radius-full` | `9999px` |

### Shadows
| Token | Value |
|-------|-------|
| `--shadow-xs` | `0 4px 12px rgba(0,0,0,0.3)` |
| `--shadow-sm` | `0 4px 12px rgba(0,0,0,0.4)` |
| `--shadow-md` | `0 8px 16px rgba(0,0,0,0.5)` |
| `--shadow-lg` | `0 12px 24px rgba(0,0,0,0.6)` |
| `--shadow-xl` | `0 20px 40px rgba(0,0,0,0.7)` |

### CSS Variables (copy-paste ready)
```css
:root {
  --color-white: #0F1019;
  --color-surface-light: #13141F;
  --color-surface: #1A1B2E;
  --color-text: #E2E8F0;
  --color-text-secondary: #9CA3AF;
  --color-text-tertiary: #6B7280;
  --color-primary: #7C3AED;
  --color-primary-light: rgba(124,58,237,0.1);
  --color-primary-dark: #5d2bb3;
  --color-secondary: #3B82F6;
  --color-secondary-light: rgba(59,130,246,0.1);
  --color-border: rgba(255,255,255,0.06);
  --color-border-light: rgba(255,255,255,0.03);
  --color-success: #22C55E;
  --color-warning: #F59E0B;
  --color-error: #EF4444;
  --color-info: #3B82F6;
  --transition: all 100ms ease-in-out;
  --font: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
  --radius-xs: 2px;
  --radius-sm: 4px;
  --radius-default: 4px;
  --radius-md: 8px;
  --radius-lg: 8px;
  --radius-full: 9999px;
  --shadow-xs: 0 4px 12px rgba(0,0,0,0.3);
  --shadow-sm: 0 4px 12px rgba(0,0,0,0.4);
  --shadow-md: 0 8px 16px rgba(0,0,0,0.5);
  --shadow-lg: 0 12px 24px rgba(0,0,0,0.6);
  --shadow-xl: 0 20px 40px rgba(0,0,0,0.7);
}
```

### Tailwind Config
```js
// tailwind.config.js theme.extend
{
  colors: {
    'white': '#0F1019',
    'surface-light': '#13141F',
    'surface': '#1A1B2E',
    'text': '#E2E8F0',
    'text-secondary': '#9CA3AF',
    'text-tertiary': '#6B7280',
    'primary': '#7C3AED',
    'primary-light': 'rgba(124,58,237,0.1)',
    'primary-dark': '#5d2bb3',
    'secondary': '#3B82F6',
    'secondary-light': 'rgba(59,130,246,0.1)',
    'border': 'rgba(255,255,255,0.06)',
    'border-light': 'rgba(255,255,255,0.03)',
    'success': '#22C55E',
    'warning': '#F59E0B',
    'error': '#EF4444',
    'info': '#3B82F6',
  },
  borderRadius: {
    'xs': '2px',
    'sm': '4px',
    'default': '4px',
    'md': '8px',
    'lg': '8px',
    'full': '9999px',
  },
  boxShadow: {
    'xs': '0 4px 12px rgba(0,0,0,0.3)',
    'sm': '0 4px 12px rgba(0,0,0,0.4)',
    'md': '0 8px 16px rgba(0,0,0,0.5)',
    'lg': '0 12px 24px rgba(0,0,0,0.6)',
    'xl': '0 20px 40px rgba(0,0,0,0.7)',
  },
  fontFamily: {
    sans: ['Inter', 'system-ui', 'sans-serif'],
  },
}
```

---

## Ecommerce Modern

**Slug:** `ecommerce-modern` | **Category:** Professional & Functional | **Font:** DM Sans

### Colors
| Token | Value |
|-------|-------|
| `--color-white` | `#ffffff` |
| `--color-surface-light` | `#FAFAFA` |
| `--color-surface` | `#f8f8f8` |
| `--color-text` | `#1A1A1A` |
| `--color-text-secondary` | `#666666` |
| `--color-text-tertiary` | `#999999` |
| `--color-primary` | `#FF5722` |
| `--color-primary-light` | `#FFF3E0` |
| `--color-primary-dark` | `#E64A19` |
| `--color-secondary` | `#1A1A1A` |
| `--color-secondary-light` | `#f5f5f5` |
| `--color-border` | `#E8E8E8` |
| `--color-border-light` | `#f5f5f5` |
| `--color-success` | `#66BB6A` |
| `--color-warning` | `#FFA726` |
| `--color-error` | `#EF5350` |
| `--color-info` | `#42A5F5` |

### Typography
| Token | Value |
|-------|-------|
| `--font-family` | `'DM Sans', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif` |
| `--transition` | `transform 0.3s, box-shadow 0.3s` |

### Border Radius
| Token | Value |
|-------|-------|
| `--radius-xs` | `2px` |
| `--radius-sm` | `8px` |
| `--radius-default` | `12px` |
| `--radius-md` | `12px` |
| `--radius-lg` | `16px` |
| `--radius-full` | `999px` |

### Shadows
| Token | Value |
|-------|-------|
| `--shadow-xs` | `0 2px 8px rgba(0, 0, 0, 0.06)` |
| `--shadow-sm` | `0 2px 8px rgba(0, 0, 0, 0.06)` |
| `--shadow-md` | `0 8px 32px rgba(0, 0, 0, 0.1)` |
| `--shadow-lg` | `0 12px 40px rgba(0, 0, 0, 0.12)` |
| `--shadow-xl` | `0 20px 48px rgba(0, 0, 0, 0.16)` |

### CSS Variables (copy-paste ready)
```css
:root {
  --color-white: #ffffff;
  --color-surface-light: #FAFAFA;
  --color-surface: #f8f8f8;
  --color-text: #1A1A1A;
  --color-text-secondary: #666666;
  --color-text-tertiary: #999999;
  --color-primary: #FF5722;
  --color-primary-light: #FFF3E0;
  --color-primary-dark: #E64A19;
  --color-secondary: #1A1A1A;
  --color-secondary-light: #f5f5f5;
  --color-border: #E8E8E8;
  --color-border-light: #f5f5f5;
  --color-success: #66BB6A;
  --color-warning: #FFA726;
  --color-error: #EF5350;
  --color-info: #42A5F5;
  --transition: transform 0.3s, box-shadow 0.3s;
  --font: 'DM Sans', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
  --radius-xs: 2px;
  --radius-sm: 8px;
  --radius-default: 12px;
  --radius-md: 12px;
  --radius-lg: 16px;
  --radius-full: 999px;
  --shadow-xs: 0 2px 8px rgba(0, 0, 0, 0.06);
  --shadow-sm: 0 2px 8px rgba(0, 0, 0, 0.06);
  --shadow-md: 0 8px 32px rgba(0, 0, 0, 0.1);
  --shadow-lg: 0 12px 40px rgba(0, 0, 0, 0.12);
  --shadow-xl: 0 20px 48px rgba(0, 0, 0, 0.16);
}
```

### Tailwind Config
```js
// tailwind.config.js theme.extend
{
  colors: {
    'white': '#ffffff',
    'surface-light': '#FAFAFA',
    'surface': '#f8f8f8',
    'text': '#1A1A1A',
    'text-secondary': '#666666',
    'text-tertiary': '#999999',
    'primary': '#FF5722',
    'primary-light': '#FFF3E0',
    'primary-dark': '#E64A19',
    'secondary': '#1A1A1A',
    'secondary-light': '#f5f5f5',
    'border': '#E8E8E8',
    'border-light': '#f5f5f5',
    'success': '#66BB6A',
    'warning': '#FFA726',
    'error': '#EF5350',
    'info': '#42A5F5',
  },
  borderRadius: {
    'xs': '2px',
    'sm': '8px',
    'default': '12px',
    'md': '12px',
    'lg': '16px',
    'full': '999px',
  },
  boxShadow: {
    'xs': '0 2px 8px rgba(0, 0, 0, 0.06)',
    'sm': '0 2px 8px rgba(0, 0, 0, 0.06)',
    'md': '0 8px 32px rgba(0, 0, 0, 0.1)',
    'lg': '0 12px 40px rgba(0, 0, 0, 0.12)',
    'xl': '0 20px 48px rgba(0, 0, 0, 0.16)',
  },
  fontFamily: {
    sans: ['DM Sans', 'system-ui', 'sans-serif'],
  },
}
```

---

## Mobile First Gesture

**Slug:** `mobile-first-gesture` | **Category:** Professional & Functional | **Font:** SF Pro Display

### Colors
| Token | Value |
|-------|-------|
| `--color-white` | `#ffffff` |
| `--color-surface-light` | `#F2F2F7` |
| `--color-surface` | `#E9E9EE` |
| `--color-text` | `#1C1C1E` |
| `--color-text-secondary` | `#3C3C43` |
| `--color-text-tertiary` | `#8E8E93` |
| `--color-primary` | `#007AFF` |
| `--color-primary-light` | `#E8F4FF` |
| `--color-primary-dark` | `#0051D5` |
| `--color-secondary` | `#5856D6` |
| `--color-secondary-light` | `#F0ECFF` |
| `--color-border` | `rgba(60,60,67,0.12)` |
| `--color-border-light` | `rgba(60,60,67,0.08)` |
| `--color-success` | `#34C759` |
| `--color-warning` | `#FF9500` |
| `--color-error` | `#FF3B30` |
| `--color-info` | `#30B0C0` |

### Typography
| Token | Value |
|-------|-------|
| `--font-family` | `-apple-system, 'SF Pro Display', 'Helvetica Neue', system-ui, sans-serif` |
| `--transition` | `all 0.3s ease` |

### Border Radius
| Token | Value |
|-------|-------|
| `--radius-xs` | `2px` |
| `--radius-sm` | `8px` |
| `--radius-default` | `12px` |
| `--radius-md` | `16px` |
| `--radius-lg` | `20px` |
| `--radius-full` | `9999px` |

### Shadows
| Token | Value |
|-------|-------|
| `--shadow-xs` | `0 1px 3px rgba(0, 0, 0, 0.04)` |
| `--shadow-sm` | `0 4px 12px rgba(0, 0, 0, 0.06)` |
| `--shadow-md` | `0 8px 24px rgba(0, 0, 0, 0.08)` |
| `--shadow-lg` | `0 12px 32px rgba(0, 0, 0, 0.12)` |
| `--shadow-xl` | `0 16px 48px rgba(0, 0, 0, 0.16)` |

### CSS Variables (copy-paste ready)
```css
:root {
  --color-white: #ffffff;
  --color-surface-light: #F2F2F7;
  --color-surface: #E9E9EE;
  --color-text: #1C1C1E;
  --color-text-secondary: #3C3C43;
  --color-text-tertiary: #8E8E93;
  --color-primary: #007AFF;
  --color-primary-light: #E8F4FF;
  --color-primary-dark: #0051D5;
  --color-secondary: #5856D6;
  --color-secondary-light: #F0ECFF;
  --color-border: rgba(60,60,67,0.12);
  --color-border-light: rgba(60,60,67,0.08);
  --color-success: #34C759;
  --color-warning: #FF9500;
  --color-error: #FF3B30;
  --color-info: #30B0C0;
  --transition: all 0.3s ease;
  --font: -apple-system, 'SF Pro Display', 'Helvetica Neue', system-ui, sans-serif;
  --radius-xs: 2px;
  --radius-sm: 8px;
  --radius-default: 12px;
  --radius-md: 16px;
  --radius-lg: 20px;
  --radius-full: 9999px;
  --shadow-xs: 0 1px 3px rgba(0, 0, 0, 0.04);
  --shadow-sm: 0 4px 12px rgba(0, 0, 0, 0.06);
  --shadow-md: 0 8px 24px rgba(0, 0, 0, 0.08);
  --shadow-lg: 0 12px 32px rgba(0, 0, 0, 0.12);
  --shadow-xl: 0 16px 48px rgba(0, 0, 0, 0.16);
}
```

### Tailwind Config
```js
// tailwind.config.js theme.extend
{
  colors: {
    'white': '#ffffff',
    'surface-light': '#F2F2F7',
    'surface': '#E9E9EE',
    'text': '#1C1C1E',
    'text-secondary': '#3C3C43',
    'text-tertiary': '#8E8E93',
    'primary': '#007AFF',
    'primary-light': '#E8F4FF',
    'primary-dark': '#0051D5',
    'secondary': '#5856D6',
    'secondary-light': '#F0ECFF',
    'border': 'rgba(60,60,67,0.12)',
    'border-light': 'rgba(60,60,67,0.08)',
    'success': '#34C759',
    'warning': '#FF9500',
    'error': '#FF3B30',
    'info': '#30B0C0',
  },
  borderRadius: {
    'xs': '2px',
    'sm': '8px',
    'default': '12px',
    'md': '16px',
    'lg': '20px',
    'full': '9999px',
  },
  boxShadow: {
    'xs': '0 1px 3px rgba(0, 0, 0, 0.04)',
    'sm': '0 4px 12px rgba(0, 0, 0, 0.06)',
    'md': '0 8px 24px rgba(0, 0, 0, 0.08)',
    'lg': '0 12px 32px rgba(0, 0, 0, 0.12)',
    'xl': '0 16px 48px rgba(0, 0, 0, 0.16)',
  },
  fontFamily: {
    sans: ['SF Pro Display', 'system-ui', 'sans-serif'],
  },
}
```

---

## Glassmorphism

**Slug:** `glassmorphism` | **Category:** Visual Effects & Depth | **Font:** Inter

### Colors
| Token | Value |
|-------|-------|
| `--color-white` | `#ffffff` |
| `--color-surface-light` | `rgba(255, 255, 255, 0.06)` |
| `--color-surface` | `rgba(255, 255, 255, 0.08)` |
| `--color-text` | `#ffffff` |
| `--color-text-secondary` | `rgba(255, 255, 255, 0.7)` |
| `--color-text-tertiary` | `rgba(255, 255, 255, 0.5)` |
| `--color-primary` | `#A78BFA` |
| `--color-primary-light` | `rgba(167, 139, 250, 0.2)` |
| `--color-primary-dark` | `#8B7ADB` |
| `--color-secondary` | `rgba(255, 255, 255, 0.3)` |
| `--color-secondary-light` | `rgba(255, 255, 255, 0.1)` |
| `--color-border` | `rgba(255, 255, 255, 0.1)` |
| `--color-border-light` | `rgba(255, 255, 255, 0.08)` |
| `--color-success` | `#10B981` |
| `--color-warning` | `#F59E0B` |
| `--color-error` | `#EF4444` |
| `--color-info` | `#06B6D4` |

### Typography
| Token | Value |
|-------|-------|
| `--font-family` | `'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif` |
| `--transition` | `all 150ms ease-in-out` |

### Border Radius
| Token | Value |
|-------|-------|
| `--radius-xs` | `2px` |
| `--radius-sm` | `4px` |
| `--radius-default` | `8px` |
| `--radius-md` | `12px` |
| `--radius-lg` | `16px` |
| `--radius-full` | `9999px` |

### Shadows
| Token | Value |
|-------|-------|
| `--shadow-xs` | `0 0 30px rgba(167, 139, 250, 0.25)` |
| `--shadow-sm` | `0 0 40px rgba(167, 139, 250, 0.35)` |
| `--shadow-md` | `0 0 50px rgba(167, 139, 250, 0.45)` |
| `--shadow-lg` | `0 0 60px rgba(167, 139, 250, 0.55)` |
| `--shadow-xl` | `0 0 80px rgba(167, 139, 250, 0.65)` |

### CSS Variables (copy-paste ready)
```css
:root {
  --color-white: #ffffff;
  --color-surface-light: rgba(255, 255, 255, 0.06);
  --color-surface: rgba(255, 255, 255, 0.08);
  --color-text: #ffffff;
  --color-text-secondary: rgba(255, 255, 255, 0.7);
  --color-text-tertiary: rgba(255, 255, 255, 0.5);
  --color-primary: #A78BFA;
  --color-primary-light: rgba(167, 139, 250, 0.2);
  --color-primary-dark: #8B7ADB;
  --color-secondary: rgba(255, 255, 255, 0.3);
  --color-secondary-light: rgba(255, 255, 255, 0.1);
  --color-border: rgba(255, 255, 255, 0.1);
  --color-border-light: rgba(255, 255, 255, 0.08);
  --color-success: #10B981;
  --color-warning: #F59E0B;
  --color-error: #EF4444;
  --color-info: #06B6D4;
  --transition: all 150ms ease-in-out;
  --font: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
  --radius-xs: 2px;
  --radius-sm: 4px;
  --radius-default: 8px;
  --radius-md: 12px;
  --radius-lg: 16px;
  --radius-full: 9999px;
  --shadow-xs: 0 0 30px rgba(167, 139, 250, 0.25);
  --shadow-sm: 0 0 40px rgba(167, 139, 250, 0.35);
  --shadow-md: 0 0 50px rgba(167, 139, 250, 0.45);
  --shadow-lg: 0 0 60px rgba(167, 139, 250, 0.55);
  --shadow-xl: 0 0 80px rgba(167, 139, 250, 0.65);
}
```

### Tailwind Config
```js
// tailwind.config.js theme.extend
{
  colors: {
    'white': '#ffffff',
    'surface-light': 'rgba(255, 255, 255, 0.06)',
    'surface': 'rgba(255, 255, 255, 0.08)',
    'text': '#ffffff',
    'text-secondary': 'rgba(255, 255, 255, 0.7)',
    'text-tertiary': 'rgba(255, 255, 255, 0.5)',
    'primary': '#A78BFA',
    'primary-light': 'rgba(167, 139, 250, 0.2)',
    'primary-dark': '#8B7ADB',
    'secondary': 'rgba(255, 255, 255, 0.3)',
    'secondary-light': 'rgba(255, 255, 255, 0.1)',
    'border': 'rgba(255, 255, 255, 0.1)',
    'border-light': 'rgba(255, 255, 255, 0.08)',
    'success': '#10B981',
    'warning': '#F59E0B',
    'error': '#EF4444',
    'info': '#06B6D4',
  },
  borderRadius: {
    'xs': '2px',
    'sm': '4px',
    'default': '8px',
    'md': '12px',
    'lg': '16px',
    'full': '9999px',
  },
  boxShadow: {
    'xs': '0 0 30px rgba(167, 139, 250, 0.25)',
    'sm': '0 0 40px rgba(167, 139, 250, 0.35)',
    'md': '0 0 50px rgba(167, 139, 250, 0.45)',
    'lg': '0 0 60px rgba(167, 139, 250, 0.55)',
    'xl': '0 0 80px rgba(167, 139, 250, 0.65)',
  },
  fontFamily: {
    sans: ['Inter', 'system-ui', 'sans-serif'],
  },
}
```

---

## Neumorphism

**Slug:** `neumorphism` | **Category:** Visual Effects & Depth | **Font:** Nunito

### Colors
| Token | Value |
|-------|-------|
| `--color-white` | `#e0e5ec` |
| `--color-surface-light` | `#e0e5ec` |
| `--color-surface` | `#e0e5ec` |
| `--color-text` | `#44476A` |
| `--color-text-secondary` | `#72788C` |
| `--color-text-tertiary` | `#9CA3AF` |
| `--color-primary` | `#6c63ff` |
| `--color-primary-light` | `#EEF2FF` |
| `--color-primary-dark` | `#5A52D5` |
| `--color-shadow-dark` | `#a3b1c6` |
| `--color-shadow-light` | `#ffffff` |
| `--color-secondary` | `#a3b1c6` |
| `--color-secondary-light` | `#e0e5ec` |
| `--color-border` | `#a3b1c6` |
| `--color-border-light` | `#cad5e2` |
| `--color-success` | `#10B981` |
| `--color-warning` | `#F59E0B` |
| `--color-error` | `#EF4444` |
| `--color-info` | `#06B6D4` |

### Typography
| Token | Value |
|-------|-------|
| `--font-family` | `'Nunito', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif` |
| `--transition` | `all 150ms ease-in-out` |

### Border Radius
| Token | Value |
|-------|-------|
| `--radius-xs` | `2px` |
| `--radius-sm` | `8px` |
| `--radius-default` | `12px` |
| `--radius-md` | `15px` |
| `--radius-lg` | `20px` |
| `--radius-full` | `9999px` |

### Shadows
| Token | Value |
|-------|-------|
| `--shadow-xs` | `8px 8px 15px #a3b1c6, -8px -8px 15px #ffffff` |
| `--shadow-sm` | `10px 10px 20px #a3b1c6, -10px -10px 20px #ffffff` |
| `--shadow-md` | `12px 12px 25px #a3b1c6, -12px -12px 25px #ffffff` |
| `--shadow-lg` | `15px 15px 30px #a3b1c6, -15px -15px 30px #ffffff` |
| `--shadow-xl` | `20px 20px 40px #a3b1c6, -20px -20px 40px #ffffff` |
| `--shadow-inset-sm` | `inset 4px 4px 8px #a3b1c6, inset -4px -4px 8px #ffffff` |
| `--shadow-inset-md` | `inset 6px 6px 12px #a3b1c6, inset -6px -6px 12px #ffffff` |

### CSS Variables (copy-paste ready)
```css
:root {
  --color-white: #e0e5ec;
  --color-surface-light: #e0e5ec;
  --color-surface: #e0e5ec;
  --color-text: #44476A;
  --color-text-secondary: #72788C;
  --color-text-tertiary: #9CA3AF;
  --color-primary: #6c63ff;
  --color-primary-light: #EEF2FF;
  --color-primary-dark: #5A52D5;
  --color-shadow-dark: #a3b1c6;
  --color-shadow-light: #ffffff;
  --color-secondary: #a3b1c6;
  --color-secondary-light: #e0e5ec;
  --color-border: #a3b1c6;
  --color-border-light: #cad5e2;
  --color-success: #10B981;
  --color-warning: #F59E0B;
  --color-error: #EF4444;
  --color-info: #06B6D4;
  --transition: all 150ms ease-in-out;
  --font: 'Nunito', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
  --radius-xs: 2px;
  --radius-sm: 8px;
  --radius-default: 12px;
  --radius-md: 15px;
  --radius-lg: 20px;
  --radius-full: 9999px;
  --shadow-xs: 8px 8px 15px #a3b1c6, -8px -8px 15px #ffffff;
  --shadow-sm: 10px 10px 20px #a3b1c6, -10px -10px 20px #ffffff;
  --shadow-md: 12px 12px 25px #a3b1c6, -12px -12px 25px #ffffff;
  --shadow-lg: 15px 15px 30px #a3b1c6, -15px -15px 30px #ffffff;
  --shadow-xl: 20px 20px 40px #a3b1c6, -20px -20px 40px #ffffff;
  --shadow-inset-sm: inset 4px 4px 8px #a3b1c6, inset -4px -4px 8px #ffffff;
  --shadow-inset-md: inset 6px 6px 12px #a3b1c6, inset -6px -6px 12px #ffffff;
}
```

### Tailwind Config
```js
// tailwind.config.js theme.extend
{
  colors: {
    'white': '#e0e5ec',
    'surface-light': '#e0e5ec',
    'surface': '#e0e5ec',
    'text': '#44476A',
    'text-secondary': '#72788C',
    'text-tertiary': '#9CA3AF',
    'primary': '#6c63ff',
    'primary-light': '#EEF2FF',
    'primary-dark': '#5A52D5',
    'shadow-dark': '#a3b1c6',
    'shadow-light': '#ffffff',
    'secondary': '#a3b1c6',
    'secondary-light': '#e0e5ec',
    'border': '#a3b1c6',
    'border-light': '#cad5e2',
    'success': '#10B981',
    'warning': '#F59E0B',
    'error': '#EF4444',
    'info': '#06B6D4',
  },
  borderRadius: {
    'xs': '2px',
    'sm': '8px',
    'default': '12px',
    'md': '15px',
    'lg': '20px',
    'full': '9999px',
  },
  boxShadow: {
    'xs': '8px 8px 15px #a3b1c6, -8px -8px 15px #ffffff',
    'sm': '10px 10px 20px #a3b1c6, -10px -10px 20px #ffffff',
    'md': '12px 12px 25px #a3b1c6, -12px -12px 25px #ffffff',
    'lg': '15px 15px 30px #a3b1c6, -15px -15px 30px #ffffff',
    'xl': '20px 20px 40px #a3b1c6, -20px -20px 40px #ffffff',
    'inset-sm': 'inset 4px 4px 8px #a3b1c6, inset -4px -4px 8px #ffffff',
    'inset-md': 'inset 6px 6px 12px #a3b1c6, inset -6px -6px 12px #ffffff',
  },
  fontFamily: {
    sans: ['Nunito', 'system-ui', 'sans-serif'],
  },
}
```

---

## Claymorphism

**Slug:** `claymorphism` | **Category:** Visual Effects & Depth | **Font:** Quicksand

### Colors
| Token | Value |
|-------|-------|
| `--color-white` | `#ffffff` |
| `--color-surface-light` | `#FAF0FF` |
| `--color-surface` | `#ffffff` |
| `--color-text` | `#6C5CE7` |
| `--color-text-secondary` | `#9B88D9` |
| `--color-text-tertiary` | `#C5B9E8` |
| `--color-primary` | `#6C5CE7` |
| `--color-primary-light` | `#FAF0FF` |
| `--color-primary-dark` | `#5A4DBF` |
| `--color-secondary` | `#A29BFE` |
| `--color-secondary-light` | `#FAF0FF` |
| `--color-border` | `#E8DFF8` |
| `--color-border-light` | `#FAF0FF` |
| `--color-success` | `#00CEC9` |
| `--color-warning` | `#FFEAA7` |
| `--color-error` | `#FD79A8` |
| `--color-info` | `#74B9FF` |

### Typography
| Token | Value |
|-------|-------|
| `--font-family` | `'Quicksand', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif` |
| `--transition` | `all 150ms ease-in-out` |

### Border Radius
| Token | Value |
|-------|-------|
| `--radius-xs` | `2px` |
| `--radius-sm` | `12px` |
| `--radius-default` | `16px` |
| `--radius-md` | `20px` |
| `--radius-lg` | `24px` |
| `--radius-full` | `9999px` |

### Shadows
| Token | Value |
|-------|-------|
| `--shadow-xs` | `0 10px 40px rgba(108, 92, 231, 0.15), inset 0 -3px 4px rgba(108, 92, 231, 0.1)` |
| `--shadow-sm` | `0 12px 50px rgba(108, 92, 231, 0.2), inset 0 -4px 6px rgba(108, 92, 231, 0.12)` |
| `--shadow-md` | `0 15px 60px rgba(108, 92, 231, 0.25), inset 0 -5px 8px rgba(108, 92, 231, 0.15)` |
| `--shadow-lg` | `0 20px 70px rgba(108, 92, 231, 0.3), inset 0 -6px 10px rgba(108, 92, 231, 0.18)` |
| `--shadow-xl` | `0 30px 90px rgba(108, 92, 231, 0.35), inset 0 -8px 12px rgba(108, 92, 231, 0.2)` |

### CSS Variables (copy-paste ready)
```css
:root {
  --color-white: #ffffff;
  --color-surface-light: #FAF0FF;
  --color-surface: #ffffff;
  --color-text: #6C5CE7;
  --color-text-secondary: #9B88D9;
  --color-text-tertiary: #C5B9E8;
  --color-primary: #6C5CE7;
  --color-primary-light: #FAF0FF;
  --color-primary-dark: #5A4DBF;
  --color-secondary: #A29BFE;
  --color-secondary-light: #FAF0FF;
  --color-border: #E8DFF8;
  --color-border-light: #FAF0FF;
  --color-success: #00CEC9;
  --color-warning: #FFEAA7;
  --color-error: #FD79A8;
  --color-info: #74B9FF;
  --transition: all 150ms ease-in-out;
  --font: 'Quicksand', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
  --radius-xs: 2px;
  --radius-sm: 12px;
  --radius-default: 16px;
  --radius-md: 20px;
  --radius-lg: 24px;
  --radius-full: 9999px;
  --shadow-xs: 0 10px 40px rgba(108, 92, 231, 0.15), inset 0 -3px 4px rgba(108, 92, 231, 0.1);
  --shadow-sm: 0 12px 50px rgba(108, 92, 231, 0.2), inset 0 -4px 6px rgba(108, 92, 231, 0.12);
  --shadow-md: 0 15px 60px rgba(108, 92, 231, 0.25), inset 0 -5px 8px rgba(108, 92, 231, 0.15);
  --shadow-lg: 0 20px 70px rgba(108, 92, 231, 0.3), inset 0 -6px 10px rgba(108, 92, 231, 0.18);
  --shadow-xl: 0 30px 90px rgba(108, 92, 231, 0.35), inset 0 -8px 12px rgba(108, 92, 231, 0.2);
}
```

### Tailwind Config
```js
// tailwind.config.js theme.extend
{
  colors: {
    'white': '#ffffff',
    'surface-light': '#FAF0FF',
    'surface': '#ffffff',
    'text': '#6C5CE7',
    'text-secondary': '#9B88D9',
    'text-tertiary': '#C5B9E8',
    'primary': '#6C5CE7',
    'primary-light': '#FAF0FF',
    'primary-dark': '#5A4DBF',
    'secondary': '#A29BFE',
    'secondary-light': '#FAF0FF',
    'border': '#E8DFF8',
    'border-light': '#FAF0FF',
    'success': '#00CEC9',
    'warning': '#FFEAA7',
    'error': '#FD79A8',
    'info': '#74B9FF',
  },
  borderRadius: {
    'xs': '2px',
    'sm': '12px',
    'default': '16px',
    'md': '20px',
    'lg': '24px',
    'full': '9999px',
  },
  boxShadow: {
    'xs': '0 10px 40px rgba(108, 92, 231, 0.15), inset 0 -3px 4px rgba(108, 92, 231, 0.1)',
    'sm': '0 12px 50px rgba(108, 92, 231, 0.2), inset 0 -4px 6px rgba(108, 92, 231, 0.12)',
    'md': '0 15px 60px rgba(108, 92, 231, 0.25), inset 0 -5px 8px rgba(108, 92, 231, 0.15)',
    'lg': '0 20px 70px rgba(108, 92, 231, 0.3), inset 0 -6px 10px rgba(108, 92, 231, 0.18)',
    'xl': '0 30px 90px rgba(108, 92, 231, 0.35), inset 0 -8px 12px rgba(108, 92, 231, 0.2)',
  },
  fontFamily: {
    sans: ['Quicksand', 'system-ui', 'sans-serif'],
  },
}
```

---

## Aurora Gradient

**Slug:** `aurora-gradient` | **Category:** Visual Effects & Depth | **Font:** Space Grotesk

### Colors
| Token | Value |
|-------|-------|
| `--color-white` | `#ffffff` |
| `--color-surface-light` | `rgba(255, 255, 255, 0.05)` |
| `--color-surface` | `rgba(255, 255, 255, 0.08)` |
| `--color-text` | `#ffffff` |
| `--color-text-secondary` | `rgba(255, 255, 255, 0.7)` |
| `--color-text-tertiary` | `rgba(255, 255, 255, 0.5)` |
| `--color-primary` | `#ec4899` |
| `--color-primary-light` | `rgba(236, 72, 153, 0.15)` |
| `--color-primary-dark` | `#be185d` |
| `--color-secondary` | `rgba(255, 255, 255, 0.2)` |
| `--color-secondary-light` | `rgba(255, 255, 255, 0.1)` |
| `--color-border` | `rgba(255, 255, 255, 0.1)` |
| `--color-border-light` | `rgba(255, 255, 255, 0.08)` |
| `--color-success` | `#10B981` |
| `--color-warning` | `#F59E0B` |
| `--color-error` | `#EF4444` |
| `--color-info` | `#06B6D4` |

### Typography
| Token | Value |
|-------|-------|
| `--font-family` | `'Space Grotesk', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif` |
| `--transition` | `all 150ms ease-in-out` |

### Border Radius
| Token | Value |
|-------|-------|
| `--radius-xs` | `2px` |
| `--radius-sm` | `8px` |
| `--radius-default` | `12px` |
| `--radius-md` | `16px` |
| `--radius-lg` | `20px` |
| `--radius-full` | `9999px` |

### Shadows
| Token | Value |
|-------|-------|
| `--shadow-xs` | `0 0 40px rgba(236, 72, 153, 0.3)` |
| `--shadow-sm` | `0 0 50px rgba(236, 72, 153, 0.4)` |
| `--shadow-md` | `0 0 60px rgba(139, 92, 246, 0.4)` |
| `--shadow-lg` | `0 0 80px rgba(59, 130, 246, 0.4)` |
| `--shadow-xl` | `0 0 100px rgba(6, 182, 212, 0.3)` |

### CSS Variables (copy-paste ready)
```css
:root {
  --color-white: #ffffff;
  --color-surface-light: rgba(255, 255, 255, 0.05);
  --color-surface: rgba(255, 255, 255, 0.08);
  --color-text: #ffffff;
  --color-text-secondary: rgba(255, 255, 255, 0.7);
  --color-text-tertiary: rgba(255, 255, 255, 0.5);
  --color-primary: #ec4899;
  --color-primary-light: rgba(236, 72, 153, 0.15);
  --color-primary-dark: #be185d;
  --color-secondary: rgba(255, 255, 255, 0.2);
  --color-secondary-light: rgba(255, 255, 255, 0.1);
  --color-border: rgba(255, 255, 255, 0.1);
  --color-border-light: rgba(255, 255, 255, 0.08);
  --color-success: #10B981;
  --color-warning: #F59E0B;
  --color-error: #EF4444;
  --color-info: #06B6D4;
  --transition: all 150ms ease-in-out;
  --font: 'Space Grotesk', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
  --radius-xs: 2px;
  --radius-sm: 8px;
  --radius-default: 12px;
  --radius-md: 16px;
  --radius-lg: 20px;
  --radius-full: 9999px;
  --shadow-xs: 0 0 40px rgba(236, 72, 153, 0.3);
  --shadow-sm: 0 0 50px rgba(236, 72, 153, 0.4);
  --shadow-md: 0 0 60px rgba(139, 92, 246, 0.4);
  --shadow-lg: 0 0 80px rgba(59, 130, 246, 0.4);
  --shadow-xl: 0 0 100px rgba(6, 182, 212, 0.3);
}
```

### Tailwind Config
```js
// tailwind.config.js theme.extend
{
  colors: {
    'white': '#ffffff',
    'surface-light': 'rgba(255, 255, 255, 0.05)',
    'surface': 'rgba(255, 255, 255, 0.08)',
    'text': '#ffffff',
    'text-secondary': 'rgba(255, 255, 255, 0.7)',
    'text-tertiary': 'rgba(255, 255, 255, 0.5)',
    'primary': '#ec4899',
    'primary-light': 'rgba(236, 72, 153, 0.15)',
    'primary-dark': '#be185d',
    'secondary': 'rgba(255, 255, 255, 0.2)',
    'secondary-light': 'rgba(255, 255, 255, 0.1)',
    'border': 'rgba(255, 255, 255, 0.1)',
    'border-light': 'rgba(255, 255, 255, 0.08)',
    'success': '#10B981',
    'warning': '#F59E0B',
    'error': '#EF4444',
    'info': '#06B6D4',
  },
  borderRadius: {
    'xs': '2px',
    'sm': '8px',
    'default': '12px',
    'md': '16px',
    'lg': '20px',
    'full': '9999px',
  },
  boxShadow: {
    'xs': '0 0 40px rgba(236, 72, 153, 0.3)',
    'sm': '0 0 50px rgba(236, 72, 153, 0.4)',
    'md': '0 0 60px rgba(139, 92, 246, 0.4)',
    'lg': '0 0 80px rgba(59, 130, 246, 0.4)',
    'xl': '0 0 100px rgba(6, 182, 212, 0.3)',
  },
  fontFamily: {
    sans: ['Space Grotesk', 'system-ui', 'sans-serif'],
  },
}
```

---

## Bento Grid

**Slug:** `bento-grid` | **Category:** Visual Effects & Depth | **Font:** Sora

### Colors
| Token | Value |
|-------|-------|
| `--color-white` | `#ffffff` |
| `--color-surface-light` | `#131313` |
| `--color-surface` | `#1a1a1a` |
| `--color-text` | `#ffffff` |
| `--color-text-secondary` | `#a0a0a0` |
| `--color-text-tertiary` | `#696969` |
| `--color-primary` | `#4f46e5` |
| `--color-primary-light` | `rgba(79, 70, 229, 0.1)` |
| `--color-primary-dark` | `#3730a3` |
| `--color-secondary` | `#7c3aed` |
| `--color-secondary-light` | `rgba(124, 58, 237, 0.1)` |
| `--color-border` | `rgba(255, 255, 255, 0.06)` |
| `--color-border-light` | `rgba(255, 255, 255, 0.03)` |
| `--color-success` | `#10b981` |
| `--color-warning` | `#f59e0b` |
| `--color-error` | `#ef4444` |
| `--color-info` | `#3b82f6` |

### Typography
| Token | Value |
|-------|-------|
| `--font-family` | `'Sora', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif` |
| `--transition` | `all 150ms ease-in-out` |

### Border Radius
| Token | Value |
|-------|-------|
| `--radius-xs` | `2px` |
| `--radius-sm` | `4px` |
| `--radius-default` | `6px` |
| `--radius-md` | `16px` |
| `--radius-lg` | `24px` |
| `--radius-full` | `9999px` |

### Shadows
| Token | Value |
|-------|-------|
| `--shadow-xs` | `0 1px 2px rgba(0, 0, 0, 0.3)` |
| `--shadow-sm` | `0 4px 12px rgba(79, 70, 229, 0.15)` |
| `--shadow-md` | `0 8px 24px rgba(79, 70, 229, 0.2)` |
| `--shadow-lg` | `0 20px 40px rgba(79, 70, 229, 0.25)` |
| `--shadow-xl` | `0 30px 60px rgba(79, 70, 229, 0.3)` |

### CSS Variables (copy-paste ready)
```css
:root {
  --color-white: #ffffff;
  --color-surface-light: #131313;
  --color-surface: #1a1a1a;
  --color-text: #ffffff;
  --color-text-secondary: #a0a0a0;
  --color-text-tertiary: #696969;
  --color-primary: #4f46e5;
  --color-primary-light: rgba(79, 70, 229, 0.1);
  --color-primary-dark: #3730a3;
  --color-secondary: #7c3aed;
  --color-secondary-light: rgba(124, 58, 237, 0.1);
  --color-border: rgba(255, 255, 255, 0.06);
  --color-border-light: rgba(255, 255, 255, 0.03);
  --color-success: #10b981;
  --color-warning: #f59e0b;
  --color-error: #ef4444;
  --color-info: #3b82f6;
  --transition: all 150ms ease-in-out;
  --font: 'Sora', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
  --radius-xs: 2px;
  --radius-sm: 4px;
  --radius-default: 6px;
  --radius-md: 16px;
  --radius-lg: 24px;
  --radius-full: 9999px;
  --shadow-xs: 0 1px 2px rgba(0, 0, 0, 0.3);
  --shadow-sm: 0 4px 12px rgba(79, 70, 229, 0.15);
  --shadow-md: 0 8px 24px rgba(79, 70, 229, 0.2);
  --shadow-lg: 0 20px 40px rgba(79, 70, 229, 0.25);
  --shadow-xl: 0 30px 60px rgba(79, 70, 229, 0.3);
}
```

### Tailwind Config
```js
// tailwind.config.js theme.extend
{
  colors: {
    'white': '#ffffff',
    'surface-light': '#131313',
    'surface': '#1a1a1a',
    'text': '#ffffff',
    'text-secondary': '#a0a0a0',
    'text-tertiary': '#696969',
    'primary': '#4f46e5',
    'primary-light': 'rgba(79, 70, 229, 0.1)',
    'primary-dark': '#3730a3',
    'secondary': '#7c3aed',
    'secondary-light': 'rgba(124, 58, 237, 0.1)',
    'border': 'rgba(255, 255, 255, 0.06)',
    'border-light': 'rgba(255, 255, 255, 0.03)',
    'success': '#10b981',
    'warning': '#f59e0b',
    'error': '#ef4444',
    'info': '#3b82f6',
  },
  borderRadius: {
    'xs': '2px',
    'sm': '4px',
    'default': '6px',
    'md': '16px',
    'lg': '24px',
    'full': '9999px',
  },
  boxShadow: {
    'xs': '0 1px 2px rgba(0, 0, 0, 0.3)',
    'sm': '0 4px 12px rgba(79, 70, 229, 0.15)',
    'md': '0 8px 24px rgba(79, 70, 229, 0.2)',
    'lg': '0 20px 40px rgba(79, 70, 229, 0.25)',
    'xl': '0 30px 60px rgba(79, 70, 229, 0.3)',
  },
  fontFamily: {
    sans: ['Sora', 'system-ui', 'sans-serif'],
  },
}
```

---

## Neo Brutalism

**Slug:** `neo-brutalism` | **Category:** Bold & Expressive | **Font:** Space Grotesk

### Colors
| Token | Value |
|-------|-------|
| `--color-white` | `#ffffff` |
| `--color-off-white` | `#FFFDF7` |
| `--color-cream` | `#FFF8F0` |
| `--color-text` | `#1A1A2E` |
| `--color-text-secondary` | `#2D2D44` |
| `--color-text-tertiary` | `#6B6B80` |
| `--color-primary` | `#FF6B6B` |
| `--color-secondary` | `#4ECDC4` |
| `--color-accent-yellow` | `#FFE66D` |
| `--color-accent-mint` | `#95E1D3` |
| `--color-accent-green` | `#A8E6CF` |
| `--color-border` | `#1A1A2E` |
| `--color-shadow` | `#1A1A2E` |

### Typography
| Token | Value |
|-------|-------|
| `--font-family` | `'Space Grotesk', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif` |
| `--transition` | `all 150ms cubic-bezier(0.34, 1.56, 0.64, 1)` |

### Border Radius
| Token | Value |
|-------|-------|
| `--radius-xs` | `0px` |
| `--radius-sm` | `2px` |
| `--radius-default` | `2px` |
| `--radius-md` | `2px` |
| `--radius-lg` | `2px` |
| `--radius-full` | `2px` |

### Shadows
| Token | Value |
|-------|-------|

### CSS Variables (copy-paste ready)
```css
:root {
  --color-white: #ffffff;
  --color-off-white: #FFFDF7;
  --color-cream: #FFF8F0;
  --color-text: #1A1A2E;
  --color-text-secondary: #2D2D44;
  --color-text-tertiary: #6B6B80;
  --color-primary: #FF6B6B;
  --color-secondary: #4ECDC4;
  --color-accent-yellow: #FFE66D;
  --color-accent-mint: #95E1D3;
  --color-accent-green: #A8E6CF;
  --color-border: #1A1A2E;
  --color-shadow: #1A1A2E;
  --transition: all 150ms cubic-bezier(0.34, 1.56, 0.64, 1);
  --font: 'Space Grotesk', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
  --radius-xs: 0px;
  --radius-sm: 2px;
  --radius-default: 2px;
  --radius-md: 2px;
  --radius-lg: 2px;
  --radius-full: 2px;
}
```

### Tailwind Config
```js
// tailwind.config.js theme.extend
{
  colors: {
    'white': '#ffffff',
    'off-white': '#FFFDF7',
    'cream': '#FFF8F0',
    'text': '#1A1A2E',
    'text-secondary': '#2D2D44',
    'text-tertiary': '#6B6B80',
    'primary': '#FF6B6B',
    'secondary': '#4ECDC4',
    'accent-yellow': '#FFE66D',
    'accent-mint': '#95E1D3',
    'accent-green': '#A8E6CF',
    'border': '#1A1A2E',
    'shadow': '#1A1A2E',
  },
  borderRadius: {
    'xs': '0px',
    'sm': '2px',
    'default': '2px',
    'md': '2px',
    'lg': '2px',
    'full': '2px',
  },
  boxShadow: {
  },
  fontFamily: {
    sans: ['Space Grotesk', 'system-ui', 'sans-serif'],
  },
}
```

---

## Cyberpunk Neon

**Slug:** `cyberpunk-neon` | **Category:** Bold & Expressive | **Font:** Share Tech Mono

### Colors
| Token | Value |
|-------|-------|
| `--color-bg-dark` | `#0a0a0f` |
| `--color-surface` | `#0d0d14` |
| `--color-card` | `#12121a` |
| `--color-hover` | `#1a1a25` |
| `--color-primary` | `#00FF41` |
| `--color-secondary` | `#FF00FF` |
| `--color-accent-cyan` | `#00FFFF` |
| `--color-accent-yellow` | `#FFD700` |
| `--color-text` | `#e0e0e0` |
| `--color-text-dim` | `rgba(255, 255, 255, 0.5)` |
| `--color-border-green` | `rgba(0, 255, 65, 0.3)` |
| `--color-border-magenta` | `rgba(255, 0, 255, 0.3)` |

### Typography
| Token | Value |
|-------|-------|
| `--font-family` | `'Share Tech Mono', monospace` |
| `--transition` | `all 200ms ease` |

### Border Radius
| Token | Value |
|-------|-------|
| `--radius-xs` | `2px` |
| `--radius-sm` | `4px` |
| `--radius-default` | `6px` |
| `--radius-md` | `8px` |
| `--radius-lg` | `12px` |
| `--radius-full` | `9999px` |

### Shadows
| Token | Value |
|-------|-------|

### CSS Variables (copy-paste ready)
```css
:root {
  --color-bg-dark: #0a0a0f;
  --color-surface: #0d0d14;
  --color-card: #12121a;
  --color-hover: #1a1a25;
  --color-primary: #00FF41;
  --color-secondary: #FF00FF;
  --color-accent-cyan: #00FFFF;
  --color-accent-yellow: #FFD700;
  --color-text: #e0e0e0;
  --color-text-dim: rgba(255, 255, 255, 0.5);
  --color-border-green: rgba(0, 255, 65, 0.3);
  --color-border-magenta: rgba(255, 0, 255, 0.3);
  --transition: all 200ms ease;
  --font: 'Share Tech Mono', monospace;
  --radius-xs: 2px;
  --radius-sm: 4px;
  --radius-default: 6px;
  --radius-md: 8px;
  --radius-lg: 12px;
  --radius-full: 9999px;
}
```

### Tailwind Config
```js
// tailwind.config.js theme.extend
{
  colors: {
    'bg-dark': '#0a0a0f',
    'surface': '#0d0d14',
    'card': '#12121a',
    'hover': '#1a1a25',
    'primary': '#00FF41',
    'secondary': '#FF00FF',
    'accent-cyan': '#00FFFF',
    'accent-yellow': '#FFD700',
    'text': '#e0e0e0',
    'text-dim': 'rgba(255, 255, 255, 0.5)',
    'border-green': 'rgba(0, 255, 65, 0.3)',
    'border-magenta': 'rgba(255, 0, 255, 0.3)',
  },
  borderRadius: {
    'xs': '2px',
    'sm': '4px',
    'default': '6px',
    'md': '8px',
    'lg': '12px',
    'full': '9999px',
  },
  boxShadow: {
  },
  fontFamily: {
    sans: ['Share Tech Mono', 'system-ui', 'sans-serif'],
  },
}
```

---

## Swiss Typography

**Slug:** `swiss-typography` | **Category:** Bold & Expressive | **Font:** Helvetica Neue

### Colors
| Token | Value |
|-------|-------|
| `--color-white` | `#ffffff` |
| `--color-surface-light` | `#f5f5f5` |
| `--color-surface` | `#fafafa` |
| `--color-text` | `#000000` |
| `--color-text-secondary` | `#333333` |
| `--color-text-tertiary` | `#666666` |
| `--color-primary` | `#ff0000` |
| `--color-primary-light` | `#ffe0e0` |
| `--color-primary-dark` | `#cc0000` |
| `--color-secondary` | `#000000` |
| `--color-secondary-light` | `#f0f0f0` |
| `--color-border` | `#000000` |
| `--color-border-light` | `#d0d0d0` |
| `--color-success` | `#00aa00` |
| `--color-warning` | `#ff9900` |
| `--color-error` | `#cc0000` |
| `--color-info` | `#0066cc` |

### Typography
| Token | Value |
|-------|-------|
| `--font-family` | `'Helvetica Neue', Arial, -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif` |
| `--transition` | `all 150ms cubic-bezier(0.25, 0.46, 0.45, 0.94)` |

### Border Radius
| Token | Value |
|-------|-------|
| `--radius-xs` | `0px` |
| `--radius-sm` | `0px` |
| `--radius-default` | `0px` |
| `--radius-md` | `0px` |
| `--radius-lg` | `0px` |
| `--radius-full` | `0px` |

### Shadows
| Token | Value |
|-------|-------|
| `--shadow-xs` | `0 1px 2px rgba(0,0,0,0.04)` |
| `--shadow-sm` | `0 2px 4px rgba(0,0,0,0.06)` |
| `--shadow-md` | `0 4px 8px rgba(0,0,0,0.06)` |
| `--shadow-lg` | `0 8px 16px rgba(0,0,0,0.06)` |
| `--shadow-xl` | `0 12px 24px rgba(0,0,0,0.08)` |

### CSS Variables (copy-paste ready)
```css
:root {
  --color-white: #ffffff;
  --color-surface-light: #f5f5f5;
  --color-surface: #fafafa;
  --color-text: #000000;
  --color-text-secondary: #333333;
  --color-text-tertiary: #666666;
  --color-primary: #ff0000;
  --color-primary-light: #ffe0e0;
  --color-primary-dark: #cc0000;
  --color-secondary: #000000;
  --color-secondary-light: #f0f0f0;
  --color-border: #000000;
  --color-border-light: #d0d0d0;
  --color-success: #00aa00;
  --color-warning: #ff9900;
  --color-error: #cc0000;
  --color-info: #0066cc;
  --transition: all 150ms cubic-bezier(0.25, 0.46, 0.45, 0.94);
  --font: 'Helvetica Neue', Arial, -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
  --radius-xs: 0px;
  --radius-sm: 0px;
  --radius-default: 0px;
  --radius-md: 0px;
  --radius-lg: 0px;
  --radius-full: 0px;
  --shadow-xs: 0 1px 2px rgba(0,0,0,0.04);
  --shadow-sm: 0 2px 4px rgba(0,0,0,0.06);
  --shadow-md: 0 4px 8px rgba(0,0,0,0.06);
  --shadow-lg: 0 8px 16px rgba(0,0,0,0.06);
  --shadow-xl: 0 12px 24px rgba(0,0,0,0.08);
}
```

### Tailwind Config
```js
// tailwind.config.js theme.extend
{
  colors: {
    'white': '#ffffff',
    'surface-light': '#f5f5f5',
    'surface': '#fafafa',
    'text': '#000000',
    'text-secondary': '#333333',
    'text-tertiary': '#666666',
    'primary': '#ff0000',
    'primary-light': '#ffe0e0',
    'primary-dark': '#cc0000',
    'secondary': '#000000',
    'secondary-light': '#f0f0f0',
    'border': '#000000',
    'border-light': '#d0d0d0',
    'success': '#00aa00',
    'warning': '#ff9900',
    'error': '#cc0000',
    'info': '#0066cc',
  },
  borderRadius: {
    'xs': '0px',
    'sm': '0px',
    'default': '0px',
    'md': '0px',
    'lg': '0px',
    'full': '0px',
  },
  boxShadow: {
    'xs': '0 1px 2px rgba(0,0,0,0.04)',
    'sm': '0 2px 4px rgba(0,0,0,0.06)',
    'md': '0 4px 8px rgba(0,0,0,0.06)',
    'lg': '0 8px 16px rgba(0,0,0,0.06)',
    'xl': '0 12px 24px rgba(0,0,0,0.08)',
  },
  fontFamily: {
    sans: ['Helvetica Neue', 'system-ui', 'sans-serif'],
  },
}
```

---

## Art Deco

**Slug:** `art-deco` | **Category:** Bold & Expressive | **Font:** Lato

### Colors
| Token | Value |
|-------|-------|
| `--color-white` | `#ffffff` |
| `--color-surface-light` | `#2a2722` |
| `--color-surface` | `#1a1a1a` |
| `--color-text` | `#f5f0e8` |
| `--color-text-secondary` | `#d4cfc6` |
| `--color-text-tertiary` | `#a8a39a` |
| `--color-primary` | `#c9a84c` |
| `--color-primary-light` | `#d4af37` |
| `--color-primary-dark` | `#b8961f` |
| `--color-secondary` | `#c9a84c` |
| `--color-secondary-light` | `rgba(201, 168, 76, 0.1)` |
| `--color-border` | `#c9a84c` |
| `--color-border-light` | `rgba(201, 168, 76, 0.2)` |
| `--color-success` | `#8fad56` |
| `--color-warning` | `#c9a84c` |
| `--color-error` | `#a85c4c` |
| `--color-info` | `#5d7c8c` |

### Typography
| Token | Value |
|-------|-------|
| `--font-family` | `'Lato', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif` |
| `--transition` | `all 200ms cubic-bezier(0.25, 0.46, 0.45, 0.94)` |

### Border Radius
| Token | Value |
|-------|-------|
| `--radius-xs` | `0px` |
| `--radius-sm` | `2px` |
| `--radius-default` | `2px` |
| `--radius-md` | `2px` |
| `--radius-lg` | `2px` |
| `--radius-full` | `0px` |

### Shadows
| Token | Value |
|-------|-------|
| `--shadow-xs` | `0 2px 4px rgba(0, 0, 0, 0.4), 0 0 12px rgba(201, 168, 76, 0.1)` |
| `--shadow-sm` | `0 4px 8px rgba(201, 168, 76, 0.15), 0 0 20px rgba(201, 168, 76, 0.1)` |
| `--shadow-md` | `0 8px 16px rgba(0, 0, 0, 0.3), 0 0 20px rgba(201, 168, 76, 0.15)` |
| `--shadow-lg` | `0 16px 32px rgba(0, 0, 0, 0.4), 0 0 24px rgba(201, 168, 76, 0.2)` |
| `--shadow-xl` | `0 24px 48px rgba(0, 0, 0, 0.5), 0 0 32px rgba(201, 168, 76, 0.2)` |

### CSS Variables (copy-paste ready)
```css
:root {
  --color-white: #ffffff;
  --color-surface-light: #2a2722;
  --color-surface: #1a1a1a;
  --color-text: #f5f0e8;
  --color-text-secondary: #d4cfc6;
  --color-text-tertiary: #a8a39a;
  --color-primary: #c9a84c;
  --color-primary-light: #d4af37;
  --color-primary-dark: #b8961f;
  --color-secondary: #c9a84c;
  --color-secondary-light: rgba(201, 168, 76, 0.1);
  --color-border: #c9a84c;
  --color-border-light: rgba(201, 168, 76, 0.2);
  --color-success: #8fad56;
  --color-warning: #c9a84c;
  --color-error: #a85c4c;
  --color-info: #5d7c8c;
  --transition: all 200ms cubic-bezier(0.25, 0.46, 0.45, 0.94);
  --font: 'Lato', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
  --radius-xs: 0px;
  --radius-sm: 2px;
  --radius-default: 2px;
  --radius-md: 2px;
  --radius-lg: 2px;
  --radius-full: 0px;
  --shadow-xs: 0 2px 4px rgba(0, 0, 0, 0.4), 0 0 12px rgba(201, 168, 76, 0.1);
  --shadow-sm: 0 4px 8px rgba(201, 168, 76, 0.15), 0 0 20px rgba(201, 168, 76, 0.1);
  --shadow-md: 0 8px 16px rgba(0, 0, 0, 0.3), 0 0 20px rgba(201, 168, 76, 0.15);
  --shadow-lg: 0 16px 32px rgba(0, 0, 0, 0.4), 0 0 24px rgba(201, 168, 76, 0.2);
  --shadow-xl: 0 24px 48px rgba(0, 0, 0, 0.5), 0 0 32px rgba(201, 168, 76, 0.2);
}
```

### Tailwind Config
```js
// tailwind.config.js theme.extend
{
  colors: {
    'white': '#ffffff',
    'surface-light': '#2a2722',
    'surface': '#1a1a1a',
    'text': '#f5f0e8',
    'text-secondary': '#d4cfc6',
    'text-tertiary': '#a8a39a',
    'primary': '#c9a84c',
    'primary-light': '#d4af37',
    'primary-dark': '#b8961f',
    'secondary': '#c9a84c',
    'secondary-light': 'rgba(201, 168, 76, 0.1)',
    'border': '#c9a84c',
    'border-light': 'rgba(201, 168, 76, 0.2)',
    'success': '#8fad56',
    'warning': '#c9a84c',
    'error': '#a85c4c',
    'info': '#5d7c8c',
  },
  borderRadius: {
    'xs': '0px',
    'sm': '2px',
    'default': '2px',
    'md': '2px',
    'lg': '2px',
    'full': '0px',
  },
  boxShadow: {
    'xs': '0 2px 4px rgba(0, 0, 0, 0.4), 0 0 12px rgba(201, 168, 76, 0.1)',
    'sm': '0 4px 8px rgba(201, 168, 76, 0.15), 0 0 20px rgba(201, 168, 76, 0.1)',
    'md': '0 8px 16px rgba(0, 0, 0, 0.3), 0 0 20px rgba(201, 168, 76, 0.15)',
    'lg': '0 16px 32px rgba(0, 0, 0, 0.4), 0 0 24px rgba(201, 168, 76, 0.2)',
    'xl': '0 24px 48px rgba(0, 0, 0, 0.5), 0 0 32px rgba(201, 168, 76, 0.2)',
  },
  fontFamily: {
    sans: ['Lato', 'system-ui', 'sans-serif'],
  },
}
```

---

## Isometric Playful

**Slug:** `isometric-playful` | **Category:** Bold & Expressive | **Font:** Poppins

### Colors
| Token | Value |
|-------|-------|
| `--color-white` | `#ffffff` |
| `--color-surface-light` | `#f5f6fb` |
| `--color-surface` | `#fafbff` |
| `--color-text` | `#0f172a` |
| `--color-text-secondary` | `#475569` |
| `--color-text-tertiary` | `#94a3b8` |
| `--color-primary` | `#6366f1` |
| `--color-primary-light` | `#e0e7ff` |
| `--color-primary-dark` | `#4f46e5` |
| `--color-secondary` | `#ec4899` |
| `--color-secondary-light` | `#fce7f3` |
| `--color-border` | `#e5e7eb` |
| `--color-border-light` | `#f3f4f6` |
| `--color-success` | `#10b981` |
| `--color-warning` | `#f59e0b` |
| `--color-error` | `#ef4444` |
| `--color-info` | `#3b82f6` |

### Typography
| Token | Value |
|-------|-------|
| `--font-family` | `'Poppins', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif` |
| `--transition` | `all 200ms cubic-bezier(0.34, 1.56, 0.64, 1)` |

### Border Radius
| Token | Value |
|-------|-------|
| `--radius-xs` | `2px` |
| `--radius-sm` | `4px` |
| `--radius-default` | `6px` |
| `--radius-md` | `12px` |
| `--radius-lg` | `16px` |
| `--radius-full` | `9999px` |

### Shadows
| Token | Value |
|-------|-------|
| `--shadow-xs` | `0 2px 4px rgba(99, 102, 241, 0.08)` |
| `--shadow-sm` | `0 4px 12px rgba(99, 102, 241, 0.12), 4px 4px 0px rgba(236, 72, 153, 0.1)` |
| `--shadow-md` | `0 8px 24px rgba(99, 102, 241, 0.15), 6px 6px 0px rgba(16, 185, 129, 0.1)` |
| `--shadow-lg` | `0 16px 32px rgba(99, 102, 241, 0.2), 8px 8px 0px rgba(236, 72, 153, 0.15)` |
| `--shadow-xl` | `0 24px 48px rgba(99, 102, 241, 0.25), 10px 10px 0px rgba(16, 185, 129, 0.12)` |

### CSS Variables (copy-paste ready)
```css
:root {
  --color-white: #ffffff;
  --color-surface-light: #f5f6fb;
  --color-surface: #fafbff;
  --color-text: #0f172a;
  --color-text-secondary: #475569;
  --color-text-tertiary: #94a3b8;
  --color-primary: #6366f1;
  --color-primary-light: #e0e7ff;
  --color-primary-dark: #4f46e5;
  --color-secondary: #ec4899;
  --color-secondary-light: #fce7f3;
  --color-border: #e5e7eb;
  --color-border-light: #f3f4f6;
  --color-success: #10b981;
  --color-warning: #f59e0b;
  --color-error: #ef4444;
  --color-info: #3b82f6;
  --transition: all 200ms cubic-bezier(0.34, 1.56, 0.64, 1);
  --font: 'Poppins', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
  --radius-xs: 2px;
  --radius-sm: 4px;
  --radius-default: 6px;
  --radius-md: 12px;
  --radius-lg: 16px;
  --radius-full: 9999px;
  --shadow-xs: 0 2px 4px rgba(99, 102, 241, 0.08);
  --shadow-sm: 0 4px 12px rgba(99, 102, 241, 0.12), 4px 4px 0px rgba(236, 72, 153, 0.1);
  --shadow-md: 0 8px 24px rgba(99, 102, 241, 0.15), 6px 6px 0px rgba(16, 185, 129, 0.1);
  --shadow-lg: 0 16px 32px rgba(99, 102, 241, 0.2), 8px 8px 0px rgba(236, 72, 153, 0.15);
  --shadow-xl: 0 24px 48px rgba(99, 102, 241, 0.25), 10px 10px 0px rgba(16, 185, 129, 0.12);
}
```

### Tailwind Config
```js
// tailwind.config.js theme.extend
{
  colors: {
    'white': '#ffffff',
    'surface-light': '#f5f6fb',
    'surface': '#fafbff',
    'text': '#0f172a',
    'text-secondary': '#475569',
    'text-tertiary': '#94a3b8',
    'primary': '#6366f1',
    'primary-light': '#e0e7ff',
    'primary-dark': '#4f46e5',
    'secondary': '#ec4899',
    'secondary-light': '#fce7f3',
    'border': '#e5e7eb',
    'border-light': '#f3f4f6',
    'success': '#10b981',
    'warning': '#f59e0b',
    'error': '#ef4444',
    'info': '#3b82f6',
  },
  borderRadius: {
    'xs': '2px',
    'sm': '4px',
    'default': '6px',
    'md': '12px',
    'lg': '16px',
    'full': '9999px',
  },
  boxShadow: {
    'xs': '0 2px 4px rgba(99, 102, 241, 0.08)',
    'sm': '0 4px 12px rgba(99, 102, 241, 0.12), 4px 4px 0px rgba(236, 72, 153, 0.1)',
    'md': '0 8px 24px rgba(99, 102, 241, 0.15), 6px 6px 0px rgba(16, 185, 129, 0.1)',
    'lg': '0 16px 32px rgba(99, 102, 241, 0.2), 8px 8px 0px rgba(236, 72, 153, 0.15)',
    'xl': '0 24px 48px rgba(99, 102, 241, 0.25), 10px 10px 0px rgba(16, 185, 129, 0.12)',
  },
  fontFamily: {
    sans: ['Poppins', 'system-ui', 'sans-serif'],
  },
}
```

---

## Editorial Monochrome

**Slug:** `editorial-monochrome` | **Category:** Retro & Nostalgic | **Font:** var(--font-sans)

### Colors
| Token | Value |
|-------|-------|
| `--color-white` | `#ffffff` |
| `--color-surface-light` | `#fafafa` |
| `--color-surface` | `#f5f5f5` |
| `--color-text` | `#111111` |
| `--color-text-secondary` | `#333333` |
| `--color-text-tertiary` | `#666666` |
| `--color-primary` | `#000000` |
| `--color-primary-light` | `#f0f0f0` |
| `--color-primary-dark` | `#000000` |
| `--color-secondary` | `#505050` |
| `--color-secondary-light` | `#e8e8e8` |
| `--color-border` | `#e5e5e5` |
| `--color-border-light` | `#ececec` |
| `--color-accent` | `#9a6b5a` |
| `--color-success` | `#1a7a3a` |
| `--color-warning` | `#8b6914` |
| `--color-error` | `#7a1a1a` |
| `--color-info` | `#1a4f7a` |

### Typography
| Token | Value |
|-------|-------|
| `--font-family` | `var(--font-sans)` |
| `--transition` | `all 200ms cubic-bezier(0.25, 0.46, 0.45, 0.94)` |

### Border Radius
| Token | Value |
|-------|-------|
| `--radius-xs` | `0px` |
| `--radius-sm` | `0px` |
| `--radius-default` | `0px` |
| `--radius-md` | `0px` |
| `--radius-lg` | `0px` |
| `--radius-full` | `0px` |

### Shadows
| Token | Value |
|-------|-------|
| `--shadow-xs` | `0 1px 2px rgba(0, 0, 0, 0.04)` |
| `--shadow-sm` | `0 2px 4px rgba(0, 0, 0, 0.08)` |
| `--shadow-md` | `0 4px 8px rgba(0, 0, 0, 0.10)` |
| `--shadow-lg` | `0 8px 16px rgba(0, 0, 0, 0.12)` |
| `--shadow-xl` | `0 12px 24px rgba(0, 0, 0, 0.15)` |

### CSS Variables (copy-paste ready)
```css
:root {
  --color-white: #ffffff;
  --color-surface-light: #fafafa;
  --color-surface: #f5f5f5;
  --color-text: #111111;
  --color-text-secondary: #333333;
  --color-text-tertiary: #666666;
  --color-primary: #000000;
  --color-primary-light: #f0f0f0;
  --color-primary-dark: #000000;
  --color-secondary: #505050;
  --color-secondary-light: #e8e8e8;
  --color-border: #e5e5e5;
  --color-border-light: #ececec;
  --color-accent: #9a6b5a;
  --color-success: #1a7a3a;
  --color-warning: #8b6914;
  --color-error: #7a1a1a;
  --color-info: #1a4f7a;
  --transition: all 200ms cubic-bezier(0.25, 0.46, 0.45, 0.94);
  --font: var(--font-sans);
  --radius-xs: 0px;
  --radius-sm: 0px;
  --radius-default: 0px;
  --radius-md: 0px;
  --radius-lg: 0px;
  --radius-full: 0px;
  --shadow-xs: 0 1px 2px rgba(0, 0, 0, 0.04);
  --shadow-sm: 0 2px 4px rgba(0, 0, 0, 0.08);
  --shadow-md: 0 4px 8px rgba(0, 0, 0, 0.10);
  --shadow-lg: 0 8px 16px rgba(0, 0, 0, 0.12);
  --shadow-xl: 0 12px 24px rgba(0, 0, 0, 0.15);
}
```

### Tailwind Config
```js
// tailwind.config.js theme.extend
{
  colors: {
    'white': '#ffffff',
    'surface-light': '#fafafa',
    'surface': '#f5f5f5',
    'text': '#111111',
    'text-secondary': '#333333',
    'text-tertiary': '#666666',
    'primary': '#000000',
    'primary-light': '#f0f0f0',
    'primary-dark': '#000000',
    'secondary': '#505050',
    'secondary-light': '#e8e8e8',
    'border': '#e5e5e5',
    'border-light': '#ececec',
    'accent': '#9a6b5a',
    'success': '#1a7a3a',
    'warning': '#8b6914',
    'error': '#7a1a1a',
    'info': '#1a4f7a',
  },
  borderRadius: {
    'xs': '0px',
    'sm': '0px',
    'default': '0px',
    'md': '0px',
    'lg': '0px',
    'full': '0px',
  },
  boxShadow: {
    'xs': '0 1px 2px rgba(0, 0, 0, 0.04)',
    'sm': '0 2px 4px rgba(0, 0, 0, 0.08)',
    'md': '0 4px 8px rgba(0, 0, 0, 0.10)',
    'lg': '0 8px 16px rgba(0, 0, 0, 0.12)',
    'xl': '0 12px 24px rgba(0, 0, 0, 0.15)',
  },
  fontFamily: {
    sans: ['var(--font-sans)', 'system-ui', 'sans-serif'],
  },
}
```

---

## Y2k Futurism

**Slug:** `y2k-futurism` | **Category:** Retro & Nostalgic | **Font:** Exo 2

### Colors
| Token | Value |
|-------|-------|
| `--color-white` | `#ffffff` |
| `--color-surface-light` | `#f0f0f0` |
| `--color-surface` | `#e8e8e8` |
| `--color-text` | `#1a1a1a` |
| `--color-text-secondary` | `#4a4a4a` |
| `--color-text-tertiary` | `#777777` |
| `--color-primary` | `#7B68EE` |
| `--color-primary-light` | `#E8DCFF` |
| `--color-primary-dark` | `#5A4BB8` |
| `--color-secondary` | `#FF69B4` |
| `--color-secondary-light` | `#FFE0F0` |
| `--color-chrome` | `#C0C0C0` |
| `--color-chrome-light` | `#E8E8E8` |
| `--color-border` | `#A8A8A8` |
| `--color-border-light` | `#D8D8D8` |
| `--color-success` | `#22c55e` |
| `--color-warning` | `#f59e0b` |
| `--color-error` | `#ef4444` |
| `--color-info` | `#3b82f6` |

### Typography
| Token | Value |
|-------|-------|
| `--font-family` | `'Exo 2', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif` |
| `--transition` | `all 200ms cubic-bezier(0.34, 1.56, 0.64, 1)` |

### Border Radius
| Token | Value |
|-------|-------|
| `--radius-xs` | `2px` |
| `--radius-sm` | `4px` |
| `--radius-default` | `22px` |
| `--radius-md` | `28px` |
| `--radius-lg` | `32px` |
| `--radius-full` | `9999px` |

### Shadows
| Token | Value |
|-------|-------|
| `--shadow-xs` | `0 2px 8px rgba(123, 104, 238, 0.25)` |
| `--shadow-sm` | `0 4px 16px rgba(123, 104, 238, 0.3)` |
| `--shadow-md` | `0 8px 24px rgba(123, 104, 238, 0.35)` |
| `--shadow-lg` | `0 12px 32px rgba(123, 104, 238, 0.4)` |
| `--shadow-xl` | `0 20px 48px rgba(123, 104, 238, 0.45)` |

### CSS Variables (copy-paste ready)
```css
:root {
  --color-white: #ffffff;
  --color-surface-light: #f0f0f0;
  --color-surface: #e8e8e8;
  --color-text: #1a1a1a;
  --color-text-secondary: #4a4a4a;
  --color-text-tertiary: #777777;
  --color-primary: #7B68EE;
  --color-primary-light: #E8DCFF;
  --color-primary-dark: #5A4BB8;
  --color-secondary: #FF69B4;
  --color-secondary-light: #FFE0F0;
  --color-chrome: #C0C0C0;
  --color-chrome-light: #E8E8E8;
  --color-border: #A8A8A8;
  --color-border-light: #D8D8D8;
  --color-success: #22c55e;
  --color-warning: #f59e0b;
  --color-error: #ef4444;
  --color-info: #3b82f6;
  --transition: all 200ms cubic-bezier(0.34, 1.56, 0.64, 1);
  --font: 'Exo 2', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
  --radius-xs: 2px;
  --radius-sm: 4px;
  --radius-default: 22px;
  --radius-md: 28px;
  --radius-lg: 32px;
  --radius-full: 9999px;
  --shadow-xs: 0 2px 8px rgba(123, 104, 238, 0.25);
  --shadow-sm: 0 4px 16px rgba(123, 104, 238, 0.3);
  --shadow-md: 0 8px 24px rgba(123, 104, 238, 0.35);
  --shadow-lg: 0 12px 32px rgba(123, 104, 238, 0.4);
  --shadow-xl: 0 20px 48px rgba(123, 104, 238, 0.45);
}
```

### Tailwind Config
```js
// tailwind.config.js theme.extend
{
  colors: {
    'white': '#ffffff',
    'surface-light': '#f0f0f0',
    'surface': '#e8e8e8',
    'text': '#1a1a1a',
    'text-secondary': '#4a4a4a',
    'text-tertiary': '#777777',
    'primary': '#7B68EE',
    'primary-light': '#E8DCFF',
    'primary-dark': '#5A4BB8',
    'secondary': '#FF69B4',
    'secondary-light': '#FFE0F0',
    'chrome': '#C0C0C0',
    'chrome-light': '#E8E8E8',
    'border': '#A8A8A8',
    'border-light': '#D8D8D8',
    'success': '#22c55e',
    'warning': '#f59e0b',
    'error': '#ef4444',
    'info': '#3b82f6',
  },
  borderRadius: {
    'xs': '2px',
    'sm': '4px',
    'default': '22px',
    'md': '28px',
    'lg': '32px',
    'full': '9999px',
  },
  boxShadow: {
    'xs': '0 2px 8px rgba(123, 104, 238, 0.25)',
    'sm': '0 4px 16px rgba(123, 104, 238, 0.3)',
    'md': '0 8px 24px rgba(123, 104, 238, 0.35)',
    'lg': '0 12px 32px rgba(123, 104, 238, 0.4)',
    'xl': '0 20px 48px rgba(123, 104, 238, 0.45)',
  },
  fontFamily: {
    sans: ['Exo 2', 'system-ui', 'sans-serif'],
  },
}
```

---

## Vaporwave

**Slug:** `vaporwave` | **Category:** Retro & Nostalgic | **Font:** System

### Colors
| Token | Value |
|-------|-------|
| `--color-white` | `#ffffff` |
| `--color-surface-light` | `rgba(255, 255, 255, 0.08)` |
| `--color-surface` | `rgba(255, 255, 255, 0.04)` |
| `--color-text` | `#ffffff` |
| `--color-text-secondary` | `rgba(255, 255, 255, 0.85)` |
| `--color-text-tertiary` | `rgba(255, 255, 255, 0.65)` |
| `--color-primary` | `#FF71CE` |
| `--color-primary-light` | `rgba(255, 113, 206, 0.25)` |
| `--color-primary-dark` | `#E060BD` |
| `--color-secondary` | `#01CDFE` |
| `--color-secondary-light` | `rgba(1, 205, 254, 0.25)` |
| `--color-tertiary` | `#B967FF` |
| `--color-border` | `rgba(255, 113, 206, 0.4)` |
| `--color-border-light` | `rgba(1, 205, 254, 0.3)` |
| `--color-success` | `#22c55e` |
| `--color-warning` | `#f59e0b` |
| `--color-error` | `#ef4444` |
| `--color-info` | `#3b82f6` |

### Typography
| Token | Value |
|-------|-------|
| `--font-family` | `'System', sans-serif` |
| `--transition` | `all 300ms cubic-bezier(0.4, 0, 0.2, 1)` |

### Border Radius
| Token | Value |
|-------|-------|
| `--radius-xs` | `2px` |
| `--radius-sm` | `4px` |
| `--radius-default` | `6px` |
| `--radius-md` | `8px` |
| `--radius-lg` | `12px` |
| `--radius-full` | `9999px` |

### Shadows
| Token | Value |
|-------|-------|
| `--shadow-xs` | `0 0 20px rgba(255, 113, 206, 0.4), 0 0 40px rgba(1, 205, 254, 0.2)` |
| `--shadow-sm` | `0 0 30px rgba(255, 113, 206, 0.5), 0 0 60px rgba(185, 103, 255, 0.3)` |
| `--shadow-md` | `0 0 40px rgba(1, 205, 254, 0.4), 0 0 80px rgba(255, 113, 206, 0.3)` |
| `--shadow-lg` | `0 0 50px rgba(255, 113, 206, 0.6), 0 0 100px rgba(185, 103, 255, 0.4)` |
| `--shadow-xl` | `0 0 80px rgba(185, 103, 255, 0.7), 0 0 120px rgba(1, 205, 254, 0.5)` |

### CSS Variables (copy-paste ready)
```css
:root {
  --color-white: #ffffff;
  --color-surface-light: rgba(255, 255, 255, 0.08);
  --color-surface: rgba(255, 255, 255, 0.04);
  --color-text: #ffffff;
  --color-text-secondary: rgba(255, 255, 255, 0.85);
  --color-text-tertiary: rgba(255, 255, 255, 0.65);
  --color-primary: #FF71CE;
  --color-primary-light: rgba(255, 113, 206, 0.25);
  --color-primary-dark: #E060BD;
  --color-secondary: #01CDFE;
  --color-secondary-light: rgba(1, 205, 254, 0.25);
  --color-tertiary: #B967FF;
  --color-border: rgba(255, 113, 206, 0.4);
  --color-border-light: rgba(1, 205, 254, 0.3);
  --color-success: #22c55e;
  --color-warning: #f59e0b;
  --color-error: #ef4444;
  --color-info: #3b82f6;
  --transition: all 300ms cubic-bezier(0.4, 0, 0.2, 1);
  --radius-xs: 2px;
  --radius-sm: 4px;
  --radius-default: 6px;
  --radius-md: 8px;
  --radius-lg: 12px;
  --radius-full: 9999px;
  --shadow-xs: 0 0 20px rgba(255, 113, 206, 0.4), 0 0 40px rgba(1, 205, 254, 0.2);
  --shadow-sm: 0 0 30px rgba(255, 113, 206, 0.5), 0 0 60px rgba(185, 103, 255, 0.3);
  --shadow-md: 0 0 40px rgba(1, 205, 254, 0.4), 0 0 80px rgba(255, 113, 206, 0.3);
  --shadow-lg: 0 0 50px rgba(255, 113, 206, 0.6), 0 0 100px rgba(185, 103, 255, 0.4);
  --shadow-xl: 0 0 80px rgba(185, 103, 255, 0.7), 0 0 120px rgba(1, 205, 254, 0.5);
}
```

### Tailwind Config
```js
// tailwind.config.js theme.extend
{
  colors: {
    'white': '#ffffff',
    'surface-light': 'rgba(255, 255, 255, 0.08)',
    'surface': 'rgba(255, 255, 255, 0.04)',
    'text': '#ffffff',
    'text-secondary': 'rgba(255, 255, 255, 0.85)',
    'text-tertiary': 'rgba(255, 255, 255, 0.65)',
    'primary': '#FF71CE',
    'primary-light': 'rgba(255, 113, 206, 0.25)',
    'primary-dark': '#E060BD',
    'secondary': '#01CDFE',
    'secondary-light': 'rgba(1, 205, 254, 0.25)',
    'tertiary': '#B967FF',
    'border': 'rgba(255, 113, 206, 0.4)',
    'border-light': 'rgba(1, 205, 254, 0.3)',
    'success': '#22c55e',
    'warning': '#f59e0b',
    'error': '#ef4444',
    'info': '#3b82f6',
  },
  borderRadius: {
    'xs': '2px',
    'sm': '4px',
    'default': '6px',
    'md': '8px',
    'lg': '12px',
    'full': '9999px',
  },
  boxShadow: {
    'xs': '0 0 20px rgba(255, 113, 206, 0.4), 0 0 40px rgba(1, 205, 254, 0.2)',
    'sm': '0 0 30px rgba(255, 113, 206, 0.5), 0 0 60px rgba(185, 103, 255, 0.3)',
    'md': '0 0 40px rgba(1, 205, 254, 0.4), 0 0 80px rgba(255, 113, 206, 0.3)',
    'lg': '0 0 50px rgba(255, 113, 206, 0.6), 0 0 100px rgba(185, 103, 255, 0.4)',
    'xl': '0 0 80px rgba(185, 103, 255, 0.7), 0 0 120px rgba(1, 205, 254, 0.5)',
  },
  fontFamily: {
    sans: ['System', 'system-ui', 'sans-serif'],
  },
}
```

---

## Synthwave

**Slug:** `synthwave` | **Category:** Retro & Nostalgic | **Font:** Rajdhani

### Colors
| Token | Value |
|-------|-------|
| `--color-white` | `#ffffff` |
| `--color-surface-light` | `rgba(255, 255, 255, 0.05)` |
| `--color-surface` | `rgba(255, 255, 255, 0.03)` |
| `--color-text` | `#ffffff` |
| `--color-text-secondary` | `rgba(255, 255, 255, 0.85)` |
| `--color-text-tertiary` | `rgba(255, 255, 255, 0.7)` |
| `--color-primary` | `#FF2D95` |
| `--color-primary-light` | `rgba(255, 45, 149, 0.2)` |
| `--color-primary-dark` | `#E01B7A` |
| `--color-secondary` | `#00F0FF` |
| `--color-secondary-light` | `rgba(0, 240, 255, 0.2)` |
| `--color-border` | `rgba(255, 45, 149, 0.2)` |
| `--color-border-light` | `rgba(0, 240, 255, 0.15)` |
| `--color-success` | `#00FF85` |
| `--color-warning` | `#FFD500` |
| `--color-error` | `#FF006E` |
| `--color-info` | `#00B4FF` |

### Typography
| Token | Value |
|-------|-------|
| `--font-family` | `'Rajdhani', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif` |
| `--transition` | `all 250ms ease-out` |

### Border Radius
| Token | Value |
|-------|-------|
| `--radius-xs` | `2px` |
| `--radius-sm` | `4px` |
| `--radius-default` | `6px` |
| `--radius-md` | `8px` |
| `--radius-lg` | `12px` |
| `--radius-full` | `9999px` |

### Shadows
| Token | Value |
|-------|-------|
| `--shadow-xs` | `0 0 10px rgba(255, 45, 149, 0.4)` |
| `--shadow-sm` | `0 0 20px rgba(255, 45, 149, 0.5)` |
| `--shadow-md` | `0 0 30px rgba(0, 240, 255, 0.4)` |
| `--shadow-lg` | `0 0 50px rgba(255, 45, 149, 0.6)` |
| `--shadow-xl` | `0 0 80px rgba(255, 45, 149, 0.8)` |

### CSS Variables (copy-paste ready)
```css
:root {
  --color-white: #ffffff;
  --color-surface-light: rgba(255, 255, 255, 0.05);
  --color-surface: rgba(255, 255, 255, 0.03);
  --color-text: #ffffff;
  --color-text-secondary: rgba(255, 255, 255, 0.85);
  --color-text-tertiary: rgba(255, 255, 255, 0.7);
  --color-primary: #FF2D95;
  --color-primary-light: rgba(255, 45, 149, 0.2);
  --color-primary-dark: #E01B7A;
  --color-secondary: #00F0FF;
  --color-secondary-light: rgba(0, 240, 255, 0.2);
  --color-border: rgba(255, 45, 149, 0.2);
  --color-border-light: rgba(0, 240, 255, 0.15);
  --color-success: #00FF85;
  --color-warning: #FFD500;
  --color-error: #FF006E;
  --color-info: #00B4FF;
  --transition: all 250ms ease-out;
  --font: 'Rajdhani', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
  --radius-xs: 2px;
  --radius-sm: 4px;
  --radius-default: 6px;
  --radius-md: 8px;
  --radius-lg: 12px;
  --radius-full: 9999px;
  --shadow-xs: 0 0 10px rgba(255, 45, 149, 0.4);
  --shadow-sm: 0 0 20px rgba(255, 45, 149, 0.5);
  --shadow-md: 0 0 30px rgba(0, 240, 255, 0.4);
  --shadow-lg: 0 0 50px rgba(255, 45, 149, 0.6);
  --shadow-xl: 0 0 80px rgba(255, 45, 149, 0.8);
}
```

### Tailwind Config
```js
// tailwind.config.js theme.extend
{
  colors: {
    'white': '#ffffff',
    'surface-light': 'rgba(255, 255, 255, 0.05)',
    'surface': 'rgba(255, 255, 255, 0.03)',
    'text': '#ffffff',
    'text-secondary': 'rgba(255, 255, 255, 0.85)',
    'text-tertiary': 'rgba(255, 255, 255, 0.7)',
    'primary': '#FF2D95',
    'primary-light': 'rgba(255, 45, 149, 0.2)',
    'primary-dark': '#E01B7A',
    'secondary': '#00F0FF',
    'secondary-light': 'rgba(0, 240, 255, 0.2)',
    'border': 'rgba(255, 45, 149, 0.2)',
    'border-light': 'rgba(0, 240, 255, 0.15)',
    'success': '#00FF85',
    'warning': '#FFD500',
    'error': '#FF006E',
    'info': '#00B4FF',
  },
  borderRadius: {
    'xs': '2px',
    'sm': '4px',
    'default': '6px',
    'md': '8px',
    'lg': '12px',
    'full': '9999px',
  },
  boxShadow: {
    'xs': '0 0 10px rgba(255, 45, 149, 0.4)',
    'sm': '0 0 20px rgba(255, 45, 149, 0.5)',
    'md': '0 0 30px rgba(0, 240, 255, 0.4)',
    'lg': '0 0 50px rgba(255, 45, 149, 0.6)',
    'xl': '0 0 80px rgba(255, 45, 149, 0.8)',
  },
  fontFamily: {
    sans: ['Rajdhani', 'system-ui', 'sans-serif'],
  },
}
```

---

## Pixel Retro

**Slug:** `pixel-retro` | **Category:** Retro & Nostalgic | **Font:** Press Start 2P

### Colors
| Token | Value |
|-------|-------|
| `--color-white` | `#ffffff` |
| `--color-surface-light` | `#3A3E52` |
| `--color-surface` | `#2A2D3E` |
| `--color-text` | `#ffffff` |
| `--color-text-secondary` | `#a8aac0` |
| `--color-text-tertiary` | `#8a8c9a` |
| `--color-primary` | `#4ADE80` |
| `--color-primary-light` | `rgba(74, 222, 128, 0.2)` |
| `--color-primary-dark` | `#22C452` |
| `--color-secondary` | `#FBBF24` |
| `--color-secondary-light` | `rgba(251, 191, 36, 0.2)` |
| `--color-border` | `#454A5E` |
| `--color-border-light` | `#3A3E52` |
| `--color-success` | `#4ADE80` |
| `--color-warning` | `#FBBF24` |
| `--color-error` | `#EF4444` |
| `--color-info` | `#3B82F6` |

### Typography
| Token | Value |
|-------|-------|
| `--font-family` | `'Press Start 2P', monospace` |
| `--transition` | `all 100ms linear` |

### Border Radius
| Token | Value |
|-------|-------|
| `--radius-xs` | `0px` |
| `--radius-sm` | `0px` |
| `--radius-default` | `0px` |
| `--radius-md` | `0px` |
| `--radius-lg` | `0px` |
| `--radius-full` | `0px` |

### Shadows
| Token | Value |
|-------|-------|
| `--shadow-xs` | `0 2px 4px rgba(0, 0, 0, 0.5)` |
| `--shadow-sm` | `0 4px 8px rgba(0, 0, 0, 0.6)` |
| `--shadow-md` | `0 8px 16px rgba(0, 0, 0, 0.7)` |
| `--shadow-lg` | `0 12px 24px rgba(0, 0, 0, 0.8)` |
| `--shadow-xl` | `0 16px 32px rgba(0, 0, 0, 0.9)` |

### CSS Variables (copy-paste ready)
```css
:root {
  --color-white: #ffffff;
  --color-surface-light: #3A3E52;
  --color-surface: #2A2D3E;
  --color-text: #ffffff;
  --color-text-secondary: #a8aac0;
  --color-text-tertiary: #8a8c9a;
  --color-primary: #4ADE80;
  --color-primary-light: rgba(74, 222, 128, 0.2);
  --color-primary-dark: #22C452;
  --color-secondary: #FBBF24;
  --color-secondary-light: rgba(251, 191, 36, 0.2);
  --color-border: #454A5E;
  --color-border-light: #3A3E52;
  --color-success: #4ADE80;
  --color-warning: #FBBF24;
  --color-error: #EF4444;
  --color-info: #3B82F6;
  --transition: all 100ms linear;
  --font: 'Press Start 2P', monospace;
  --radius-xs: 0px;
  --radius-sm: 0px;
  --radius-default: 0px;
  --radius-md: 0px;
  --radius-lg: 0px;
  --radius-full: 0px;
  --shadow-xs: 0 2px 4px rgba(0, 0, 0, 0.5);
  --shadow-sm: 0 4px 8px rgba(0, 0, 0, 0.6);
  --shadow-md: 0 8px 16px rgba(0, 0, 0, 0.7);
  --shadow-lg: 0 12px 24px rgba(0, 0, 0, 0.8);
  --shadow-xl: 0 16px 32px rgba(0, 0, 0, 0.9);
}
```

### Tailwind Config
```js
// tailwind.config.js theme.extend
{
  colors: {
    'white': '#ffffff',
    'surface-light': '#3A3E52',
    'surface': '#2A2D3E',
    'text': '#ffffff',
    'text-secondary': '#a8aac0',
    'text-tertiary': '#8a8c9a',
    'primary': '#4ADE80',
    'primary-light': 'rgba(74, 222, 128, 0.2)',
    'primary-dark': '#22C452',
    'secondary': '#FBBF24',
    'secondary-light': 'rgba(251, 191, 36, 0.2)',
    'border': '#454A5E',
    'border-light': '#3A3E52',
    'success': '#4ADE80',
    'warning': '#FBBF24',
    'error': '#EF4444',
    'info': '#3B82F6',
  },
  borderRadius: {
    'xs': '0px',
    'sm': '0px',
    'default': '0px',
    'md': '0px',
    'lg': '0px',
    'full': '0px',
  },
  boxShadow: {
    'xs': '0 2px 4px rgba(0, 0, 0, 0.5)',
    'sm': '0 4px 8px rgba(0, 0, 0, 0.6)',
    'md': '0 8px 16px rgba(0, 0, 0, 0.7)',
    'lg': '0 12px 24px rgba(0, 0, 0, 0.8)',
    'xl': '0 16px 32px rgba(0, 0, 0, 0.9)',
  },
  fontFamily: {
    sans: ['Press Start 2P', 'system-ui', 'sans-serif'],
  },
}
```

---

## Skeuomorphic

**Slug:** `skeuomorphic` | **Category:** Tactile & Organic | **Font:** Verdana

### Colors
| Token | Value |
|-------|-------|
| `--color-white` | `#ffffff` |
| `--color-surface-light` | `#F9F6F1` |
| `--color-surface` | `#FFFFFF` |
| `--color-text` | `#2C2C2C` |
| `--color-text-secondary` | `#555555` |
| `--color-text-tertiary` | `#888888` |
| `--color-primary` | `#2E5090` |
| `--color-primary-light` | `rgba(46, 80, 144, 0.1)` |
| `--color-primary-dark` | `#1F3860` |
| `--color-secondary` | `#8B4513` |
| `--color-secondary-light` | `rgba(139, 69, 19, 0.1)` |
| `--color-border` | `#B0B0B0` |
| `--color-border-light` | `#D9D9D9` |
| `--color-success` | `#22c55e` |
| `--color-warning` | `#f59e0b` |
| `--color-error` | `#ef4444` |
| `--color-info` | `#3b82f6` |

### Typography
| Token | Value |
|-------|-------|
| `--font-family` | `'Verdana', sans-serif` |
| `--transition` | `all 150ms ease-in-out` |

### Border Radius
| Token | Value |
|-------|-------|
| `--radius-xs` | `2px` |
| `--radius-sm` | `4px` |
| `--radius-default` | `6px` |
| `--radius-md` | `8px` |
| `--radius-lg` | `12px` |
| `--radius-full` | `9999px` |

### Shadows
| Token | Value |
|-------|-------|
| `--shadow-xs` | `inset 0 1px 2px rgba(255, 255, 255, 0.5), inset 0 -2px 3px rgba(0, 0, 0, 0.2), 0 2px 4px rgba(0, 0, 0, 0.1)` |
| `--shadow-sm` | `inset 0 1px 3px rgba(255, 255, 255, 0.6), inset 0 -3px 5px rgba(0, 0, 0, 0.25), 0 4px 8px rgba(0, 0, 0, 0.15)` |
| `--shadow-md` | `inset 0 1px 4px rgba(255, 255, 255, 0.8), inset 0 -4px 8px rgba(0, 0, 0, 0.2), 0 6px 12px rgba(0, 0, 0, 0.15)` |
| `--shadow-lg` | `inset 0 2px 6px rgba(255, 255, 255, 0.8), inset 0 -6px 12px rgba(0, 0, 0, 0.25), 0 10px 20px rgba(0, 0, 0, 0.2)` |
| `--shadow-xl` | `inset 0 2px 8px rgba(255, 255, 255, 0.8), inset 0 -8px 16px rgba(0, 0, 0, 0.3), 0 15px 30px rgba(0, 0, 0, 0.25)` |

### CSS Variables (copy-paste ready)
```css
:root {
  --color-white: #ffffff;
  --color-surface-light: #F9F6F1;
  --color-surface: #FFFFFF;
  --color-text: #2C2C2C;
  --color-text-secondary: #555555;
  --color-text-tertiary: #888888;
  --color-primary: #2E5090;
  --color-primary-light: rgba(46, 80, 144, 0.1);
  --color-primary-dark: #1F3860;
  --color-secondary: #8B4513;
  --color-secondary-light: rgba(139, 69, 19, 0.1);
  --color-border: #B0B0B0;
  --color-border-light: #D9D9D9;
  --color-success: #22c55e;
  --color-warning: #f59e0b;
  --color-error: #ef4444;
  --color-info: #3b82f6;
  --transition: all 150ms ease-in-out;
  --font: 'Verdana', sans-serif;
  --radius-xs: 2px;
  --radius-sm: 4px;
  --radius-default: 6px;
  --radius-md: 8px;
  --radius-lg: 12px;
  --radius-full: 9999px;
  --shadow-xs: inset 0 1px 2px rgba(255, 255, 255, 0.5), inset 0 -2px 3px rgba(0, 0, 0, 0.2), 0 2px 4px rgba(0, 0, 0, 0.1);
  --shadow-sm: inset 0 1px 3px rgba(255, 255, 255, 0.6), inset 0 -3px 5px rgba(0, 0, 0, 0.25), 0 4px 8px rgba(0, 0, 0, 0.15);
  --shadow-md: inset 0 1px 4px rgba(255, 255, 255, 0.8), inset 0 -4px 8px rgba(0, 0, 0, 0.2), 0 6px 12px rgba(0, 0, 0, 0.15);
  --shadow-lg: inset 0 2px 6px rgba(255, 255, 255, 0.8), inset 0 -6px 12px rgba(0, 0, 0, 0.25), 0 10px 20px rgba(0, 0, 0, 0.2);
  --shadow-xl: inset 0 2px 8px rgba(255, 255, 255, 0.8), inset 0 -8px 16px rgba(0, 0, 0, 0.3), 0 15px 30px rgba(0, 0, 0, 0.25);
}
```

### Tailwind Config
```js
// tailwind.config.js theme.extend
{
  colors: {
    'white': '#ffffff',
    'surface-light': '#F9F6F1',
    'surface': '#FFFFFF',
    'text': '#2C2C2C',
    'text-secondary': '#555555',
    'text-tertiary': '#888888',
    'primary': '#2E5090',
    'primary-light': 'rgba(46, 80, 144, 0.1)',
    'primary-dark': '#1F3860',
    'secondary': '#8B4513',
    'secondary-light': 'rgba(139, 69, 19, 0.1)',
    'border': '#B0B0B0',
    'border-light': '#D9D9D9',
    'success': '#22c55e',
    'warning': '#f59e0b',
    'error': '#ef4444',
    'info': '#3b82f6',
  },
  borderRadius: {
    'xs': '2px',
    'sm': '4px',
    'default': '6px',
    'md': '8px',
    'lg': '12px',
    'full': '9999px',
  },
  boxShadow: {
    'xs': 'inset 0 1px 2px rgba(255, 255, 255, 0.5), inset 0 -2px 3px rgba(0, 0, 0, 0.2), 0 2px 4px rgba(0, 0, 0, 0.1)',
    'sm': 'inset 0 1px 3px rgba(255, 255, 255, 0.6), inset 0 -3px 5px rgba(0, 0, 0, 0.25), 0 4px 8px rgba(0, 0, 0, 0.15)',
    'md': 'inset 0 1px 4px rgba(255, 255, 255, 0.8), inset 0 -4px 8px rgba(0, 0, 0, 0.2), 0 6px 12px rgba(0, 0, 0, 0.15)',
    'lg': 'inset 0 2px 6px rgba(255, 255, 255, 0.8), inset 0 -6px 12px rgba(0, 0, 0, 0.25), 0 10px 20px rgba(0, 0, 0, 0.2)',
    'xl': 'inset 0 2px 8px rgba(255, 255, 255, 0.8), inset 0 -8px 16px rgba(0, 0, 0, 0.3), 0 15px 30px rgba(0, 0, 0, 0.25)',
  },
  fontFamily: {
    sans: ['Verdana', 'system-ui', 'sans-serif'],
  },
}
```

---

## Terminal Hacker

**Slug:** `terminal-hacker` | **Category:** Tactile & Organic | **Font:** JetBrains Mono

### Colors
| Token | Value |
|-------|-------|
| `--color-white` | `#ffffff` |
| `--color-surface-light` | `rgba(0, 255, 65, 0.05)` |
| `--color-surface` | `#0F0A12` |
| `--color-text` | `#00FF41` |
| `--color-text-secondary` | `rgba(0, 255, 65, 0.8)` |
| `--color-text-tertiary` | `rgba(0, 255, 65, 0.6)` |
| `--color-primary` | `#00FF41` |
| `--color-primary-light` | `rgba(0, 255, 65, 0.15)` |
| `--color-primary-dark` | `#00CC33` |
| `--color-secondary` | `#FFB000` |
| `--color-secondary-light` | `rgba(255, 176, 0, 0.15)` |
| `--color-border` | `rgba(0, 255, 65, 0.2)` |
| `--color-border-light` | `rgba(0, 255, 65, 0.1)` |
| `--color-success` | `#00FF41` |
| `--color-warning` | `#FFB000` |
| `--color-error` | `#FF0000` |
| `--color-info` | `#00D9FF` |

### Typography
| Token | Value |
|-------|-------|
| `--font-family` | `'JetBrains Mono', monospace` |
| `--transition` | `all 100ms ease-out` |

### Border Radius
| Token | Value |
|-------|-------|
| `--radius-xs` | `0px` |
| `--radius-sm` | `0px` |
| `--radius-default` | `0px` |
| `--radius-md` | `0px` |
| `--radius-lg` | `0px` |
| `--radius-full` | `0px` |

### Shadows
| Token | Value |
|-------|-------|
| `--shadow-xs` | `0 0 10px rgba(0, 255, 65, 0.2)` |
| `--shadow-sm` | `0 0 20px rgba(0, 255, 65, 0.3)` |
| `--shadow-md` | `0 0 30px rgba(0, 255, 65, 0.4)` |
| `--shadow-lg` | `0 0 50px rgba(0, 255, 65, 0.5)` |
| `--shadow-xl` | `0 0 80px rgba(0, 255, 65, 0.6)` |

### CSS Variables (copy-paste ready)
```css
:root {
  --color-white: #ffffff;
  --color-surface-light: rgba(0, 255, 65, 0.05);
  --color-surface: #0F0A12;
  --color-text: #00FF41;
  --color-text-secondary: rgba(0, 255, 65, 0.8);
  --color-text-tertiary: rgba(0, 255, 65, 0.6);
  --color-primary: #00FF41;
  --color-primary-light: rgba(0, 255, 65, 0.15);
  --color-primary-dark: #00CC33;
  --color-secondary: #FFB000;
  --color-secondary-light: rgba(255, 176, 0, 0.15);
  --color-border: rgba(0, 255, 65, 0.2);
  --color-border-light: rgba(0, 255, 65, 0.1);
  --color-success: #00FF41;
  --color-warning: #FFB000;
  --color-error: #FF0000;
  --color-info: #00D9FF;
  --transition: all 100ms ease-out;
  --font: 'JetBrains Mono', monospace;
  --radius-xs: 0px;
  --radius-sm: 0px;
  --radius-default: 0px;
  --radius-md: 0px;
  --radius-lg: 0px;
  --radius-full: 0px;
  --shadow-xs: 0 0 10px rgba(0, 255, 65, 0.2);
  --shadow-sm: 0 0 20px rgba(0, 255, 65, 0.3);
  --shadow-md: 0 0 30px rgba(0, 255, 65, 0.4);
  --shadow-lg: 0 0 50px rgba(0, 255, 65, 0.5);
  --shadow-xl: 0 0 80px rgba(0, 255, 65, 0.6);
}
```

### Tailwind Config
```js
// tailwind.config.js theme.extend
{
  colors: {
    'white': '#ffffff',
    'surface-light': 'rgba(0, 255, 65, 0.05)',
    'surface': '#0F0A12',
    'text': '#00FF41',
    'text-secondary': 'rgba(0, 255, 65, 0.8)',
    'text-tertiary': 'rgba(0, 255, 65, 0.6)',
    'primary': '#00FF41',
    'primary-light': 'rgba(0, 255, 65, 0.15)',
    'primary-dark': '#00CC33',
    'secondary': '#FFB000',
    'secondary-light': 'rgba(255, 176, 0, 0.15)',
    'border': 'rgba(0, 255, 65, 0.2)',
    'border-light': 'rgba(0, 255, 65, 0.1)',
    'success': '#00FF41',
    'warning': '#FFB000',
    'error': '#FF0000',
    'info': '#00D9FF',
  },
  borderRadius: {
    'xs': '0px',
    'sm': '0px',
    'default': '0px',
    'md': '0px',
    'lg': '0px',
    'full': '0px',
  },
  boxShadow: {
    'xs': '0 0 10px rgba(0, 255, 65, 0.2)',
    'sm': '0 0 20px rgba(0, 255, 65, 0.3)',
    'md': '0 0 30px rgba(0, 255, 65, 0.4)',
    'lg': '0 0 50px rgba(0, 255, 65, 0.5)',
    'xl': '0 0 80px rgba(0, 255, 65, 0.6)',
  },
  fontFamily: {
    sans: ['JetBrains Mono', 'system-ui', 'sans-serif'],
  },
}
```

---

## Warm Soft

**Slug:** `warm-soft` | **Category:** Tactile & Organic | **Font:** Nunito

### Colors
| Token | Value |
|-------|-------|
| `--color-white` | `#ffffff` |
| `--color-surface-light` | `#fff3eb` |
| `--color-surface` | `#fff9f5` |
| `--color-accent-bg` | `#ffe8d6` |
| `--color-text` | `#3d405b` |
| `--color-text-secondary` | `#6b6e82` |
| `--color-text-tertiary` | `#9b9dae` |
| `--color-primary` | `#e07a5f` |
| `--color-primary-light` | `#ffe8d6` |
| `--color-primary-dark` | `#d4644f` |
| `--color-secondary` | `#81b29a` |
| `--color-secondary-light` | `#e6f3ee` |
| `--color-accent` | `#f2cc8f` |
| `--color-border` | `#ede5da` |
| `--color-border-light` | `#faf6f1` |
| `--color-success` | `#81b29a` |
| `--color-warning` | `#f2cc8f` |
| `--color-error` | `#d4544d` |
| `--color-info` | `#a9a9db` |

### Typography
| Token | Value |
|-------|-------|
| `--font-family` | `'Nunito', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif` |
| `--transition` | `all 150ms ease-in-out` |

### Border Radius
| Token | Value |
|-------|-------|
| `--radius-xs` | `4px` |
| `--radius-sm` | `8px` |
| `--radius-default` | `12px` |
| `--radius-md` | `12px` |
| `--radius-lg` | `16px` |
| `--radius-xl` | `24px` |
| `--radius-full` | `9999px` |

### Shadows
| Token | Value |
|-------|-------|
| `--shadow-xs` | `0 1px 3px rgba(224, 122, 95, 0.08)` |
| `--shadow-sm` | `0 4px 16px rgba(224, 122, 95, 0.12)` |
| `--shadow-md` | `0 8px 24px rgba(224, 122, 95, 0.15)` |
| `--shadow-lg` | `0 12px 40px rgba(224, 122, 95, 0.18)` |
| `--shadow-xl` | `0 20px 56px rgba(224, 122, 95, 0.22)` |

### CSS Variables (copy-paste ready)
```css
:root {
  --color-white: #ffffff;
  --color-surface-light: #fff3eb;
  --color-surface: #fff9f5;
  --color-accent-bg: #ffe8d6;
  --color-text: #3d405b;
  --color-text-secondary: #6b6e82;
  --color-text-tertiary: #9b9dae;
  --color-primary: #e07a5f;
  --color-primary-light: #ffe8d6;
  --color-primary-dark: #d4644f;
  --color-secondary: #81b29a;
  --color-secondary-light: #e6f3ee;
  --color-accent: #f2cc8f;
  --color-border: #ede5da;
  --color-border-light: #faf6f1;
  --color-success: #81b29a;
  --color-warning: #f2cc8f;
  --color-error: #d4544d;
  --color-info: #a9a9db;
  --transition: all 150ms ease-in-out;
  --font: 'Nunito', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
  --radius-xs: 4px;
  --radius-sm: 8px;
  --radius-default: 12px;
  --radius-md: 12px;
  --radius-lg: 16px;
  --radius-xl: 24px;
  --radius-full: 9999px;
  --shadow-xs: 0 1px 3px rgba(224, 122, 95, 0.08);
  --shadow-sm: 0 4px 16px rgba(224, 122, 95, 0.12);
  --shadow-md: 0 8px 24px rgba(224, 122, 95, 0.15);
  --shadow-lg: 0 12px 40px rgba(224, 122, 95, 0.18);
  --shadow-xl: 0 20px 56px rgba(224, 122, 95, 0.22);
}
```

### Tailwind Config
```js
// tailwind.config.js theme.extend
{
  colors: {
    'white': '#ffffff',
    'surface-light': '#fff3eb',
    'surface': '#fff9f5',
    'accent-bg': '#ffe8d6',
    'text': '#3d405b',
    'text-secondary': '#6b6e82',
    'text-tertiary': '#9b9dae',
    'primary': '#e07a5f',
    'primary-light': '#ffe8d6',
    'primary-dark': '#d4644f',
    'secondary': '#81b29a',
    'secondary-light': '#e6f3ee',
    'accent': '#f2cc8f',
    'border': '#ede5da',
    'border-light': '#faf6f1',
    'success': '#81b29a',
    'warning': '#f2cc8f',
    'error': '#d4544d',
    'info': '#a9a9db',
  },
  borderRadius: {
    'xs': '4px',
    'sm': '8px',
    'default': '12px',
    'md': '12px',
    'lg': '16px',
    'xl': '24px',
    'full': '9999px',
  },
  boxShadow: {
    'xs': '0 1px 3px rgba(224, 122, 95, 0.08)',
    'sm': '0 4px 16px rgba(224, 122, 95, 0.12)',
    'md': '0 8px 24px rgba(224, 122, 95, 0.15)',
    'lg': '0 12px 40px rgba(224, 122, 95, 0.18)',
    'xl': '0 20px 56px rgba(224, 122, 95, 0.22)',
  },
  fontFamily: {
    sans: ['Nunito', 'system-ui', 'sans-serif'],
  },
}
```

---

## Organic Earth

**Slug:** `organic-earth` | **Category:** Tactile & Organic | **Font:** Source Sans 3

### Colors
| Token | Value |
|-------|-------|
| `--color-white` | `#ffffff` |
| `--color-surface-light` | `#FBF8F3` |
| `--color-surface` | `#FAF5EF` |
| `--color-text` | `#3C3C3C` |
| `--color-text-secondary` | `#6B6B6B` |
| `--color-text-tertiary` | `#999999` |
| `--color-primary` | `#8B7355` |
| `--color-primary-light` | `#E8DFD0` |
| `--color-primary-dark` | `#6B5743` |
| `--color-secondary` | `#6B8E23` |
| `--color-secondary-light` | `#E6EED6` |
| `--color-border` | `#D4C5B2` |
| `--color-border-light` | `#E8DFD0` |
| `--color-success` | `#2D5016` |
| `--color-warning` | `#C89858` |
| `--color-error` | `#A0573D` |
| `--color-info` | `#5B7C5B` |

### Typography
| Token | Value |
|-------|-------|
| `--font-family` | `'Source Sans 3', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif` |
| `--transition` | `all 200ms cubic-bezier(0.25, 0.46, 0.45, 0.94)` |

### Border Radius
| Token | Value |
|-------|-------|
| `--radius-xs` | `4px` |
| `--radius-sm` | `6px` |
| `--radius-default` | `8px` |
| `--radius-md` | `10px` |
| `--radius-lg` | `12px` |
| `--radius-full` | `9999px` |

### Shadows
| Token | Value |
|-------|-------|
| `--shadow-xs` | `0 2px 4px rgba(93, 64, 55, 0.08)` |
| `--shadow-sm` | `0 4px 8px rgba(93, 64, 55, 0.12)` |
| `--shadow-md` | `0 8px 16px rgba(93, 64, 55, 0.15)` |
| `--shadow-lg` | `0 12px 24px rgba(93, 64, 55, 0.18)` |
| `--shadow-xl` | `0 16px 32px rgba(93, 64, 55, 0.2)` |

### CSS Variables (copy-paste ready)
```css
:root {
  --color-white: #ffffff;
  --color-surface-light: #FBF8F3;
  --color-surface: #FAF5EF;
  --color-text: #3C3C3C;
  --color-text-secondary: #6B6B6B;
  --color-text-tertiary: #999999;
  --color-primary: #8B7355;
  --color-primary-light: #E8DFD0;
  --color-primary-dark: #6B5743;
  --color-secondary: #6B8E23;
  --color-secondary-light: #E6EED6;
  --color-border: #D4C5B2;
  --color-border-light: #E8DFD0;
  --color-success: #2D5016;
  --color-warning: #C89858;
  --color-error: #A0573D;
  --color-info: #5B7C5B;
  --transition: all 200ms cubic-bezier(0.25, 0.46, 0.45, 0.94);
  --font: 'Source Sans 3', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
  --radius-xs: 4px;
  --radius-sm: 6px;
  --radius-default: 8px;
  --radius-md: 10px;
  --radius-lg: 12px;
  --radius-full: 9999px;
  --shadow-xs: 0 2px 4px rgba(93, 64, 55, 0.08);
  --shadow-sm: 0 4px 8px rgba(93, 64, 55, 0.12);
  --shadow-md: 0 8px 16px rgba(93, 64, 55, 0.15);
  --shadow-lg: 0 12px 24px rgba(93, 64, 55, 0.18);
  --shadow-xl: 0 16px 32px rgba(93, 64, 55, 0.2);
}
```

### Tailwind Config
```js
// tailwind.config.js theme.extend
{
  colors: {
    'white': '#ffffff',
    'surface-light': '#FBF8F3',
    'surface': '#FAF5EF',
    'text': '#3C3C3C',
    'text-secondary': '#6B6B6B',
    'text-tertiary': '#999999',
    'primary': '#8B7355',
    'primary-light': '#E8DFD0',
    'primary-dark': '#6B5743',
    'secondary': '#6B8E23',
    'secondary-light': '#E6EED6',
    'border': '#D4C5B2',
    'border-light': '#E8DFD0',
    'success': '#2D5016',
    'warning': '#C89858',
    'error': '#A0573D',
    'info': '#5B7C5B',
  },
  borderRadius: {
    'xs': '4px',
    'sm': '6px',
    'default': '8px',
    'md': '10px',
    'lg': '12px',
    'full': '9999px',
  },
  boxShadow: {
    'xs': '0 2px 4px rgba(93, 64, 55, 0.08)',
    'sm': '0 4px 8px rgba(93, 64, 55, 0.12)',
    'md': '0 8px 16px rgba(93, 64, 55, 0.15)',
    'lg': '0 12px 24px rgba(93, 64, 55, 0.18)',
    'xl': '0 16px 32px rgba(93, 64, 55, 0.2)',
  },
  fontFamily: {
    sans: ['Source Sans 3', 'system-ui', 'sans-serif'],
  },
}
```

---

## Zen Wabi Sabi

**Slug:** `zen-wabi-sabi` | **Category:** Tactile & Organic | **Font:** Noto Sans

### Colors
| Token | Value |
|-------|-------|
| `--color-white` | `#ffffff` |
| `--color-surface-light` | `#FDFCF9` |
| `--color-surface` | `#F5F0EB` |
| `--color-text` | `#2C2C2C` |
| `--color-text-secondary` | `#5A5A5A` |
| `--color-text-tertiary` | `#888888` |
| `--color-primary` | `#8B6914` |
| `--color-primary-light` | `#EBE5D9` |
| `--color-primary-dark` | `#6B5410` |
| `--color-secondary` | `#7A7A7A` |
| `--color-secondary-light` | `#EFEFEF` |
| `--color-border` | `#D4C9BC` |
| `--color-border-light` | `#E8E3DB` |
| `--color-success` | `#5A6B52` |
| `--color-warning` | `#A68B5B` |
| `--color-error` | `#8B5A52` |
| `--color-info` | `#6B7A8B` |

### Typography
| Token | Value |
|-------|-------|
| `--font-family` | `'Noto Sans', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif` |
| `--transition` | `all 300ms ease-in-out` |

### Border Radius
| Token | Value |
|-------|-------|
| `--radius-xs` | `2px` |
| `--radius-sm` | `2px` |
| `--radius-default` | `3px` |
| `--radius-md` | `4px` |
| `--radius-lg` | `4px` |
| `--radius-full` | `9999px` |

### Shadows
| Token | Value |
|-------|-------|
| `--shadow-xs` | `0 1px 2px rgba(0, 0, 0, 0.04)` |
| `--shadow-sm` | `0 2px 4px rgba(0, 0, 0, 0.06)` |
| `--shadow-md` | `0 4px 8px rgba(0, 0, 0, 0.08)` |
| `--shadow-lg` | `0 8px 16px rgba(0, 0, 0, 0.1)` |
| `--shadow-xl` | `0 12px 24px rgba(0, 0, 0, 0.12)` |

### CSS Variables (copy-paste ready)
```css
:root {
  --color-white: #ffffff;
  --color-surface-light: #FDFCF9;
  --color-surface: #F5F0EB;
  --color-text: #2C2C2C;
  --color-text-secondary: #5A5A5A;
  --color-text-tertiary: #888888;
  --color-primary: #8B6914;
  --color-primary-light: #EBE5D9;
  --color-primary-dark: #6B5410;
  --color-secondary: #7A7A7A;
  --color-secondary-light: #EFEFEF;
  --color-border: #D4C9BC;
  --color-border-light: #E8E3DB;
  --color-success: #5A6B52;
  --color-warning: #A68B5B;
  --color-error: #8B5A52;
  --color-info: #6B7A8B;
  --transition: all 300ms ease-in-out;
  --font: 'Noto Sans', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
  --radius-xs: 2px;
  --radius-sm: 2px;
  --radius-default: 3px;
  --radius-md: 4px;
  --radius-lg: 4px;
  --radius-full: 9999px;
  --shadow-xs: 0 1px 2px rgba(0, 0, 0, 0.04);
  --shadow-sm: 0 2px 4px rgba(0, 0, 0, 0.06);
  --shadow-md: 0 4px 8px rgba(0, 0, 0, 0.08);
  --shadow-lg: 0 8px 16px rgba(0, 0, 0, 0.1);
  --shadow-xl: 0 12px 24px rgba(0, 0, 0, 0.12);
}
```

### Tailwind Config
```js
// tailwind.config.js theme.extend
{
  colors: {
    'white': '#ffffff',
    'surface-light': '#FDFCF9',
    'surface': '#F5F0EB',
    'text': '#2C2C2C',
    'text-secondary': '#5A5A5A',
    'text-tertiary': '#888888',
    'primary': '#8B6914',
    'primary-light': '#EBE5D9',
    'primary-dark': '#6B5410',
    'secondary': '#7A7A7A',
    'secondary-light': '#EFEFEF',
    'border': '#D4C9BC',
    'border-light': '#E8E3DB',
    'success': '#5A6B52',
    'warning': '#A68B5B',
    'error': '#8B5A52',
    'info': '#6B7A8B',
  },
  borderRadius: {
    'xs': '2px',
    'sm': '2px',
    'default': '3px',
    'md': '4px',
    'lg': '4px',
    'full': '9999px',
  },
  boxShadow: {
    'xs': '0 1px 2px rgba(0, 0, 0, 0.04)',
    'sm': '0 2px 4px rgba(0, 0, 0, 0.06)',
    'md': '0 4px 8px rgba(0, 0, 0, 0.08)',
    'lg': '0 8px 16px rgba(0, 0, 0, 0.1)',
    'xl': '0 12px 24px rgba(0, 0, 0, 0.12)',
  },
  fontFamily: {
    sans: ['Noto Sans', 'system-ui', 'sans-serif'],
  },
}
```

---

## Dark Premium

**Slug:** `dark-premium` | **Category:** Dark & Immersive | **Font:** Inter

### Colors
| Token | Value |
|-------|-------|
| `--color-white` | `#ffffff` |
| `--color-bg-darkest` | `#0a0a0b` |
| `--color-bg-dark` | `#111113` |
| `--color-bg-surface` | `#1a1a1e` |
| `--color-bg-light` | `#232328` |
| `--color-text` | `#f8fafc` |
| `--color-text-secondary` | `rgba(255, 255, 255, 0.7)` |
| `--color-text-tertiary` | `rgba(255, 255, 255, 0.4)` |
| `--color-primary` | `#8b5cf6` |
| `--color-primary-glow` | `0 0 20px rgba(139, 92, 246, 0.3)` |
| `--color-secondary` | `#06b6d4` |
| `--color-accent` | `#d946ef` |
| `--color-border` | `1px solid rgba(255, 255, 255, 0.08)` |
| `--color-border-light` | `1px solid rgba(255, 255, 255, 0.06)` |
| `--color-success` | `#10b981` |
| `--color-warning` | `#f59e0b` |
| `--color-error` | `#ef4444` |
| `--color-info` | `#3b82f6` |

### Typography
| Token | Value |
|-------|-------|
| `--font-family` | `'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif` |
| `--transition` | `all 150ms ease-in-out` |

### Border Radius
| Token | Value |
|-------|-------|
| `--radius-xs` | `2px` |
| `--radius-sm` | `4px` |
| `--radius-default` | `8px` |
| `--radius-md` | `8px` |
| `--radius-lg` | `12px` |
| `--radius-full` | `9999px` |

### Shadows
| Token | Value |
|-------|-------|
| `--shadow-xs` | `0 1px 3px rgba(0, 0, 0, 0.3)` |
| `--shadow-sm` | `0 4px 6px rgba(0, 0, 0, 0.3)` |
| `--shadow-md` | `0 10px 15px rgba(0, 0, 0, 0.4)` |
| `--shadow-lg` | `0 20px 25px rgba(0, 0, 0, 0.5), 0 0 16px rgba(139, 92, 246, 0.15)` |
| `--shadow-xl` | `0 40px 60px rgba(0, 0, 0, 0.6), 0 0 24px rgba(139, 92, 246, 0.2)` |

### CSS Variables (copy-paste ready)
```css
:root {
  --color-white: #ffffff;
  --color-bg-darkest: #0a0a0b;
  --color-bg-dark: #111113;
  --color-bg-surface: #1a1a1e;
  --color-bg-light: #232328;
  --color-text: #f8fafc;
  --color-text-secondary: rgba(255, 255, 255, 0.7);
  --color-text-tertiary: rgba(255, 255, 255, 0.4);
  --color-primary: #8b5cf6;
  --color-primary-glow: 0 0 20px rgba(139, 92, 246, 0.3);
  --color-secondary: #06b6d4;
  --color-accent: #d946ef;
  --color-border: 1px solid rgba(255, 255, 255, 0.08);
  --color-border-light: 1px solid rgba(255, 255, 255, 0.06);
  --color-success: #10b981;
  --color-warning: #f59e0b;
  --color-error: #ef4444;
  --color-info: #3b82f6;
  --transition: all 150ms ease-in-out;
  --font: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
  --radius-xs: 2px;
  --radius-sm: 4px;
  --radius-default: 8px;
  --radius-md: 8px;
  --radius-lg: 12px;
  --radius-full: 9999px;
  --shadow-xs: 0 1px 3px rgba(0, 0, 0, 0.3);
  --shadow-sm: 0 4px 6px rgba(0, 0, 0, 0.3);
  --shadow-md: 0 10px 15px rgba(0, 0, 0, 0.4);
  --shadow-lg: 0 20px 25px rgba(0, 0, 0, 0.5), 0 0 16px rgba(139, 92, 246, 0.15);
  --shadow-xl: 0 40px 60px rgba(0, 0, 0, 0.6), 0 0 24px rgba(139, 92, 246, 0.2);
}
```

### Tailwind Config
```js
// tailwind.config.js theme.extend
{
  colors: {
    'white': '#ffffff',
    'bg-darkest': '#0a0a0b',
    'bg-dark': '#111113',
    'bg-surface': '#1a1a1e',
    'bg-light': '#232328',
    'text': '#f8fafc',
    'text-secondary': 'rgba(255, 255, 255, 0.7)',
    'text-tertiary': 'rgba(255, 255, 255, 0.4)',
    'primary': '#8b5cf6',
    'primary-glow': '0 0 20px rgba(139, 92, 246, 0.3)',
    'secondary': '#06b6d4',
    'accent': '#d946ef',
    'border': '1px solid rgba(255, 255, 255, 0.08)',
    'border-light': '1px solid rgba(255, 255, 255, 0.06)',
    'success': '#10b981',
    'warning': '#f59e0b',
    'error': '#ef4444',
    'info': '#3b82f6',
  },
  borderRadius: {
    'xs': '2px',
    'sm': '4px',
    'default': '8px',
    'md': '8px',
    'lg': '12px',
    'full': '9999px',
  },
  boxShadow: {
    'xs': '0 1px 3px rgba(0, 0, 0, 0.3)',
    'sm': '0 4px 6px rgba(0, 0, 0, 0.3)',
    'md': '0 10px 15px rgba(0, 0, 0, 0.4)',
    'lg': '0 20px 25px rgba(0, 0, 0, 0.5), 0 0 16px rgba(139, 92, 246, 0.15)',
    'xl': '0 40px 60px rgba(0, 0, 0, 0.6), 0 0 24px rgba(139, 92, 246, 0.2)',
  },
  fontFamily: {
    sans: ['Inter', 'system-ui', 'sans-serif'],
  },
}
```

---

## Candy Pop

**Slug:** `candy-pop` | **Category:** Dark & Immersive | **Font:** Quicksand

### Colors
| Token | Value |
|-------|-------|
| `--color-white` | `#ffffff` |
| `--color-surface-light` | `#fff0f5` |
| `--color-surface` | `#fff5f9` |
| `--color-text` | `#2d1b69` |
| `--color-text-secondary` | `#6b5b8d` |
| `--color-text-tertiary` | `#9b8fb5` |
| `--color-primary` | `#ff69b4` |
| `--color-primary-light` | `#ffe0ec` |
| `--color-primary-dark` | `#ff1493` |
| `--color-secondary` | `#9b59b6` |
| `--color-secondary-light` | `#f3e5f5` |
| `--color-border` | `#ffd6e8` |
| `--color-border-light` | `#fff0f5` |
| `--color-success` | `#7ed321` |
| `--color-warning` | `#ffa500` |
| `--color-error` | `#ff6b6b` |
| `--color-info` | `#00ced1` |
| `--color-accent` | `#00ced1` |
| `--color-gold` | `#ffd700` |
| `--color-coral` | `#ff6b6b` |

### Typography
| Token | Value |
|-------|-------|
| `--font-family` | `'Quicksand', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif` |
| `--transition` | `all 300ms cubic-bezier(0.34, 1.56, 0.64, 1)` |

### Border Radius
| Token | Value |
|-------|-------|
| `--radius-full` | `9999px` |
| `--radius-lg` | `20px` |
| `--radius-default` | `16px` |

### Shadows
| Token | Value |
|-------|-------|

### CSS Variables (copy-paste ready)
```css
:root {
  --color-white: #ffffff;
  --color-surface-light: #fff0f5;
  --color-surface: #fff5f9;
  --color-text: #2d1b69;
  --color-text-secondary: #6b5b8d;
  --color-text-tertiary: #9b8fb5;
  --color-primary: #ff69b4;
  --color-primary-light: #ffe0ec;
  --color-primary-dark: #ff1493;
  --color-secondary: #9b59b6;
  --color-secondary-light: #f3e5f5;
  --color-border: #ffd6e8;
  --color-border-light: #fff0f5;
  --color-success: #7ed321;
  --color-warning: #ffa500;
  --color-error: #ff6b6b;
  --color-info: #00ced1;
  --color-accent: #00ced1;
  --color-gold: #ffd700;
  --color-coral: #ff6b6b;
  --transition: all 300ms cubic-bezier(0.34, 1.56, 0.64, 1);
  --font: 'Quicksand', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
  --radius-full: 9999px;
  --radius-lg: 20px;
  --radius-default: 16px;
}
```

### Tailwind Config
```js
// tailwind.config.js theme.extend
{
  colors: {
    'white': '#ffffff',
    'surface-light': '#fff0f5',
    'surface': '#fff5f9',
    'text': '#2d1b69',
    'text-secondary': '#6b5b8d',
    'text-tertiary': '#9b8fb5',
    'primary': '#ff69b4',
    'primary-light': '#ffe0ec',
    'primary-dark': '#ff1493',
    'secondary': '#9b59b6',
    'secondary-light': '#f3e5f5',
    'border': '#ffd6e8',
    'border-light': '#fff0f5',
    'success': '#7ed321',
    'warning': '#ffa500',
    'error': '#ff6b6b',
    'info': '#00ced1',
    'accent': '#00ced1',
    'gold': '#ffd700',
    'coral': '#ff6b6b',
  },
  borderRadius: {
    'full': '9999px',
    'lg': '20px',
    'default': '16px',
  },
  boxShadow: {
  },
  fontFamily: {
    sans: ['Quicksand', 'system-ui', 'sans-serif'],
  },
}
```

---

## Anime Gacha

**Slug:** `anime-gacha` | **Category:** Dark & Immersive | **Font:** Nunito

### Colors
| Token | Value |
|-------|-------|
| `--color-white` | `#ffffff` |
| `--color-surface-light` | `#1A1A3E` |
| `--color-surface` | `#0F0F2E` |
| `--color-text` | `#FFFFFF` |
| `--color-text-secondary` | `#B0B8D4` |
| `--color-text-tertiary` | `#7A8AB0` |
| `--color-primary` | `#4A5FE0` |
| `--color-primary-light` | `rgba(74, 95, 224, 0.15)` |
| `--color-primary-dark` | `#2E3BA8` |
| `--color-secondary` | `#C98FFF` |
| `--color-secondary-light` | `rgba(201, 143, 255, 0.15)` |
| `--color-border` | `rgba(74, 95, 224, 0.3)` |
| `--color-border-light` | `rgba(74, 95, 224, 0.2)` |
| `--color-success` | `#4FD991` |
| `--color-warning` | `#FFB84D` |
| `--color-error` | `#FF6B6B` |
| `--color-info` | `#5FC3FF` |
| `--color-gold` | `#FFD700` |

### Typography
| Token | Value |
|-------|-------|
| `--font-family` | `'Nunito', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif` |
| `--transition` | `all 250ms cubic-bezier(0.34, 1.56, 0.64, 1)` |

### Border Radius
| Token | Value |
|-------|-------|
| `--radius-xs` | `6px` |
| `--radius-sm` | `8px` |
| `--radius-default` | `12px` |
| `--radius-md` | `14px` |
| `--radius-lg` | `16px` |
| `--radius-full` | `9999px` |

### Shadows
| Token | Value |
|-------|-------|
| `--shadow-xs` | `0 0 12px rgba(74, 95, 224, 0.2)` |
| `--shadow-sm` | `0 0 20px rgba(74, 95, 224, 0.3)` |
| `--shadow-md` | `0 0 32px rgba(74, 95, 224, 0.4)` |
| `--shadow-lg` | `0 0 48px rgba(74, 95, 224, 0.5)` |
| `--shadow-xl` | `0 0 64px rgba(74, 95, 224, 0.6)` |

### CSS Variables (copy-paste ready)
```css
:root {
  --color-white: #ffffff;
  --color-surface-light: #1A1A3E;
  --color-surface: #0F0F2E;
  --color-text: #FFFFFF;
  --color-text-secondary: #B0B8D4;
  --color-text-tertiary: #7A8AB0;
  --color-primary: #4A5FE0;
  --color-primary-light: rgba(74, 95, 224, 0.15);
  --color-primary-dark: #2E3BA8;
  --color-secondary: #C98FFF;
  --color-secondary-light: rgba(201, 143, 255, 0.15);
  --color-border: rgba(74, 95, 224, 0.3);
  --color-border-light: rgba(74, 95, 224, 0.2);
  --color-success: #4FD991;
  --color-warning: #FFB84D;
  --color-error: #FF6B6B;
  --color-info: #5FC3FF;
  --color-gold: #FFD700;
  --transition: all 250ms cubic-bezier(0.34, 1.56, 0.64, 1);
  --font: 'Nunito', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
  --radius-xs: 6px;
  --radius-sm: 8px;
  --radius-default: 12px;
  --radius-md: 14px;
  --radius-lg: 16px;
  --radius-full: 9999px;
  --shadow-xs: 0 0 12px rgba(74, 95, 224, 0.2);
  --shadow-sm: 0 0 20px rgba(74, 95, 224, 0.3);
  --shadow-md: 0 0 32px rgba(74, 95, 224, 0.4);
  --shadow-lg: 0 0 48px rgba(74, 95, 224, 0.5);
  --shadow-xl: 0 0 64px rgba(74, 95, 224, 0.6);
}
```

### Tailwind Config
```js
// tailwind.config.js theme.extend
{
  colors: {
    'white': '#ffffff',
    'surface-light': '#1A1A3E',
    'surface': '#0F0F2E',
    'text': '#FFFFFF',
    'text-secondary': '#B0B8D4',
    'text-tertiary': '#7A8AB0',
    'primary': '#4A5FE0',
    'primary-light': 'rgba(74, 95, 224, 0.15)',
    'primary-dark': '#2E3BA8',
    'secondary': '#C98FFF',
    'secondary-light': 'rgba(201, 143, 255, 0.15)',
    'border': 'rgba(74, 95, 224, 0.3)',
    'border-light': 'rgba(74, 95, 224, 0.2)',
    'success': '#4FD991',
    'warning': '#FFB84D',
    'error': '#FF6B6B',
    'info': '#5FC3FF',
    'gold': '#FFD700',
  },
  borderRadius: {
    'xs': '6px',
    'sm': '8px',
    'default': '12px',
    'md': '14px',
    'lg': '16px',
    'full': '9999px',
  },
  boxShadow: {
    'xs': '0 0 12px rgba(74, 95, 224, 0.2)',
    'sm': '0 0 20px rgba(74, 95, 224, 0.3)',
    'md': '0 0 32px rgba(74, 95, 224, 0.4)',
    'lg': '0 0 48px rgba(74, 95, 224, 0.5)',
    'xl': '0 0 64px rgba(74, 95, 224, 0.6)',
  },
  fontFamily: {
    sans: ['Nunito', 'system-ui', 'sans-serif'],
  },
}
```

---

## Grunge Underground

**Slug:** `grunge-underground` | **Category:** Dark & Immersive | **Font:** Roboto Mono

### Colors
| Token | Value |
|-------|-------|
| `--color-white` | `#ffffff` |
| `--color-surface-light` | `#F9F6F1` |
| `--color-surface` | `#F2E8D5` |
| `--color-text` | `#1A1A1A` |
| `--color-text-secondary` | `#4A4A4A` |
| `--color-text-tertiary` | `#7A7A7A` |
| `--color-primary` | `#C62828` |
| `--color-primary-light` | `#F5DDD8` |
| `--color-primary-dark` | `#8B1A1A` |
| `--color-secondary` | `#4A4A4A` |
| `--color-secondary-light` | `#E5E5E5` |
| `--color-border` | `#333333` |
| `--color-border-light` | `#D4D4D4` |
| `--color-success` | `#3D5A2C` |
| `--color-warning` | `#B8860B` |
| `--color-error` | `#C62828` |
| `--color-info` | `#2C5282` |

### Typography
| Token | Value |
|-------|-------|
| `--font-family` | `'Roboto Mono', monospace` |
| `--transition` | `all 180ms cubic-bezier(0.4, 0, 0.2, 1)` |

### Border Radius
| Token | Value |
|-------|-------|
| `--radius-xs` | `0px` |
| `--radius-sm` | `0px` |
| `--radius-default` | `0px` |
| `--radius-md` | `0px` |
| `--radius-lg` | `0px` |
| `--radius-full` | `9999px` |

### Shadows
| Token | Value |
|-------|-------|
| `--shadow-xs` | `0 2px 4px rgba(0, 0, 0, 0.15)` |
| `--shadow-sm` | `0 4px 8px rgba(0, 0, 0, 0.2)` |
| `--shadow-md` | `0 8px 16px rgba(0, 0, 0, 0.25)` |
| `--shadow-lg` | `0 12px 24px rgba(0, 0, 0, 0.3)` |
| `--shadow-xl` | `0 16px 32px rgba(0, 0, 0, 0.4)` |

### CSS Variables (copy-paste ready)
```css
:root {
  --color-white: #ffffff;
  --color-surface-light: #F9F6F1;
  --color-surface: #F2E8D5;
  --color-text: #1A1A1A;
  --color-text-secondary: #4A4A4A;
  --color-text-tertiary: #7A7A7A;
  --color-primary: #C62828;
  --color-primary-light: #F5DDD8;
  --color-primary-dark: #8B1A1A;
  --color-secondary: #4A4A4A;
  --color-secondary-light: #E5E5E5;
  --color-border: #333333;
  --color-border-light: #D4D4D4;
  --color-success: #3D5A2C;
  --color-warning: #B8860B;
  --color-error: #C62828;
  --color-info: #2C5282;
  --transition: all 180ms cubic-bezier(0.4, 0, 0.2, 1);
  --font: 'Roboto Mono', monospace;
  --radius-xs: 0px;
  --radius-sm: 0px;
  --radius-default: 0px;
  --radius-md: 0px;
  --radius-lg: 0px;
  --radius-full: 9999px;
  --shadow-xs: 0 2px 4px rgba(0, 0, 0, 0.15);
  --shadow-sm: 0 4px 8px rgba(0, 0, 0, 0.2);
  --shadow-md: 0 8px 16px rgba(0, 0, 0, 0.25);
  --shadow-lg: 0 12px 24px rgba(0, 0, 0, 0.3);
  --shadow-xl: 0 16px 32px rgba(0, 0, 0, 0.4);
}
```

### Tailwind Config
```js
// tailwind.config.js theme.extend
{
  colors: {
    'white': '#ffffff',
    'surface-light': '#F9F6F1',
    'surface': '#F2E8D5',
    'text': '#1A1A1A',
    'text-secondary': '#4A4A4A',
    'text-tertiary': '#7A7A7A',
    'primary': '#C62828',
    'primary-light': '#F5DDD8',
    'primary-dark': '#8B1A1A',
    'secondary': '#4A4A4A',
    'secondary-light': '#E5E5E5',
    'border': '#333333',
    'border-light': '#D4D4D4',
    'success': '#3D5A2C',
    'warning': '#B8860B',
    'error': '#C62828',
    'info': '#2C5282',
  },
  borderRadius: {
    'xs': '0px',
    'sm': '0px',
    'default': '0px',
    'md': '0px',
    'lg': '0px',
    'full': '9999px',
  },
  boxShadow: {
    'xs': '0 2px 4px rgba(0, 0, 0, 0.15)',
    'sm': '0 4px 8px rgba(0, 0, 0, 0.2)',
    'md': '0 8px 16px rgba(0, 0, 0, 0.25)',
    'lg': '0 12px 24px rgba(0, 0, 0, 0.3)',
    'xl': '0 16px 32px rgba(0, 0, 0, 0.4)',
  },
  fontFamily: {
    sans: ['Roboto Mono', 'system-ui', 'sans-serif'],
  },
}
```

---

## Holographic Futurism

**Slug:** `holographic-futurism` | **Category:** Dark & Immersive | **Font:** Inter

### Colors
| Token | Value |
|-------|-------|
| `--color-white` | `#ffffff` |
| `--color-surface-light` | `rgba(255, 255, 255, 0.05)` |
| `--color-surface` | `rgba(255, 255, 255, 0.03)` |
| `--color-text` | `#FFFFFF` |
| `--color-text-secondary` | `rgba(255, 255, 255, 0.7)` |
| `--color-text-tertiary` | `rgba(255, 255, 255, 0.4)` |
| `--color-primary` | `#00F5FF` |
| `--color-primary-light` | `rgba(0, 245, 255, 0.15)` |
| `--color-primary-dark` | `#00B8CC` |
| `--color-secondary` | `#FF00FF` |
| `--color-secondary-light` | `rgba(255, 0, 255, 0.15)` |
| `--color-border` | `rgba(255, 255, 255, 0.08)` |
| `--color-border-light` | `rgba(255, 255, 255, 0.12)` |
| `--color-success` | `#00FF88` |
| `--color-warning` | `#FFAA00` |
| `--color-error` | `#FF0055` |
| `--color-info` | `#00FFFF` |

### Typography
| Token | Value |
|-------|-------|
| `--font-family` | `'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif` |
| `--transition` | `all 300ms cubic-bezier(0.34, 1.56, 0.64, 1)` |

### Border Radius
| Token | Value |
|-------|-------|
| `--radius-xs` | `12px` |
| `--radius-sm` | `14px` |
| `--radius-default` | `16px` |
| `--radius-md` | `18px` |
| `--radius-lg` | `20px` |
| `--radius-full` | `9999px` |

### Shadows
| Token | Value |
|-------|-------|
| `--shadow-xs` | `0 0 20px rgba(0, 245, 255, 0.2)` |
| `--shadow-sm` | `0 0 40px rgba(0, 245, 255, 0.3)` |
| `--shadow-md` | `0 0 60px rgba(0, 245, 255, 0.4)` |
| `--shadow-lg` | `0 0 80px rgba(0, 245, 255, 0.5)` |
| `--shadow-xl` | `0 0 120px rgba(0, 245, 255, 0.6)` |

### CSS Variables (copy-paste ready)
```css
:root {
  --color-white: #ffffff;
  --color-surface-light: rgba(255, 255, 255, 0.05);
  --color-surface: rgba(255, 255, 255, 0.03);
  --color-text: #FFFFFF;
  --color-text-secondary: rgba(255, 255, 255, 0.7);
  --color-text-tertiary: rgba(255, 255, 255, 0.4);
  --color-primary: #00F5FF;
  --color-primary-light: rgba(0, 245, 255, 0.15);
  --color-primary-dark: #00B8CC;
  --color-secondary: #FF00FF;
  --color-secondary-light: rgba(255, 0, 255, 0.15);
  --color-border: rgba(255, 255, 255, 0.08);
  --color-border-light: rgba(255, 255, 255, 0.12);
  --color-success: #00FF88;
  --color-warning: #FFAA00;
  --color-error: #FF0055;
  --color-info: #00FFFF;
  --transition: all 300ms cubic-bezier(0.34, 1.56, 0.64, 1);
  --font: 'Inter', -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
  --radius-xs: 12px;
  --radius-sm: 14px;
  --radius-default: 16px;
  --radius-md: 18px;
  --radius-lg: 20px;
  --radius-full: 9999px;
  --shadow-xs: 0 0 20px rgba(0, 245, 255, 0.2);
  --shadow-sm: 0 0 40px rgba(0, 245, 255, 0.3);
  --shadow-md: 0 0 60px rgba(0, 245, 255, 0.4);
  --shadow-lg: 0 0 80px rgba(0, 245, 255, 0.5);
  --shadow-xl: 0 0 120px rgba(0, 245, 255, 0.6);
}
```

### Tailwind Config
```js
// tailwind.config.js theme.extend
{
  colors: {
    'white': '#ffffff',
    'surface-light': 'rgba(255, 255, 255, 0.05)',
    'surface': 'rgba(255, 255, 255, 0.03)',
    'text': '#FFFFFF',
    'text-secondary': 'rgba(255, 255, 255, 0.7)',
    'text-tertiary': 'rgba(255, 255, 255, 0.4)',
    'primary': '#00F5FF',
    'primary-light': 'rgba(0, 245, 255, 0.15)',
    'primary-dark': '#00B8CC',
    'secondary': '#FF00FF',
    'secondary-light': 'rgba(255, 0, 255, 0.15)',
    'border': 'rgba(255, 255, 255, 0.08)',
    'border-light': 'rgba(255, 255, 255, 0.12)',
    'success': '#00FF88',
    'warning': '#FFAA00',
    'error': '#FF0055',
    'info': '#00FFFF',
  },
  borderRadius: {
    'xs': '12px',
    'sm': '14px',
    'default': '16px',
    'md': '18px',
    'lg': '20px',
    'full': '9999px',
  },
  boxShadow: {
    'xs': '0 0 20px rgba(0, 245, 255, 0.2)',
    'sm': '0 0 40px rgba(0, 245, 255, 0.3)',
    'md': '0 0 60px rgba(0, 245, 255, 0.4)',
    'lg': '0 0 80px rgba(0, 245, 255, 0.5)',
    'xl': '0 0 120px rgba(0, 245, 255, 0.6)',
  },
  fontFamily: {
    sans: ['Inter', 'system-ui', 'sans-serif'],
  },
}
```

---
