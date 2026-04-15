# Dokali UI Kit

A beautiful, very lightweight CSS UI kit with multiple color themes and full RTL support 
by Belaid Dokali - Libya 2026.

## Features

- **7 Color Themes**: Ocean, Forest, Sunset, Berry, Midnight, Rose, Slate
- **Full RTL Support**: Complete right-to-left layout support
- **Modal Transitions Kit**: 12+ smooth modal animations
- **Toast Notifications**: 9 animation types with auto-dismiss
- **No Dependencies**: Pure CSS, no frameworks required
- **Responsive**: Mobile-friendly components
- **Accessible**: WCAG-compliant components

## Quick Start

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <link rel="stylesheet" href="css/dokali-ui-kit.min.css">
</head>
<body data-theme="ocean">
  <!-- Your content here -->
</body>
</html>
```

## File Structure

```
css/
├── dokali-ui-kit.min.css    (38KB) - Core UI Kit
├── dokali-modals.min.css    (17KB) - Modal Transitions
└── dokali-toasts.min.css   (14KB) - Toast Notifications
```

Use the minified versions in production:

```html
<link rel="stylesheet" href="css/dokali-ui-kit.min.css">
<link rel="stylesheet" href="css/dokali-modals.min.css">
<link rel="stylesheet" href="css/dokali-toasts.min.css">
```

## Color Themes

Change theme by adding `data-theme` attribute to body:

```html
<body data-theme="forest">...</body>
```

Available themes: `ocean`, `forest`, `sunset`, `berry`, `midnight`, `rose`, `slate`

## RTL Support

Enable RTL mode by adding `dir="rtl"` to html element:

```html
<html dir="rtl">
```

Or toggle via JavaScript:

```javascript
document.documentElement.setAttribute('dir', 'rtl');
```

### RTL Components Example

```html
<html dir="rtl">
  <nav class="navbar">
    <div class="navbar-actions">
      <button class="btn btn-primary">تسجيل</button>
    </div>
    <ul class="navbar-nav">
      <li><a class="navbar-nav-link active">الرئيسية</a></li>
      <li><a class="navbar-nav-link">من نحن</a></li>
    </ul>
    <a class="navbar-brand">المتجر</a>
  </nav>

  <div class="breadcrumb">
    <li class="breadcrumb-item"><a href="#">الرئيسية</a></li>
    <li class="breadcrumb-item"><a href="#">المنتجات</a></li>
    <li class="breadcrumb-item active">التفاصيل</li>
  </div>

  <div class="sidebar">
    <a class="sidebar-link active">لوحة التحكم</a>
    <a class="sidebar-link">الملف الشخصي</a>
    <a class="sidebar-link">الإعدادات</a>
  </div>

  <div class="pagination">
    <li class="pagination-item"><a class="pagination-link">›</a></li>
    <li class="pagination-item"><a class="pagination-link active">1</a></li>
    <li class="pagination-item"><a class="pagination-link">‹</a></li>
  </div>
</html>
```

All components automatically adjust for RTL:
- Navbar: logo moves to right, actions move to left
- Sidebar: content aligns to right
- Breadcrumb: separator direction reverses
- Pagination: arrows reverse direction
- Form inputs: text alignment adjusts

## Components

### Buttons

```html
<button class="btn btn-primary">Primary</button>
<button class="btn btn-secondary">Secondary</button>
<button class="btn btn-ghost">Ghost</button>
<button class="btn btn-danger">Danger</button>
<button class="btn btn-success">Success</button>

<!-- Sizes -->
<button class="btn btn-primary btn-sm">Small</button>
<button class="btn btn-primary btn-lg">Large</button>
```

### Cards

```html
<div class="card">
  <h4 class="card-title">Card Title</h4>
  <p class="card-body">Card content here</p>
</div>

<!-- Elevated -->
<div class="card card-elevated">...</div>

<!-- With Header/Footer -->
<div class="card">
  <div class="card-header">
    <h4 class="card-title">Title</h4>
    <p class="card-subtitle">Subtitle</p>
  </div>
  <p class="card-body">Content</p>
  <div class="card-footer">Action</div>
</div>
```

### Form Elements

```html
<!-- Input -->
<div class="form-group">
  <label class="form-label">Email</label>
  <input type="email" class="form-input" placeholder="Enter email">
</div>

<!-- Textarea -->
<textarea class="form-input form-textarea"></textarea>

