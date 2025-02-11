# The Gift Game Landing Page - Maintenance Guide

This guide will help you maintain and customize The Gift Game landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the main navigation and logo. To update:

1. **Logo Text:**
```html
<!-- Find this section near the top -->
<a href="/" class="text-2xl font-bold bg-gradient-to-r from-purple-600 to-pink-600 bg-clip-text text-transparent">
    The Gift Game  <!-- Change this text to update the logo -->
</a>
```

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <!-- Each link can be modified here -->
    <a href="#features" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Features</a>
</div>
```

### Hero Section
The main headline and subtitle appear in the hero section:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8 bg-gradient-to-r from-purple-600 to-pink-600 bg-clip-text text-transparent">
    The Art of Gift Giving: For Him and For Her  <!-- Main headline -->
</h1>
<p class="text-xl text-gray-600 mb-12">
    Discover the perfect gift for every occasion...  <!-- Subtitle -->
</p>
```

### Understanding Tailwind Classes
Common classes used throughout:
- `text-[size]`: Controls text size (e.g., `text-xl`, `text-2xl`)
- `font-[weight]`: Controls text weight (e.g., `font-bold`, `font-medium`)
- `mb-[size]`: Adds margin bottom (e.g., `mb-8`, `mb-12`)
- `px-[size]`: Adds horizontal padding (e.g., `px-6`)
- `py-[size]`: Adds vertical padding (e.g., `py-4`)

## Managing Links

### Navigation Links
Current navigation links are:

```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To update a link:
1. Locate the `<a>` tag
2. Modify the `href` attribute
3. Update the text between the tags

Example:
```html
<!-- From -->
<a href="#features">Features</a>

<!-- To -->
<a href="/new-page">New Page</a>
```

### Call-to-Action Buttons
The main CTA buttons currently point to "https://giftswrapping.com". To update:

```html
<!-- Find buttons like this -->
<a href="https://giftswrapping.com" class="inline-block px-8 py-4 bg-gradient-to-r from-purple-600 to-pink-600 text-white rounded-full">
    Start Finding Gifts
</a>

<!-- Replace the href with your new URL -->
<a href="https://your-new-url.com" class="inline-block px-8 py-4 bg-gradient-to-r from-purple-600 to-pink-600 text-white rounded-full">
    Start Finding Gifts
</a>
```

## Adding Privacy and Terms Pages

### Footer Links
The footer contains placeholder links for Privacy Policy and Terms of Service:

```html
<div>
    <h4 class="text-white text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <!-- Update these href attributes -->
        <li><a href="/privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="/terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To link to new pages:
1. Create `privacy.html` and `terms.html` in your root directory
2. Update the href attributes as shown above
3. Ensure the new pages use consistent styling

## Troubleshooting

Common issues and solutions:

1. **Broken Internal Links:**
   - Ensure all internal links start with `#` for same-page navigation
   - Check that section IDs match exactly (case-sensitive)

2. **Responsive Design Issues:**
   - Don't remove `md:` or `lg:` prefixes from classes
   - Keep the `container` class on parent elements
   - Maintain the existing grid structure in responsive sections

3. **Gradient Text Not Showing:**
   - Ensure all three classes are present:
     ```html
     bg-gradient-to-r from-purple-600 to-pink-600 bg-clip-text text-transparent
     ```

4. **Navigation Menu Hidden on Mobile:**
   - The `hidden md:flex` class combination is intentional for mobile responsiveness
   - Don't remove unless implementing a mobile menu alternative

Remember to test all changes across different screen sizes using your browser's developer tools (F12 or right-click > Inspect).

For additional help or more complex modifications, consult the [Tailwind CSS documentation](https://tailwindcss.com/docs) or reach out to your development team.