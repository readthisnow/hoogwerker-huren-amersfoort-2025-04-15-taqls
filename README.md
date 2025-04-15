# Landing Page Maintenance Guide

This guide will help you maintain and customize the Hoogwerker Huren Amersfoort landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Text Content Updates

#### Header Section
```html
<header class="sticky top-0 z-50 bg-white shadow-md">
    <nav class="container mx-auto px-4 py-4 flex items-center justify-between">
        <a href="/" class="text-2xl font-bold">Hoogwerker</a>
        <!-- Navigation items -->
    </nav>
</header>
```
To update the company name:
1. Locate the `<a>` tag with "Hoogwerker"
2. Replace "Hoogwerker" with your desired text
3. Keep the class attributes unchanged to maintain styling

#### Hero Section
```html
<div class="relative text-center text-white max-w-4xl mx-auto px-4">
    <h1 class="text-4xl md:text-6xl font-bold mb-6">Hoogwerker Huren Amersfoort</h1>
    <p class="text-xl md:text-2xl mb-8">Schrijf Alles Over Dit Product In Het Nederlands</p>
</div>
```
To update the hero text:
1. Replace the h1 content for the main title
2. Update the paragraph text
3. The `md:text-6xl` class makes text larger on desktop screens

### Tailwind CSS Modifications

#### Understanding Responsive Classes
- `md:` prefix = applies styles on medium screens and larger
- `lg:` prefix = applies styles on large screens and larger
- Example: `text-4xl md:text-6xl` means:
  - `text-4xl` (smaller screens): font-size of 2.25rem
  - `md:text-6xl` (medium screens): font-size of 3.75rem

#### Common Class Modifications
```html
<!-- Button styling example -->
<a href="#" class="bg-blue-600 text-white px-6 py-2 rounded-full hover:bg-blue-700">
```
To modify button colors:
1. Replace `bg-blue-600` with desired color (e.g., `bg-red-600`)
2. Update hover state `hover:bg-blue-700` accordingly
3. Available colors: red, blue, green, yellow, gray, etc.
4. Numbers indicate shade (100-900)

## Managing Links

### Navigation Menu Links
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="hover:text-blue-600 transition-colors duration-300">Features</a>
    <a href="#benefits" class="hover:text-blue-600 transition-colors duration-300">Benefits</a>
    <a href="#faq" class="hover:text-blue-600 transition-colors duration-300">FAQ</a>
</div>
```
To update internal links:
1. Locate the `href` attribute
2. For internal sections, use `#section-id`
3. For external pages, use full URL: `https://example.com`

### External Links
Current external link:
```html
<a href="https://hoogwerkerhurenamersfoort.nl" class="bg-blue-600 text-white px-6 py-2">Contact Us</a>
```
To update:
1. Replace `https://hoogwerkerhurenamersfoort.nl` with your URL
2. Test the link after updating
3. Ensure URL includes `https://` prefix

## Adding Privacy and Terms Pages

### Footer Modification
Add these links to the footer section:
```html
<div class="grid grid-cols-1 md:grid-cols-4 gap-8">
    <!-- Existing footer content -->
    <div>
        <h3 class="text-xl font-bold mb-4">Legal</h3>
        <ul class="space-y-2">
            <li><a href="/privacy.html" class="hover:text-gray-300">Privacy Policy</a></li>
            <li><a href="/terms.html" class="hover:text-gray-300">Terms of Service</a></li>
        </ul>
    </div>
</div>
```

### Creating Policy Pages
1. Create new files:
   - `privacy.html`
   - `terms.html`
2. Use consistent styling:
```html
<!-- privacy.html/terms.html template -->
<!DOCTYPE html>
<html lang="nl" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Privacy Policy - Hoogwerker Huren Amersfoort</title>
    <link href="https://cdn.jsdelivr.net/npm/tailwindcss@2.2.19/dist/tailwind.min.css" rel="stylesheet">
</head>
<body class="font-sans antialiased">
    <!-- Copy header from index.html -->
    <main class="container mx-auto px-4 py-12">
        <h1 class="text-3xl font-bold mb-8">Privacy Policy</h1>
        <!-- Add your policy content here -->
    </main>
    <!-- Copy footer from index.html -->
</body>
</html>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Images**
   - Verify image URLs in `src` attributes
   - Ensure images are uploaded to correct location
   - Check file permissions

2. **Responsive Design Issues**
   - Test on multiple screen sizes
   - Verify `md:` and `lg:` classes are properly set
   - Use browser developer tools to inspect elements

3. **Link Problems**
   - Confirm all URLs start with `https://` or `/`
   - Test internal links match section IDs exactly
   - Check for typos in URLs

### Need Help?
- Review Tailwind CSS documentation for class references
- Use browser inspector to examine element styling
- Test all changes in multiple browsers
- Keep backup copies of working code

Remember to test all changes thoroughly before publishing to your live site.