<!-- Select -->
<select class="form-input form-select">
  <option>Choose...</option>
</select>

<!-- Checkbox -->
<label>
  <input type="checkbox" class="form-checkbox">
  <span>Remember me</span>
</label>

<!-- Switch -->
<label>
  <input type="checkbox" class="form-switch">
  <span>Dark Mode</span>
</label>
```

### Badges

```html
<span class="badge badge-primary">Primary</span>
<span class="badge badge-success">Success</span>
<span class="badge badge-warning">Warning</span>
<span class="badge badge-error">Error</span>
<span class="badge badge-info">Info</span>
```

### Alerts

```html
<div class="alert alert-success">Success message!</div>
<div class="alert alert-warning">Warning message!</div>
<div class="alert alert-error">Error message!</div>
<div class="alert alert-info">Info message!</div>
```

### Tables

```html
<div class="table-container">
  <table class="table">
    <thead>
      <tr><th>Name</th><th>Email</th></tr>
    </thead>
    <tbody>
      <tr><td>John</td><td>john@example.com</td></tr>
    </tbody>
  </table>
</div>

<!-- Variants -->
<table class="table table-striped">...</table>
<table class="table table-bordered">...</table>
<table class="table table-sm">...</table>
<table class="table table-lg">...</table>
```

### Lists

```html
<ul class="list">
  <li class="list-item">
    <span class="list-item-content">
      <div class="list-item-title">Title</div>
      <div class="list-item-description">Description</div>
    </span>
  </li>
</ul>

<!-- Variants -->
<ul class="list list-bordered">...</ul>
<ul class="list list-divided">...</ul>
```

### Navigation - Navbar

```html
<nav class="navbar">
  <a href="#" class="navbar-brand">
    <div class="navbar-logo">K</div>
    <span>Brand</span>
  </a>
  <ul class="navbar-nav">
    <li class="navbar-nav-item">
      <a class="navbar-nav-link active">Home</a>
    </li>
    <li class="navbar-nav-item">
      <a class="navbar-nav-link">About</a>
    </li>
  </ul>
  <div class="navbar-actions">
    <button class="btn btn-primary">Get Started</button>
  </div>
</nav>
```

### Navigation - Sidebar

```html
<aside class="sidebar">
  <div class="sidebar-header">
    <a href="#" class="sidebar-brand">Brand</a>
  </div>
  <nav class="sidebar-nav">
    <div class="sidebar-section">
      <div class="sidebar-section-title">Menu</div>
      <a href="#" class="sidebar-link active">Dashboard</a>
      <a href="#" class="sidebar-link">Profile</a>
    </div>
  </nav>
</aside>
```

### Navigation - Breadcrumb

```html
<ol class="breadcrumb">
  <li class="breadcrumb-item"><a href="#">Home</a></li>
  <li class="breadcrumb-item"><a href="#">Products</a></li>
  <li class="breadcrumb-item active">Current</li>
</ol>
```

### Navigation - Pagination

```html
<ul class="pagination">
  <li class="pagination-item">
    <a class="pagination-link disabled">‹</a>
  </li>
  <li class="pagination-item">
    <a class="pagination-link active">1</a>
  </li>
  <li class="pagination-item">
    <a class="pagination-link">2</a>
  </li>
  <li class="pagination-item">
    <a class="pagination-link">›</a>
  </li>
</ul>
```

### Navigation - Steps

```html
<div class="steps">
  <div class="step completed">
    <div class="step-icon">✓</div>
    <div class="step-label">Step 1</div>
  </div>
  <div class="step active">
    <div class="step-icon">2</div>
    <div class="step-label">Step 2</div>
  </div>
  <div class="step">
    <div class="step-icon">3</div>
    <div class="step-label">Step 3</div>
  </div>
</div>
```

### Navigation - Tabs

```html
<!-- Pill Style -->
<div class="tab-list tab-pills">
  <button class="tab-button active">Tab 1</button>
  <button class="tab-button">Tab 2</button>
</div>

<!-- Underline Style -->
<div class="tabs">
  <button class="tab active">Tab 1</button>
  <button class="tab">Tab 2</button>
