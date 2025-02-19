# Landing Page Maintenance Guide
## For SewingManuals.xyz

This guide provides detailed instructions for maintaining and customizing the SewingManuals.xyz landing page. Whether you're new to web development or need a quick reference, you'll find step-by-step guidance for common maintenance tasks.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your site name and navigation menu. To update:

1. **Site Name:**
```html
<div class="text-xl font-bold text-gray-800">
    SewingManuals.xyz  <!-- Change this text -->
</div>
```

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>  <!-- Update text here -->
    <a href="#benefits">Benefits</a>  <!-- And here -->
    <!-- etc. -->
</div>
```

### Hero Section
Update the main headline and subtitle:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6 leading-tight">
    Sewing Machine Manuals & Troubleshooting – Find, Fix, Sew!  <!-- Main headline -->
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-8">
    Easily find manuals & fix your sewing machine today!  <!-- Subtitle -->
</p>
```

### Tailwind CSS Classes Explained
Common classes used throughout:
- `text-[size]`: Controls text size (xl, 2xl, 3xl, etc.)
- `font-[weight]`: Controls text weight (bold, semibold, etc.)
- `bg-[color]`: Sets background color
- `text-[color]`: Sets text color
- `px-[size]` and `py-[size]`: Sets padding
- `mb-[size]`: Sets margin bottom

Example modification:
```html
<!-- Original -->
<div class="text-xl font-bold text-gray-800">

<!-- To make text larger and blue -->
<div class="text-2xl font-bold text-blue-800">
```

## Managing Links

### Navigation Menu Links
Current internal links in the navigation:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To update:
1. The `#` symbol indicates an internal page link
2. Match the href value to the section's ID
3. Example: `<a href="#new-section">New Section</a>`

### Call-to-Action Links
Current CTA links:
```html
<a href="https://shrsl.com/4ud5g" class="inline-block bg-blue-600 text-white...">
    Find Your Manual Now
</a>
```

To update:
1. Replace the URL in `href=""`
2. Update button text between `<a>` tags
3. Maintain the existing classes for consistent styling

## Adding Privacy and Terms Pages

### Footer Link Updates
Locate the footer links section:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Links</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To link to new pages:
1. Create `privacy.html` and `terms.html` in your root directory
2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Ensure section IDs match href values exactly
   - Check for typos in IDs
   - IDs are case-sensitive

2. **Responsive Design Issues**
   - Don't remove `md:` or `lg:` prefixes from classes
   - Keep the viewport meta tag in the header
   - Test on multiple screen sizes

3. **Style Inconsistencies**
   - Copy existing class combinations for new elements
   - Maintain color scheme using provided color classes
   - Keep spacing consistent using existing margin/padding classes

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Verify Font Awesome icon names in their [icon library](https://fontawesome.com/icons)
- Test links using your browser's developer tools (F12)

Remember to always test changes in multiple browsers and screen sizes before publishing updates.

This guide covers the basics of maintaining your landing page. For additional assistance or complex modifications, consider consulting with a web developer.