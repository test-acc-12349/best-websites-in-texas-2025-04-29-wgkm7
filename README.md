# Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the TexasWeb landing page. Follow these steps carefully to make updates while preserving the page's functionality and design.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the company logo and navigation menu. To update:

1. **Company Name/Logo**
```html
<!-- Located in header section -->
<span class="text-2xl font-bold text-primary">TexasWeb</span>
```
- Replace "TexasWeb" with your company name
- Adjust text size using Tailwind classes:
  - `text-xl` (smaller)
  - `text-2xl` (current size)
  - `text-3xl` (larger)

### Hero Section
The main banner section contains your primary headline and call-to-action:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight tracking-tight mb-6">
    Custom Websites For Your Business
</h1>
```
- Update headline text between the `<h1>` tags
- Responsive sizing is handled by:
  - `text-4xl` (mobile)
  - `md:text-5xl` (tablet)
  - `lg:text-6xl` (desktop)

### Features Cards
Each feature card follows this structure:
```html
<div class="p-8">
    <div class="flex items-center justify-center w-16 h-16 bg-blue-100 rounded-full mb-6">
        <i class="fas fa-mouse-pointer text-2xl text-primary"></i>
    </div>
    <h3 class="text-xl font-bold text-gray-900 mb-3">Easy to use</h3>
    <p class="text-gray-600">Intuitive interfaces that make managing your website simple...</p>
</div>
```
To modify:
1. Change icon by updating the `fa-mouse-pointer` class with any [Font Awesome](https://fontawesome.com/icons) icon
2. Update heading text in the `<h3>` tag
3. Modify description in the `<p>` tag

## Fixing Broken Links

### Navigation Menu Links
Current navigation links are:
```html
<nav class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-primary transition-colors duration-300 font-medium">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-primary transition-colors duration-300 font-medium">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-primary transition-colors duration-300 font-medium">FAQ</a>
    <a href="#contact" class="text-gray-600 hover:text-primary transition-colors duration-300 font-medium">Contact</a>
</nav>
```

To update:
1. Internal links (starting with #) connect to section IDs on the same page
2. For external links, replace `href="#features"` with your full URL: `href="https://yoursite.com/page"`
3. Maintain the same class structure to preserve styling

### Call-to-Action Links
Current CTA links point to "sigmaseo.io":
```html
<a href="https://sigmaseo.io" class="inline-flex items-center justify-center px-8 py-3 border border-transparent text-base font-medium rounded-md text-white bg-primary hover:bg-secondary transition-all duration-300 transform hover:scale-105 shadow-lg">Get Started</a>
```

Replace all instances of `https://sigmaseo.io` with your desired URL.

## Linking Privacy and Terms Pages

### Footer Legal Links
Current placeholder links:
```html
<ul class="space-y-2">
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Cookie Policy</a></li>
</ul>
```

To link policy pages:
1. Create your policy pages (e.g., `privacy.html`, `terms.html`)
2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Ensure section IDs match navigation links exactly
   - Example: `href="#features"` must link to `<section id="features">`

2. **Responsive Design Issues**
   - Don't remove responsive classes (e.g., `md:`, `lg:` prefixes)
   - Test on multiple screen sizes after changes

3. **Icon Not Displaying**
   - Verify Font Awesome is loading properly
   - Check icon class names against Font Awesome documentation

4. **Style Problems**
   - Keep Tailwind class order consistent
   - Don't remove utility classes without understanding their purpose
   - Test hover and transition effects after changes

Need more help? Contact technical support or refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs).