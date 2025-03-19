# PMP Bot Landing Page - Maintenance Guide

This guide will help you maintain and customize the PMP Bot landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the main navigation and logo. To update:

1. **Logo Text**: Find this line in the header:
```html
<a href="/" class="text-2xl font-bold bg-gradient-to-r from-purple-500 to-pink-500 bg-clip-text text-transparent">PMP Bot</a>
```
Replace "PMP Bot" with your desired text while keeping the classes intact.

2. **Navigation Items**: Located in both desktop and mobile menus:
```html
<a href="#features" class="text-gray-300 hover:text-white transition-colors duration-300">Features</a>
```
Update the text between `<a>` tags to change menu items.

### Hero Section
Find the main headline and subtitle:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8 bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text text-transparent">Study Anytime, Anywhere with Our Intelligent PMP Chatbot</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12">Get Ready for the PMP Exam with Instant Feedback</p>
```
- To modify text size, adjust the `text-4xl`, `text-5xl`, or `text-6xl` classes
- For spacing, modify `mb-8` (margin-bottom) values
- Keep the gradient classes to maintain the colorful text effect

### Features and Benefits
Each feature card follows this structure:
```html
<div class="bg-gray-800 rounded-2xl p-8 transform hover:scale-105 transition-all duration-300 hover:shadow-xl border border-gray-700">
    <h3 class="text-xl font-semibold mb-4">Feature Title</h3>
    <p class="text-gray-400">Feature description text here.</p>
</div>
```
- Update text between `<h3>` and `<p>` tags
- Maintain the classes for consistent styling
- The `hover:scale-105` creates the hover animation

## Managing Links

### Navigation Links
1. **Internal Links**: These scroll to page sections:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
```
- Ensure the href matches the section id (e.g., `id="features"`)
- Add new sections by creating a section with matching id

2. **External Links**: The "Get Started" button links to:
```html
<a href="https://pmp.aibizbots4u.com" class="px-6 py-2 rounded-full bg-gradient-to-r from-purple-600 to-pink-600">Get Started</a>
```
Replace the URL with your actual application link.

### Footer Links
Update contact information and links in the footer:
```html
<div>
    <h4 class="font-semibold mb-4">Contact</h4>
    <p class="text-gray-400">sales@aibizbots4u.com</p>
</div>
```
Replace email address and social media links as needed.

## Adding Privacy and Terms Pages

1. **Create New Files**
Create two new HTML files in your project:
- `privacy.html`
- `terms.html`

2. **Update Footer Links**
Replace the placeholder links:
```html
<!-- Find these lines in the footer -->
<li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>

<!-- Replace with -->
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Gradients**
If text gradients disappear, ensure these classes are present:
```html
bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text text-transparent
```

2. **Responsive Issues**
Check these breakpoint classes:
- `md:` (medium screens)
- `lg:` (large screens)
Example:
```html
class="text-4xl md:text-5xl lg:text-6xl"
```

3. **Missing Hover Effects**
Ensure transition classes are present:
```html
transition-colors duration-300
```

### Need Help?
- Double-check class names match exactly (Tailwind is case-sensitive)
- Verify all opening tags have matching closing tags
- Test the page at different screen sizes
- Keep the original code as a backup before making changes

Remember to test all changes in multiple browsers and screen sizes before deploying to production.