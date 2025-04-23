# Alphington Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Alphington accounting services landing page. Follow these step-by-step instructions to make common updates while preserving the page's responsive design and functionality.

## 1. Updating Text and Tailwind CSS Classes

### Text Content Updates

#### Hero Section
```html
<!-- Located in the first section after the header -->
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6 leading-tight">
    We transform numbers into opportunities
</h1>
```
To update the main headline:
1. Locate the `<h1>` tag in the hero section
2. Replace the text between the opening and closing tags
3. Maintain the existing classes to preserve styling

#### Service Cards
Each service card follows this structure:
```html
<div class="bg-white p-8 rounded-2xl shadow-lg hover:shadow-xl transition-shadow duration-300">
    <h3 class="text-xl font-bold mb-4">Dedicated Manager</h3>
    <p class="text-gray-600 leading-relaxed">Your personal financial expert...</p>
</div>
```
To update service descriptions:
1. Find the service cards in the "Features Section"
2. Modify the text within the `<h3>` and `<p>` tags
3. Keep the existing classes to maintain styling

### Tailwind CSS Classes Explained

#### Common Class Patterns
- Spacing: `p-8` (padding), `mb-4` (margin-bottom)
- Colors: `text-gray-600`, `bg-blue-600`
- Responsive design: `md:text-4xl` (applies at medium screens)
- Hover effects: `hover:bg-blue-700`

#### Modifying Responsive Classes
Example:
```html
<div class="text-base md:text-lg lg:text-xl">
```
- `text-base`: Default size
- `md:text-lg`: Medium screens (768px+)
- `lg:text-xl`: Large screens (1024px+)

## 2. Fixing Broken Links

### Navigation Menu Links
Current navigation structure:
```html
<div class="hidden md:flex space-x-8">
    <a href="#services">Services</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To update links:
1. For internal section links:
   - Keep the `#` prefix
   - Ensure the href matches the section's ID
   - Example: `href="#services"` links to `<section id="services">`

2. For external links:
   - Replace `https://theaccountants.com` with your actual URL
   - Example: `<a href="https://your-domain.com/page">`

### Call-to-Action Buttons
```html
<a href="https://theaccountants.com" class="px-8 py-4 bg-blue-600 text-white rounded-lg">
    Get Started Today
</a>
```
To update:
1. Replace `https://theaccountants.com` with your desired URL
2. Test the link after updating

## 3. Linking Privacy and Terms Pages

### Footer Link Structure
Current footer links:
```html
<div>
    <h4 class="text-lg font-semibold text-white mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add privacy and terms pages:
1. Create your privacy.html and terms.html files
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting Tips

1. Broken Internal Links
- Check that section IDs match exactly with href attributes
- IDs are case-sensitive
- Example: `href="#FAQ"` won't link to `id="faq"`

2. Responsive Design Issues
- Test at different screen sizes using browser dev tools
- Verify media query classes (md:, lg:) are working
- Common breakpoints:
  - md: 768px
  - lg: 1024px

3. Styling Problems
- Check for missing classes
- Ensure Tailwind CDN is loading properly
- Verify class names match Tailwind conventions

## Best Practices

1. Always backup before making changes
2. Test all links after updating
3. View changes across different devices and browsers
4. Maintain consistent styling with existing elements
5. Keep the responsive design intact by preserving media query classes

Remember to:
- Test all changes in a development environment first
- Validate links before pushing to production
- Maintain consistent spacing and formatting
- Keep backup copies of the original files

For additional help, consult the [Tailwind CSS documentation](https://tailwindcss.com/docs) or reach out to your development team.