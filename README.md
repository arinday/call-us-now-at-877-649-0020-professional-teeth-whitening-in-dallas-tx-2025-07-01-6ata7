# BrightSmile Landing Page - Maintenance Guide

This guide will help you maintain and customize the BrightSmile dental landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company logo and navigation menu. To modify:

1. **Company Name/Logo**
```html
<a href="/" class="text-2xl font-bold text-blue-600">BrightSmile</a>
```
- Replace "BrightSmile" with your company name
- Adjust size using `text-2xl` (options: text-lg, text-xl, text-3xl)
- Change color using `text-blue-600` (options: text-[color]-[shade])

2. **Navigation Menu Items**
```html
<div class="hidden md:flex space-x-8">
    <a href="#services" class="text-gray-600 hover:text-blue-600">Services</a>
    <!-- Additional menu items -->
</div>
```
- Replace text between `<a>` tags
- Maintain the `hidden md:flex` class for mobile responsiveness
- `space-x-8` controls spacing between items

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-6">
    Professional Teeth Whitening in Dallas, TX
</h1>
```
- Update heading text while keeping the responsive classes
- `text-4xl`: mobile size
- `md:text-5xl`: tablet size
- `lg:text-6xl`: desktop size

### Feature Cards
Each service feature is contained in a card:
```html
<div class="bg-white rounded-xl shadow-lg p-8">
    <h3 class="text-xl font-semibold mb-4">15-Min Response</h3>
    <p class="text-gray-600">Quick response time...</p>
</div>
```
- Modify heading and paragraph text
- Maintain padding (`p-8`) and margin (`mb-4`) classes
- Keep shadow classes for visual depth

## Managing Links

### Navigation Links
Current navigation links include:
- Services (`#services`)
- Benefits (`#benefits`)
- FAQ (`#faq`)
- Phone number (`tel:8776490020`)

To update:
1. Locate the navigation section in the header
2. Update `href` attributes:
```html
<!-- Before -->
<a href="#services" class="text-gray-600">Services</a>

<!-- After -->
<a href="#new-section" class="text-gray-600">New Section Name</a>
```

### Call-to-Action (CTA) Links
Main CTA button:
```html
<a href="https://professional-teeth-whitening-dallas-tx.netlify.app/" 
   class="inline-block bg-blue-600 text-white px-8 py-4 rounded-lg">
   Schedule Your Appointment
</a>
```
- Replace the `href` with your booking page URL
- Maintain all styling classes for consistent appearance

## Adding Privacy and Terms Pages

### Footer Link Setup
Locate the legal section in the footer:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white">Terms of Service</a></li>
    </ul>
</div>
```

To link privacy and terms pages:
1. Create privacy.html and terms.html in your project folder
2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Responsive Design**
- Check that you haven't removed important responsive classes like `md:` or `lg:`
- Verify all Tailwind CSS classes are spelled correctly
- Test on different screen sizes using browser dev tools

2. **Missing Styles**
If Tailwind styles aren't applying:
```html
<!-- Verify this line is in your head section -->
<script src="https://cdn.tailwindcss.com"></script>
```

3. **Links Not Working**
- Ensure file paths are correct relative to index.html
- Check for typos in href attributes
- Verify that linked pages exist in the correct location

### Best Practices
- Always test changes in multiple browsers
- Maintain consistent spacing and padding
- Keep the responsive design intact
- Back up files before making major changes

Need more help? Contact your web development team or refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs).