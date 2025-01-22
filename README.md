# Roofing Newcastle Landing Page - Maintenance Guide

This guide will help you maintain and customize the Roofing Newcastle landing page. Whether you're new to HTML and CSS or just getting started, follow these detailed instructions to make updates safely and effectively.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your company name and navigation menu. To update:

1. **Company Name:**
```html
<a href="/" class="text-2xl font-bold text-blue-600">Roofing Newcastle</a>
```
- Replace "Roofing Newcastle" with your company name
- Keep the classes (`text-2xl font-bold text-blue-600`) to maintain styling

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition duration-300">Features</a>
    <!-- Other menu items -->
</div>
```
- Update text between `>` and `</a>` tags
- Maintain the class structure for consistent styling

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8 text-gray-900">
    Redefining Roofing: Innovative, Sustainable, Stylish
</h1>
```
- Update heading text while keeping the classes
- The `md:` and `lg:` prefixes control responsive text sizes
- `mb-8` adds margin bottom spacing

### Tailwind CSS Class Guide
Common classes used throughout:
- Text sizes: `text-xl`, `text-2xl`, `text-3xl`
- Colors: `text-blue-600`, `text-gray-900`
- Spacing: `px-4`, `py-2`, `mb-8`
- Hover effects: `hover:text-blue-600`, `hover:bg-blue-700`

## Managing Links

### Internal Links
These point to sections within the page:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
```
- The `#` symbol indicates an internal page section
- Ensure the href matches the section's ID attribute
- Example: `href="#features"` links to `<section id="features">`

### External Links
Current external links:
```html
<a href="https://briansavic.com/contact-us" class="px-6 py-2 bg-blue-600 text-white rounded-full">Contact Us</a>
```
To update:
1. Replace the URL in `href=""`
2. Test the new link
3. Maintain the classes for consistent styling

### Social Media Links
Located in the footer:
```html
<div class="flex space-x-4">
    <a href="#" class="hover:text-white transition duration-300">
        <!-- Social icon SVG -->
    </a>
</div>
```
- Replace `#` with your social media profile URLs
- Keep the SVG icons and classes for proper styling

## Adding Privacy and Terms Pages

### Step 1: Add Footer Links
Insert these lines in the footer's Quick Links section:
```html
<ul class="space-y-2">
    <!-- Existing links -->
    <li><a href="privacy.html" class="hover:text-white transition duration-300">Privacy Policy</a></li>
    <li><a href="terms.html" class="hover:text-white transition duration-300">Terms of Service</a></li>
</ul>
```

### Step 2: Create New Pages
1. Create `privacy.html` and `terms.html` in your root directory
2. Copy the header and footer from `index.html`
3. Add your policy content between them
4. Maintain consistent styling using the same Tailwind classes

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
- Check that section IDs match href attributes
- IDs are case-sensitive
- Example: `href="#FAQ"` won't link to `id="faq"`

2. **Responsive Design Issues**
- Don't remove `md:` or `lg:` prefixes from classes
- These control how elements appear on different screen sizes
- Test changes on mobile, tablet, and desktop views

3. **Style Inconsistencies**
- Copy existing classes when adding new elements
- Example: New buttons should use:
```html
class="px-6 py-2 bg-blue-600 text-white rounded-full hover:bg-blue-700 transition duration-300"
```

### Need Help?
- Review the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Test changes in a development environment first
- Keep a backup of the original files
- Use browser developer tools (F12) to inspect elements

Remember to always test your changes across different devices and browsers before publishing updates to your live site.