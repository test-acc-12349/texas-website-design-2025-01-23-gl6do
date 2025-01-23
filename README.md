# Landing Page Maintenance Guide

This guide will help you maintain and customize your Texas Website Design landing page. Follow these instructions carefully to make updates while preserving the design and functionality.

## 1. Updating Text and Tailwind CSS Classes

### Header Section
```html
<header class="fixed w-full bg-white/90 backdrop-blur-md z-50 border-b border-gray-100">
```
- To change the company name "TWD", locate:
```html
<div class="text-2xl font-bold bg-gradient-to-r from-purple-600 to-blue-500 bg-clip-text text-transparent">
    TWD
</div>
```
- The gradient colors can be modified by changing `from-purple-600` and `to-blue-500`

### Hero Section
```html
<section class="pt-32 pb-24 bg-gradient-to-br from-purple-50 to-blue-50">
```
To update the main headline and subheading:
1. Find the `<h1>` tag for the main title
2. Find the `<p>` tag below it for the subtitle
3. Simply replace the text while keeping the classes intact

### Tailwind CSS Tips
- Font sizes use this pattern: `text-[size]`
  - Example: `text-4xl` (larger) vs `text-base` (normal)
- Colors use this pattern: `[type]-[color]-[shade]`
  - Example: `bg-purple-600`, `text-gray-900`
- Spacing uses this pattern: `[property]-[size]`
  - Example: `px-6` (padding left/right), `my-4` (margin top/bottom)

## 2. Fixing Broken Links

### Navigation Menu Links
Current navigation structure:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To update links:
1. Locate the `href` attribute in each `<a>` tag
2. For internal section links, keep the `#` prefix
3. For external links, use the full URL
   - Example: `href="https://yourwebsite.com/page"`

### Call-to-Action Buttons
Current placeholder:
```html
<a href="https://twd.com" class="inline-block px-8 py-4...">
```
Replace `https://twd.com` with your actual website URL

### Social Media Links
Located in the footer:
```html
<div class="flex space-x-4">
    <a href="#" class="hover:text-white transition-colors duration-300">
        <i class="fab fa-twitter"></i>
    </a>
    <!-- Similar for Facebook and Instagram -->
</div>
```
Replace `#` with your social media profile URLs

## 3. Adding Privacy and Terms Pages

### Footer Modification
Add privacy and terms links in the Quick Links section:
```html
<ul class="space-y-2">
    <li><a href="#features">Features</a></li>
    <!-- Add these new lines -->
    <li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
</ul>
```

### Creating New Pages
1. Create `privacy.html` and `terms.html` in your root directory
2. Use the same header and footer as `index.html`
3. Maintain consistent styling by copying these classes:
   ```html
   class="hover:text-white transition-colors duration-300"
   ```

## Troubleshooting Tips

1. If the navigation menu disappears on mobile:
   - Check that the `hidden md:flex` classes are present
   - These control mobile responsiveness

2. If gradients aren't showing:
   - Verify Tailwind CSS is properly loaded in the head section
   - Check for typos in gradient class names

3. If spacing looks incorrect:
   - Ensure container classes are present: `container mx-auto px-6`
   - Check for missing padding/margin classes

## Important Notes

- Always backup your code before making changes
- Test all links after updating
- View changes on multiple devices to ensure responsiveness
- Keep the gradient theme consistent throughout the page
- Maintain the existing responsive design classes
- Test the page in multiple browsers

For additional help or questions, contact your web developer or refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs).