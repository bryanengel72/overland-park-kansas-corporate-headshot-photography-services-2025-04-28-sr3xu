# 101Headshots Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the 101Headshots landing page. Whether you're new to web development or need a quick reference, follow these steps to make common updates safely and effectively.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the company logo and navigation menu. To update:

1. **Company Logo Text:**
```html
<!-- Find this line in the header section -->
<a href="/" class="text-2xl font-bold text-gray-800">101Headshots</a>
```
Simply replace "101Headshots" with your desired text.

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#services" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Services</a>
    <!-- Additional menu items -->
</div>
```
- Change text between `>` and `</a>` tags
- Keep the `class` attributes unchanged to maintain styling

### Hero Section
Located at the top of the page with the main heading:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight tracking-tight text-gray-900 mb-6">
    Overland Park, Kansas Corporate Headshot Photography Services
</h1>
```
- Update the text while keeping the classes intact
- The classes ensure proper responsive sizing:
  - `text-4xl`: Base size for mobile
  - `md:text-5xl`: Medium screens
  - `lg:text-6xl`: Large screens

### Services Section
Each service card follows this structure:
```html
<div class="bg-white rounded-xl shadow-lg p-8 hover:shadow-xl transition-shadow duration-300">
    <h3 class="text-xl font-semibold mb-4">Professional Lighting</h3>
    <p class="text-gray-600">Studio-quality lighting setup...</p>
</div>
```
To modify:
1. Change the heading text in the `<h3>` tag
2. Update the description in the `<p>` tag
3. Keep all classes to maintain styling and hover effects

## Fixing Broken Links

### Navigation Menu Links
Current internal links in the navigation:
```html
<a href="#services">Services</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact Us</a>
```

To update:
1. For internal section links:
   - Keep the `#` prefix
   - Ensure the href matches the `id` of the target section
   - Example: `href="#services"` links to `<section id="services">`

2. For external links:
   - Replace the href with the full URL
   - Example: `<a href="https://www.example.com">Link</a>`

### Book Now Button
Located in multiple sections:
```html
<a href="https://www.101headshots.com" class="inline-block px-8 py-4 bg-blue-600...">
    Book Your Session
</a>
```
Update the `href` attribute with your booking page URL.

## Linking Privacy and Terms Pages

### Footer Legal Links
Current placeholder links:
```html
<div>
    <h4 class="text-lg font-semibold text-white mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add proper links:
1. Create your privacy.html and terms.html files
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
- Check that section IDs match exactly with href values
- IDs are case-sensitive
- Example: `href="#FAQ"` won't link to `id="faq"`

2. **Responsive Design Issues**
- Don't remove `md:` or `lg:` prefixes from classes
- These control how elements appear on different screen sizes
- Example: `class="text-4xl md:text-5xl lg:text-6xl"`

3. **Style Changes Not Applying**
- Ensure you're modifying the correct element
- Check that you've kept all necessary Tailwind classes
- Classes must be exactly as written (spaces matter)

### Need Help?
If you encounter issues:
1. Check the browser's developer tools (F12) for errors
2. Verify all class names match the Tailwind documentation
3. Ensure all tags are properly closed
4. Compare against the original code provided above

Remember to always test changes across different screen sizes and browsers before deploying to production.