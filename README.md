# Omar Carreón - Portfolio

A clean, modern one-page portfolio website built with Astro and Tailwind CSS.

## 🚀 Live Site

Once deployed: [https://omarcarreon.github.io/portfolio](https://omarcarreon.github.io/portfolio)

## ✨ Features

- **Hero Section**: Introduction with name, title, and professional summary
- **Featured Projects**: Showcase of 2 personal projects
- **Contact Section**: Easy ways to get in touch
- **Responsive Design**: Works beautifully on all devices
- **Dark Mode**: Built-in dark mode support
- **Fast & Lightweight**: Built with Astro for optimal performance

## 🛠️ Tech Stack

- [Astro](https://astro.build) - Static site generator
- [Tailwind CSS](https://tailwindcss.com) - Styling
- [DaisyUI](https://daisyui.com) - Component library
- GitHub Pages - Hosting

## 📦 Getting Started

### Prerequisites

- Node.js 18+ and npm

### Installation

1. Clone the repository:
```bash
git clone https://github.com/omarcarreon/portfolio.git
cd portfolio
```

2. Install dependencies:
```bash
npm install
```

3. Start the development server:
```bash
npm run dev
```

The site will be available at `http://localhost:4321`

## 🎨 Customization

### Update Personal Information

Edit the following files to customize your content:

- **`src/pages/index.astro`** - Main content (hero, projects, contact)
- **`src/config.ts`** - Site title and description
- **`src/components/SideBarFooter.astro`** - Social media links
- **`public/profile.webp`** - Replace with your profile photo

### Add Project Details

In `src/pages/index.astro`, update the `HorizontalCard` components with your project information:

```astro
<HorizontalCard
  title="Your Project Name"
  img="/project-image.webp"
  desc="Your project description"
  url="https://github.com/yourusername/project"
  badge="Featured"
/>
```

## 🚀 Deployment to GitHub Pages

### First Time Setup

1. Create a new repository on GitHub named `portfolio`

2. Add the remote and push:
```bash
git remote add origin https://github.com/omarcarreon/portfolio.git
git add .
git commit -m "Initial commit"
git branch -M main
git push -u origin main
```

3. Deploy to GitHub Pages:
```bash
npm run deploy
```

4. Enable GitHub Pages:
   - Go to your repository on GitHub
   - Navigate to **Settings** → **Pages**
   - Under **Source**, select the `gh-pages` branch
   - Click **Save**

Your site will be live at `https://omarcarreon.github.io/portfolio` in a few minutes!

### Subsequent Deployments

After making changes, simply run:

```bash
npm run deploy
```

## 📝 Available Scripts

- `npm run dev` - Start development server
- `npm run build` - Build for production
- `npm run preview` - Preview production build locally
- `npm run deploy` - Deploy to GitHub Pages

## 📄 License

This project is based on the [Astrofy](https://github.com/manuelernestog/astrofy) template by Manuel Ernesto.

## 🤝 Connect

- LinkedIn: [linkedin.com/in/omarcarreon](https://www.linkedin.com/in/omarcarreon/)
- GitHub: [github.com/omarcarreon](https://github.com/omarcarreon)
