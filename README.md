# TegelDisplay Landing Page - Maintenance Guide

This guide will help you maintain and customize the TegelDisplay landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions to make updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Legal Pages](#adding-legal-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Text
The site header contains the brand name and navigation menu:
```html
<div class="text-2xl font-bold text-gray-800">TegelDisplay</div>
```
To update the brand name:
1. Locate this div in the header section
2. Replace "TegelDisplay" with your desired text
3. Adjust text size by modifying `text-2xl` to `text-xl` (smaller) or `text-3xl` (larger)

### Hero Section
The main promotional section includes:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6">
    🔥 Tegel Display <span class="text-red-600">Nu 20% Korting</span>
</h1>
```
To modify:
1. Change the emoji (🔥) or remove it
2. Update the promotional text
3. Adjust the discount amount in the red span
4. Maintain the responsive text sizes (`text-4xl`, `md:text-5xl`, `lg:text-6xl`)

### Tailwind CSS Classes Explained
Common classes used throughout:
- Size classes: `text-sm`, `text-xl`, `text-2xl` (text size)
- Spacing: `px-4`, `py-4` (padding), `mb-6`, `mt-4` (margin)
- Colors: `text-gray-900`, `bg-white`, `text-blue-600`
- Responsive prefixes: `md:`, `lg:` (apply at specific breakpoints)

## Managing Links

### Navigation Menu Links
Current internal links:
```html
<div class="hidden lg:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-gray-900">Features</a>
    <a href="#voordelen" class="text-gray-600 hover:text-gray-900">Voordelen</a>
    <a href="#faq" class="text-gray-600 hover:text-gray-900">FAQ</a>
    <a href="#contact" class="text-gray-600 hover:text-gray-900">Contact</a>
</div>
```
To update:
1. Locate the link you want to change
2. Modify the `href` attribute
   - For internal sections, use `#section-name`
   - For external links, use complete URLs (https://...)
3. Update the link text between `<a>` tags

### Call-to-Action Links
Current promotional links:
```html
<a href="https://amzn.to/3Eo8cYl" class="inline-block bg-blue-600 hover:bg-blue-700 text-white">
    Claim Nu Je Korting
</a>
```
To update:
1. Replace `https://amzn.to/3Eo8cYl` with your new URL
2. Modify button text as needed
3. Keep the styling classes to maintain appearance

## Adding Legal Pages

### Footer Modification
Add privacy and terms links to the footer:
```html
<div class="mt-12 pt-8 border-t border-gray-800 text-center text-gray-400">
    <p>&copy; 2024 TegelDisplay. Alle rechten voorbehouden.</p>
    <!-- Add this code below the copyright notice -->
    <div class="mt-4">
        <a href="privacy.html" class="text-gray-400 hover:text-white mr-4">Privacy Policy</a>
        <a href="terms.html" class="text-gray-400 hover:text-white">Terms & Conditions</a>
    </div>
</div>
```

### Creating Legal Pages
1. Create two new files:
   - `privacy.html`
   - `terms.html`
2. Use the same header and footer as `index.html`
3. Add your legal content in the main section

## Troubleshooting

### Common Issues
1. **Broken Layout**
   - Check for missing closing tags
   - Verify Tailwind CSS classes are spelled correctly
   - Ensure responsive classes use correct prefixes

2. **Missing Styles**
   - Confirm the Tailwind CDN link is working:
   ```html
   <script src="https://cdn.tailwindcss.com"></script>
   ```

3. **Non-Working Links**
   - Verify file names match exactly (case-sensitive)
   - Check for proper URL formatting
   - Ensure section IDs match navigation links

### Need Help?
- Double-check the HTML structure
- Use browser developer tools (F12) to inspect elements
- Maintain backup copies before making changes
- Test all changes on multiple devices and browsers

Remember to always test your changes in a development environment before pushing to production. For additional assistance, consult the [Tailwind CSS documentation](https://tailwindcss.com/docs) or reach out to your development team.