# DevAxis Website

A modern, professional portfolio website for DevAxis - showcasing software development, system automation, and innovation incubation services.

## Features

- 🎨 Modern, tech-forward design with neon accents
- 📱 Fully responsive (mobile, tablet, desktop)
- ⚡ Smooth animations and transitions
- 🎯 Clear service offerings and project showcase
- 📧 Contact form ready for integration
- 🚀 Optimized for GitHub Pages

## Quick Start

### Deploying to GitHub Pages

1. **Create a GitHub account** (if you don't have one)
   - Go to https://github.com
   - Sign up for free

2. **Create a new repository**
   - Click the '+' icon → 'New repository'
   - Name it: `yourusername.github.io` (replace 'yourusername' with your actual GitHub username)
   - Make it **Public**
   - Click 'Create repository'

3. **Upload these files**
   - Click 'Add file' → 'Upload files'
   - Drag and drop all files:
     - index.html
     - style.css
     - script.js
     - README.md
   - Click 'Commit changes'

4. **Your site is live!**
   - Visit: `https://yourusername.github.io`
   - It may take 1-2 minutes to deploy

## File Structure

```
devaxis-website/
├── index.html       # Main HTML file
├── style.css        # Stylesheet with all designs
├── script.js        # JavaScript for interactions
└── README.md        # This file
```

## Customization Guide

### Update Your Information

1. **Contact Details** (in index.html, lines ~420-450)
   - Email: Change `hello@devaxis.com`
   - Phone: Change `+123 456 7890`
   - Location: Already set to Nairobi, Kenya
   - Social media links: Add your Twitter, LinkedIn, GitHub URLs

2. **Projects** (in index.html, lines ~200-300)
   - Replace the example projects with your actual projects
   - Update titles, descriptions, and technologies
   - Add project images (see below)

3. **Statistics** (in index.html, lines ~90-110)
   - Update project counts
   - Modify client numbers
   - Adjust any metrics

### Adding Project Images

You can add actual project screenshots:

1. Create an `images` folder in your repository
2. Upload project screenshots
3. Update the project cards in index.html:

```html
<div class="project-image" style="background: url('images/project1.jpg') center/cover;">
```

### Color Customization

Want different colors? Edit these variables in `style.css` (lines 1-15):

```css
--primary: #00ff88;      /* Main accent color */
--secondary: #0affff;     /* Secondary accent */
--accent: #ff00ff;        /* Additional accent */
```

### Adding More Projects

Copy this block in index.html and modify:

```html
<div class="project-card">
    <div class="project-image">
        <div class="project-overlay">
            <span class="project-tag">Your Tag</span>
        </div>
    </div>
    <div class="project-content">
        <h3 class="project-title">Project Name</h3>
        <p class="project-description">Description here...</p>
        <div class="project-tech">
            <span class="tech-tag">Tech1</span>
            <span class="tech-tag">Tech2</span>
        </div>
        <a href="#" class="project-link">View Case Study →</a>
    </div>
</div>
```

## Integrating Contact Form

The contact form currently shows an alert. To make it functional:

### Option 1: Formspree (Free & Easy)
1. Go to https://formspree.io
2. Create free account
3. Create a form
4. Replace form submission in `script.js` (line 60):

```javascript
contactForm?.addEventListener('submit', async (e) => {
    e.preventDefault();
    const formData = new FormData(contactForm);
    
    try {
        const response = await fetch('https://formspree.io/f/YOUR_FORM_ID', {
            method: 'POST',
            body: formData,
            headers: { 'Accept': 'application/json' }
        });
        
        if (response.ok) {
            alert('Message sent successfully!');
            contactForm.reset();
        }
    } catch (error) {
        alert('Error sending message. Please try again.');
    }
});
```

### Option 2: EmailJS (Free)
1. Go to https://www.emailjs.com
2. Create account and email service
3. Follow their integration guide

### Option 3: Backend API
If you have your own backend, update the fetch URL to your API endpoint.

## Performance Tips

1. **Optimize images**: Compress all images before uploading
2. **Use WebP format**: Modern image format for better performance
3. **Lazy loading**: Add `loading="lazy"` to image tags

## Browser Support

- ✅ Chrome (latest)
- ✅ Firefox (latest)
- ✅ Safari (latest)
- ✅ Edge (latest)
- ✅ Mobile browsers

## Technologies Used

- HTML5
- CSS3 (with CSS Variables, Grid, Flexbox)
- Vanilla JavaScript (no frameworks)
- Google Fonts (Orbitron, IBM Plex Mono)

## Future Enhancements

Ideas for improvement:
- [ ] Add blog section
- [ ] Integrate CMS for easy content updates
- [ ] Add dark/light mode toggle
- [ ] Create case study pages for each project
- [ ] Add animations with Framer Motion
- [ ] Implement search functionality
- [ ] Add testimonials section
- [ ] Create admin dashboard for project management

## License

Free to use and modify for your business.

## Support

Questions? Contact:
- Email: hello@devaxis.com
- GitHub Issues: Create an issue in your repository

---

**Built with 💚 by DevAxis**
*Innovating Beyond Boundaries*
