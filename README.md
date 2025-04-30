# Landing Page Maintenance Guide

This guide will help you maintain and customize your landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates while preserving the design integrity.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your logo and navigation menu. To update:

1. **Logo Text**
```html
<div class="text-2xl font-bold bg-gradient-to-r from-purple-600 to-pink-600 bg-clip-text text-transparent">
    Logo <!-- Replace "Logo" with your company name -->
</div>
```

2. **Navigation Menu Items**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a> <!-- Update text within these links -->
    <a href="#benefits">Benefits</a>
    <a href="#contact">Contact</a>
</div>
```

### Hero Section
Located at the top of the page after the header:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8">
    Lorem ipsum dolor <!-- Replace with your main headline -->
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">
    Lorem ipsum dolor <!-- Replace with your subheading -->
</p>
```

### Tailwind CSS Class Guide
- `text-4xl`: Large text size (increases with `md:` and `lg:` prefixes)
- `mb-8`: Margin bottom spacing (8 units)
- `bg-white`: White background
- `text-gray-600`: Gray text color
- `hover:scale-105`: Grows element to 105% on hover

## Managing Links

### Navigation Menu Links
Current internal links point to page sections:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#contact">Contact</a>
```

To update:
1. For internal sections: Keep the `#` prefix
2. For external pages: Replace with full URL
```html
<a href="https://yoursite.com/about">About</a>
```

### Footer Links
The footer contains multiple link sections:
```html
<!-- Company Links -->
<ul class="space-y-2">
    <li><a href="#">About</a></li> <!-- Replace "#" with actual URLs -->
    <li><a href="#">Careers</a></li>
    <li><a href="#">Contact</a></li>
</ul>
```

To update links:
1. Locate the `<a href="#">` tag
2. Replace `#` with your URL
3. Update the text between `<a>` tags

## Adding Privacy and Terms Pages

### Footer Legal Section
Locate the legal section in the footer:
```html
<div>
    <h4 class="font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="privacy.html" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Privacy</a></li>
        <li><a href="terms.html" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Terms</a></li>
    </ul>
</div>
```

To link privacy and terms pages:
1. Create `privacy.html` and `terms.html` in your root directory
2. Update the href attributes as shown above
3. Maintain consistent styling by copying the classes

## Troubleshooting

### Common Issues

1. **Broken Links**
   - Check for typos in URLs
   - Ensure files exist in the specified location
   - Verify that `href` attributes include the correct file extension

2. **Styling Problems**
   - Check for missing class names
   - Ensure Tailwind CSS is properly loaded
   - Verify that responsive classes (md:, lg:) are correctly formatted

3. **Layout Issues**
   - Maintain the container structure:
   ```html
   <div class="container mx-auto px-6">
       <!-- Content here -->
   </div>
   ```
   - Keep the responsive grid system intact:
   ```html
   <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3">
   ```

### Need Help?
- Double-check the Tailwind CSS version (currently using 2.2.19)
- Verify Alpine.js is loading correctly
- Ensure all sections have matching opening and closing tags
- Maintain the existing responsive design patterns

Remember to test all changes across different screen sizes using your browser's developer tools.