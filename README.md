# Texas Web Design Landing Page - Maintenance Guide

This guide will help you maintain and customize the Texas Web Design landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the logo and navigation menu. To modify:

1. **Logo Text**: 
```html
<a href="/" class="text-2xl font-bold text-blue-600">TWD</a>
```
- Replace "TWD" with your desired text
- Adjust size using `text-2xl` (options: text-sm, text-lg, text-3xl, etc.)

2. **Navigation Menu Items**:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-blue-600">Benefits</a>
    <a href="#contact" class="text-gray-600 hover:text-blue-600">Contact</a>
</div>
```
- Replace text between `<a>` tags
- Maintain the `hover:text-blue-600` class for consistent hover effects

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6">Best Websites In Texas</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">Professional web design solutions...</p>
```
- Update heading text between `<h1>` tags
- Modify subheading text between `<p>` tags
- Keep responsive classes (`md:text-5xl`, `lg:text-6xl`) for proper scaling

### Features Section
Each feature card follows this structure:
```html
<div class="p-8 bg-white rounded-2xl shadow-lg hover:shadow-xl">
    <h3 class="text-xl font-semibold mb-4">Feature Title</h3>
    <p class="text-gray-600">Feature description</p>
</div>
```
- Update titles in `<h3>` tags
- Modify descriptions in `<p>` tags
- Maintain padding (`p-8`) and shadow classes for consistent styling

## Managing Links

### Navigation Links
Current links in the navigation:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#contact">Contact</a>
<a href="https://twd.com">Get Started</a>
```
To update:
1. Internal links (starting with #): Match with section IDs
2. External links: Replace `https://twd.com` with your actual domain
3. Test all links after updating

### Call-to-Action Buttons
```html
<a href="https://twd.com" class="px-8 py-4 bg-blue-600 text-white rounded-full">Start Your Project</a>
```
- Update `href` attribute with your desired URL
- Maintain button styling classes for consistent appearance

### Footer Links
```html
<div class="space-y-2">
    <li><a href="#features">Features</a></li>
    <li><a href="#benefits">Benefits</a></li>
    <li><a href="#contact">Contact</a></li>
</div>
```
- Update `href` attributes to match corresponding section IDs
- Ensure all internal links have matching section IDs in the page

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
Create two new files:
- `privacy.html`
- `terms.html`

### Step 2: Update Footer Links
Replace placeholder links with actual page links:
```html
<!-- Original -->
<li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>

<!-- Updated -->
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

### Step 3: Maintain Consistent Styling
Copy these classes to maintain consistent link styling:
```html
class="hover:text-white transition-colors duration-300"
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
- Ensure section IDs match exactly (case-sensitive)
- Example: `href="#Features"` won't link to `id="features"`

2. **Responsive Design Issues**
- Don't remove `md:` or `lg:` prefixes from classes
- These ensure proper mobile responsiveness
- Example: `class="text-4xl md:text-5xl lg:text-6xl"`

3. **Styling Inconsistencies**
- Copy existing classes when adding new elements
- Maintain padding and margin patterns
- Example: `class="p-8 bg-white rounded-2xl shadow-lg"`

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Validate HTML at [W3C Validator](https://validator.w3.org/)
- Test responsiveness using browser developer tools

Remember to always test changes across different devices and browsers before deploying to production.