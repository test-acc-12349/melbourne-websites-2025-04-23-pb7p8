# Melbourne Websites Landing Page - Maintenance Guide

This guide will help you maintain and customize the Melbourne Websites landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the main navigation and brand name. To update:

1. **Company Name:**
```html
<a href="#" class="text-2xl font-bold text-white hover:text-blue-400 transition duration-300">
    Melbourne Websites  <!-- Change this text -->
</a>
```

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-300 hover:text-white transition duration-300">Features</a>
    <!-- Modify text within each <a> tag -->
</div>
```

### Hero Section
Update the main headline and subheading:

```html
<h1 class="text-4xl md:text-5xl lg:text-7xl font-bold mb-8 bg-gradient-to-r from-blue-400 to-purple-500 bg-clip-text text-transparent">
    Best Websites In Melbourne  <!-- Change headline here -->
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12 max-w-3xl mx-auto">
    Creating stunning, high-performance websites...  <!-- Change description here -->
</p>
```

### Tailwind CSS Tips
- `text-{size}`: Controls font size (xl, 2xl, 3xl, etc.)
- `md:text-{size}`: Applies style at medium screen sizes
- `bg-{color}-{shade}`: Changes background color
- `hover:`: Adds hover effects
- `transition`: Enables smooth transitions

## Managing Links

### Navigation Links
Current internal links in the navigation:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To update:
1. Internal links (same page): Use `#section-id`
2. External links: Use full URL
   ```html
   <a href="https://your-domain.com/page">Link Text</a>
   ```

### Call-to-Action Buttons
Update the "Get Started" links:
```html
<!-- Header CTA -->
<a href="https://twd.com" class="hidden md:block px-6 py-2 bg-blue-600">
    Get Started
</a>

<!-- Hero CTA -->
<a href="https://twd.com" class="inline-block px-8 py-4 bg-blue-600">
    Start Your Project
</a>
```

Replace `https://twd.com` with your actual URL.

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
Create two new files in your project directory:
- `privacy.html`
- `terms.html`

### Step 2: Update Footer Links
Locate the footer section and modify the legal links:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2 text-gray-400">
        <li><a href="privacy.html" class="hover:text-white transition duration-300">Privacy Policy</a></li>
        <li><a href="terms.html" class="hover:text-white transition duration-300">Terms of Service</a></li>
    </ul>
</div>
```

### Step 3: Maintain Consistent Styling
Copy these classes to maintain consistent link styling:
```html
class="hover:text-white transition duration-300"
```

## Troubleshooting

### Common Issues and Solutions

1. **Links Not Working**
   - Check for typos in `href` attributes
   - Ensure file names match exactly
   - Verify file locations are correct

2. **Responsive Design Issues**
   - Keep the `md:` prefix for medium screen styles
   - Don't remove `hidden md:flex` from navigation
   - Maintain existing responsive classes

3. **Styling Problems**
   - Don't remove `transition duration-300` classes
   - Keep gradient classes intact
   - Maintain the existing color scheme classes

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Verify all changes in multiple browsers
- Test responsive design using browser dev tools
- Make one change at a time and test

Remember to:
- Back up files before making changes
- Test all links after updates
- Verify changes on mobile and desktop
- Keep the original structure intact
- Maintain existing accessibility features

This landing page uses modern design practices - be careful when modifying the existing structure to maintain its professional appearance and functionality.