</div>
```

### Modals

```html
<div class="modal-overlay active">
  <div class="modal">
    <div class="modal-header">
      <h3 class="modal-title">Modal Title</h3>
      <button class="modal-close">×</button>
    </div>
    <div class="modal-body">
      <p>Modal content</p>
    </div>
    <div class="modal-footer">
      <button class="btn btn-secondary">Cancel</button>
      <button class="btn btn-primary">Confirm</button>
    </div>
  </div>
</div>

<!-- Sizes -->
<div class="modal modal-sm">...</div>
<div class="modal modal-lg">...</div>
<div class="modal modal-xl">...</div>
```

### Modal Transitions

Include dokali-modals.css and use transition classes:

```html
<div class="modal-overlay active">
  <div class="modal modal-slide-in">...</div>
  <div class="modal modal-zoom-in">...</div>
  <div class="modal modal-flip-in">...</div>
  <div class="modal modal-bounce-in">...</div>
  <!-- Many more animations available -->
</div>
```

### Toast Notifications

Include dokali-toasts.css:

```html
<div class="toast-container">
  <div class="toast toast-success">Message</div>
  <div class="toast toast-error">Message</div>
  <div class="toast toast-warning">Message</div>
  <div class="toast toast-info">Message</div>
</div>

<!-- With animations -->
<div class="toast toast-slide">...</div>
<div class="toast toast-fade">...</div>
<div class="toast toast-scale">...</div>
<!-- Many more animations available -->

<!-- Auto-dismiss with progress -->
<div class="toast toast-dismissible">
  <div class="toast-progress" style="animation: toast-progress 5s linear forwards;"></div>
</div>
```

### Progress Bars

```html
<div class="progress">
  <div class="progress-bar" style="width: 65%;"></div>
</div>

<!-- Sizes -->
<div class="progress progress-sm">...</div>
<div class="progress progress-lg">...</div>
```

### Avatars

```html
<div class="avatar avatar-sm">JD</div>
<div class="avatar avatar-md">JD</div>
<div class="avatar avatar-lg">JD</div>
<div class="avatar avatar-xl">JD</div>

<!-- With Image -->
<div class="avatar avatar-md">
  <img src="photo.jpg" alt="User">
</div>

<!-- Group -->
<div class="avatar-group">
  <div class="avatar avatar-md">A</div>
  <div class="avatar avatar-md">B</div>
  <div class="avatar avatar-md">+3</div>
</div>
```

## Utility Classes

### Flexbox

```html
<div class="flex">...</div>
<div class="flex flex-col">...</div>
<div class="flex items-center">...</div>
<div class="flex justify-center">...</div>
<div class="flex justify-between">...</div>
<div class="flex gap-2">...</div>
```

### Spacing

```html
<div class="mt-1">margin-top: 0.25rem</div>
<div class="mt-2">margin-top: 0.5rem</div>
<div class="mt-3">margin-top: 0.75rem</div>
<div class="mt-4">margin-top: 1rem</div>
<div class="mb-1">margin-bottom: 0.25rem</div>
<div class="mb-2">margin-bottom: 0.5rem</div>
<div class="mb-3">margin-bottom: 0.75rem</div>
<div class="mb-4">margin-bottom: 1rem</div>
```

### Text

```html
<p class="text-primary">Primary text</p>
<p class="text-secondary">Secondary text</p>
<p class="text-muted">Muted text</p>
<p class="text-success">Success text</p>
<p class="text-warning">Warning text</p>
<p class="text-error">Error text</p>
```

### Display

```html
<div class="block">...</div>
<div class="inline">...</div>
<div class="inline-block">...</div>
<div class="hidden">...</div>
```

### Border Radius

```html
<div class="rounded">...</div>
<div class="rounded-lg">...</div>
<div class="rounded-full">...</div>
```

### Shadows

```html
<div class="shadow">...</div>
<div class="shadow-lg">...</div>
```

## CSS Variables

```css
:root {
  --primary: #0ea5e9;
  --primary-hover: #0284c7;
  --primary-light: #e0f2fe;
  --secondary: #64748b;
  --background: #f8fafc;
  --surface: #ffffff;
  --text-primary: #0f172a;
  --text-secondary: #64748b;
  --text-muted: #94a3b8;
  --border: #e2e8f0;
  --success: #22c55e;
  --warning: #f59e0b;
  --error: #ef4444;
  --info: #3b82f6;
  --radius-sm: 6px;
  --radius-md: 10px;
  --radius-lg: 16px;
  --radius-xl: 24px;
  --radius-full: 9999px;
}
```

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## License

MIT License
