# Personal Details Page

A responsive medical records interface with collapsible left navigation using token CSS design system with consistent spacing patterns.

## 🎯 Features

- **Collapsible Left Sidebar**: Toggle between expanded (280px) and collapsed (80px) states
- **Consistent Spacing**: Matches LeftNav component spacing patterns
- **Easy Logo Replacement**: Multiple logo options with clear documentation
- **Fully Responsive**: Works seamlessly from desktop to mobile
- **Dark Mode Support**: Automatic theme switching through token CSS

## 📐 Left Sidebar Navigation

### Expanded State (280px)
**Container Structure:**
- **Container padding**: `var(--spacing-300)` (24px) - all sides
- **Logo section**: Positioned at top
- **Below logo**: `var(--spacing-100)` (8px)
- **Collapse toggle**: Full width button
- **Below toggle**: `var(--spacing-100)` (8px)
- **Search section**: Input with icon
- **Below search**: `var(--spacing-100)` (8px)
- **Navigation items gap**: `var(--spacing-100)` (8px) between each
- **Item padding**: `var(--spacing-150) var(--spacing-200)` (12px 16px)
- **Submenu items gap**: `var(--spacing-100)` (8px)

### Collapsed State (80px)
- **Container padding**: `var(--spacing-300)` (24px)
- **All gaps**: `var(--spacing-100)` (8px) maintained
- **Item padding**: `var(--spacing-150)` (12px) - centered
- **Icons centered, labels hidden**
- **Tooltips on hover**
- **Smooth 0.3s transition**

### Collapse Toggle
- Located below logo
- Full width button
- Chevron icon rotates (left ← → right)
- Click to toggle between states
- Keyboard accessible (aria-expanded)

## 🎨 Spacing Patterns (Matching LeftNav)

This page follows the same spacing patterns as the LeftNav component for consistency:

### Container Spacing
- **Main padding**: `var(--spacing-300)` (24px)
- **Gap between sections**: `var(--spacing-300)` (24px)
- **Consistent vertical rhythm**: All major sections use spacing-300

### Component Spacing
- **Navigation items**: `padding: var(--spacing-150) var(--spacing-200)` (12px 16px)
- **Tab links**: `padding: var(--spacing-200) var(--spacing-300)` (16px 24px)
- **Tab gaps**: `var(--spacing-150)` (12px) between individual tabs
- **Section gaps**: `var(--spacing-300)` (24px) for major sections

### Entry Content Spacing
- **Between sections**: `var(--spacing-300)` (24px)
- **Within sections**: `var(--spacing-150)` (12px)
- **Two-column layout**: `var(--spacing-400)` (32px) horizontal gap

## 🔄 Logo Component - Easy Replacement

The logo component is designed to be easily replaceable. See [logo-component.html](logo-component.html) for all options.

### Current Logo (Default)
```html
<div class="nav-brand">
    <div class="logo-container">
        <div class="logo-square logo-square-top"></div>
        <div class="logo-square logo-square-bottom"></div>
    </div>
    <span class="brand-name">EG Infodoc</span>
</div>
```

### Replace with Image Logo
```html
<div class="nav-brand">
    <img src="path/to/logo.svg" alt="Company Logo" class="logo-image">
    <span class="brand-name">Company Name</span>
</div>
```

### Replace with Icon Logo
```html
<div class="nav-brand">
    <div class="logo-icon-container">
        <i data-lucide="heart-pulse"></i>
    </div>
    <span class="brand-name">MedTech</span>
</div>
```

### Text-Only Logo
```html
<div class="nav-brand">
    <span class="brand-name">Your Brand Name</span>
</div>
```

## 📱 Responsive Breakpoints

- **Desktop**: Full layout with all features
- **1024px**: Reduced padding, 2-column patient details
- **768px**: Stack patient card, hide nav links, single column entries
- **480px**: Compact spacing, icon-only buttons, mobile-optimized
- **360px**: Ultra-compact for small devices

## 🎯 Design System

All spacing, colors, typography, and interactions use token CSS:
- Colors: `var(--color-primary-default)`, `var(--text-default)`, etc.
- Spacing: `var(--spacing-100)` through `var(--spacing-600)`
- Typography: `var(--font-size-small)`, `var(--font-weight-semibold)`, etc.
- Borders: `var(--border-radius-100)`, `var(--border-width-thin)`, etc.

## 🌗 Dark Mode

Dark mode is automatically supported through the token CSS system. The page adapts to `[data-theme="dark"]` attribute on the HTML element.

## 📁 Files

- `personal-details.html` - Main page structure
- `personal-details.css` - Styles with token CSS
- `logo-component.html` - Reusable logo options
- `README.md` - This documentation

## 🚀 Usage

1. Include the tokens CSS file: `../_tokens.css`
2. Include the personal details CSS: `personal-details.css`
3. Include Lucide icons: `https://unpkg.com/lucide@latest`
4. Replace the logo component as needed
5. Customize content while maintaining spacing patterns
