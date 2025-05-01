# Landing Page Maintenance Guide

This guide will help you maintain and customize your WebAgency landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your company name and navigation menu. To update:

1. **Company Name**
```html
<!-- Located in the header section -->
<a href="/" class="text-2xl font-bold bg-gradient-to-r from-blue-500 to-cyan-500 bg-clip-text text-transparent">WebAgency</a>
```
- Replace "WebAgency" with your company name
- Keep the existing classes to maintain the gradient effect

### Hero Section
The main headline and subheading are in the hero section:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold mb-6 bg-gradient-to-r from-blue-500 to-cyan-500 bg-clip-text text-transparent">Best Web Agency In Sydney</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12">Grow your business with clicks</p>
```
- Update the h1 text to your main headline
- Modify the paragraph text for your subheading
- The `md:` and `lg:` prefixes control responsive text sizes - keep these for proper mobile display

### Features Section
Each feature card follows this structure:
```html
<div class="bg-gray-700 rounded-2xl p-8 hover:scale-105 transition-transform duration-300">
    <div class="w-16 h-16 bg-blue-600 rounded-full flex items-center justify-center mb-6">
        <i class="fas fa-magic text-2xl"></i>
    </div>
    <h3 class="text-xl font-semibold mb-4">Easy to Use</h3>
    <p class="text-gray-300">Intuitive interfaces and user-friendly designs...</p>
</div>
```
To modify:
1. Change the icon by updating the `fas fa-magic` class to any [Font Awesome](https://fontawesome.com/icons) icon
2. Update the h3 title text
3. Modify the description paragraph
4. Keep all Tailwind classes to maintain styling and hover effects

## Managing Links

### Navigation Menu Links
Current navigation links are:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="hover:text-blue-400 transition-colors duration-300">Features</a>
    <a href="#benefits" class="hover:text-blue-400 transition-colors duration-300">Benefits</a>
    <a href="#faq" class="hover:text-blue-400 transition-colors duration-300">FAQ</a>
    <a href="#contact" class="hover:text-blue-400 transition-colors duration-300">Contact</a>
</div>
```

To update:
1. The `href="#features"` links to section IDs on the page
2. For external links, replace with full URLs: `href="https://example.com"`
3. For internal pages, use relative paths: `href="/about.html"`

### Call-to-Action Links
Current CTA buttons point to "https://fixrr.online". Update these in two locations:
```html
<!-- Header CTA -->
<a href="https://fixrr.online" class="hidden md:block px-6 py-2 bg-blue-600 hover:bg-blue-700 rounded-full">

<!-- Hero Section CTA -->
<a href="https://fixrr.online" class="inline-block px-8 py-4 bg-blue-600 hover:bg-blue-700 rounded-full">
```

### Contact Information
Update email and social links in the contact section:
```html
<a href="mailto:contact@example.com" class="text-blue-400 hover:text-blue-300">contact@example.com</a>
```

## Adding Privacy and Terms Pages

### Footer Modification
Add privacy and terms links to the Quick Links section:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Quick Links</h4>
    <ul class="space-y-2">
        <!-- Existing links -->
        <li><a href="#features" class="text-gray-400 hover:text-white transition-colors duration-300">Features</a></li>
        <!-- Add new links -->
        <li><a href="/privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="/terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Ensure section IDs match exactly: `href="#features"` links to `id="features"`
   - Check for typos in IDs and hrefs
   - IDs are case-sensitive

2. **Responsive Design Issues**
   - Don't remove `md:` or `lg:` prefixes from classes
   - Keep the `hidden md:flex` class on the navigation menu for mobile responsiveness

3. **Icon Problems**
   - Verify Font Awesome is loading (check network tab in browser dev tools)
   - Ensure icon class names are correct (e.g., `fas fa-magic`)
   - Reference the [Font Awesome documentation](https://fontawesome.com/icons) for correct class names

### Need Help?
If you encounter issues:
1. Use browser developer tools (F12) to inspect elements
2. Check the console for error messages
3. Verify all files are in the correct directory
4. Ensure all links use the correct relative or absolute paths

Remember to test all changes across different devices and browsers to ensure consistency.