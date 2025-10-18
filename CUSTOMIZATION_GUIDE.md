# Customization Guide

This guide will help you customize your portfolio with your personal information, projects, and photos.

## 🎯 Quick Customization Checklist

- [ ] Update hero section text
- [ ] Add your professional summary
- [ ] Update project information (2 projects)
- [ ] Add your profile photo
- [ ] Add project images
- [ ] Update contact information
- [ ] Review and adjust colors/theme (optional)

## 📝 Content Updates

### 1. Hero Section (Introduction)

**File**: `src/pages/index.astro`

Update lines 14-23 with your information:

```astro
<div class="text-5xl font-bold">I'm Omar Carreón</div>
<div class="text-3xl py-3 font-bold">Software Engineer</div>
```

**What to update**:
- Your name
- Your professional title/role
- Your bio/professional summary
- Location (if you want to add it)

### 2. Projects Section

**File**: `src/pages/index.astro`

Find the two `HorizontalCard` components (around lines 36-49) and update with your project details:

```astro
<HorizontalCard
  title="Your Project Name"
  img="/your-project-image.webp"
  desc="Brief description of what your project does and technologies used"
  url="https://github.com/omarcarreon/your-project"
  badge="Featured"  // Optional: "Featured", "NEW", etc.
/>
```

**For each project, provide**:
- **title**: Project name
- **img**: Path to project screenshot (place in `/public` folder)
- **desc**: 1-2 sentence description highlighting key features and tech stack
- **url**: Link to GitHub repo or live demo
- **badge**: Optional tag (e.g., "Featured", "Open Source", "In Progress")

### 3. Contact Section

**File**: `src/pages/index.astro`

The contact section (lines 51-61) is already set up with your LinkedIn. You can:
- Add your email address
- Add a contact form
- Link to other social profiles

Example with email:

```astro
<div class="py-2">
  <text class="text-lg">
    I'm always interested in hearing about new opportunities. 
    Reach me at <a href="mailto:your.email@example.com" class="text-primary hover:underline">your.email@example.com</a> 
    or connect on <a href="https://www.linkedin.com/in/omarcarreon/" target="_blank" class="text-primary hover:underline">LinkedIn</a>.
  </text>
</div>
```

### 4. Social Links

**File**: `src/components/SideBarFooter.astro`

The template currently shows:
- GitHub: https://github.com/omarcarreon
- LinkedIn: https://www.linkedin.com/in/omarcarreon/

To add more social links (Twitter, email, etc.), add new `<a>` tags with SVG icons. You can find icons at [SVG Repo](https://www.svgrepo.com/) or [Heroicons](https://heroicons.com/).

## 🖼️ Images

### Profile Photo

1. Prepare your photo:
   - Square aspect ratio (e.g., 500x500px)
   - Professional headshot recommended
   - Save as WebP format for best performance (or JPG/PNG)

2. Replace the file:
   - Place your photo in `/public/`
   - Name it `profile.webp` (or update `src/components/SideBar.astro` line 15)

### Project Images

1. Prepare screenshots:
   - Landscape format works best (e.g., 1200x630px)
   - Show the key feature or UI of your project
   - Save as WebP format

2. Add to project:
   - Place images in `/public/` folder
   - Name them descriptively (e.g., `project-chatbot.webp`)
   - Reference in the `img` property of `HorizontalCard`

## 🎨 Styling & Theme

### Colors

The template uses DaisyUI themes. To change the color scheme:

**File**: `tailwind.config.cjs`

```javascript
daisyui: {
  themes: ["light", "dark"],  // Change these theme names
}
```

Available themes: light, dark, cupcake, bumblebee, emerald, corporate, synthwave, retro, cyberpunk, valentine, halloween, garden, forest, aqua, lofi, pastel, fantasy, wireframe, black, luxury, dracula, cmyk, autumn, business, acid, lemonade, night, coffee, winter

### Typography

To change fonts:

**File**: `src/styles/global.css`

Add your preferred Google Font or system font.

## 📊 From Resume to Portfolio

Here's how to extract content from your resume:

### Professional Summary
- Use your resume's "About Me" or "Summary" section
- Keep it to 2-3 sentences for the hero section

### Projects
For each project on your resume:
1. **Title**: Use the project name
2. **Description**: Condense the project description to 1-2 sentences
3. **Tech Stack**: Mention in the description (e.g., "Built with React, Node.js, and MongoDB")
4. **Link**: Add GitHub link or live demo URL

### Skills
While this template doesn't have a dedicated skills section, you can:
- Mention skills in your bio
- Include them in project descriptions
- Add a skills section if needed (requires creating a new component)

## 🔧 Advanced Customization

### Add a CV/Resume Download Button

In `src/pages/index.astro`, add a button in the hero section:

```astro
<a href="/resume.pdf" download class="btn btn-outline">
  Download Resume
</a>
```

Then place your `resume.pdf` file in the `/public` folder.

### Remove Unused Pages

The template includes blog, store, and services pages. To hide them:

1. They're already removed from the menu
2. Optionally delete the files:
   - `/src/pages/blog/`
   - `/src/pages/store/`
   - `/src/pages/services.astro`
   - `/src/pages/cv.astro`
   - `/src/pages/projects.astro`

## 📱 Testing Your Changes

After making changes:

```bash
# Start dev server
npm run dev

# Open browser to http://localhost:4321
# Check on desktop and mobile views
```

Use browser dev tools (F12) to test responsive design.

## ✅ Final Checks Before Deployment

- [ ] All personal information is accurate
- [ ] Profile photo looks good
- [ ] Project links work
- [ ] Social links are correct
- [ ] No placeholder text remaining
- [ ] Site looks good on mobile
- [ ] All images load properly
- [ ] No broken links

---

Need help? Check out the [Astro documentation](https://docs.astro.build) or the [DaisyUI docs](https://daisyui.com/).

