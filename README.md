# Modern Astro Portfolio

A beautiful, modern portfolio website built with Astro and Tailwind CSS.

## Features

- 🎨 Modern, responsive design with gradient effects
- 🚀 Built with Astro for optimal performance
- 💅 Styled with Tailwind CSS
- 📱 Fully responsive and mobile-friendly
- ⚡ Fast page loads and smooth animations
- 🎯 Sections for About, Skills, Projects, and Contact
- 📄 Resume download functionality
- 🔗 Social media links integration
- 🌐 Deployed on GitHub Pages

## Getting Started

### Installation

```bash
npm install
```

### Development

Start the development server:

```bash
npm run dev
```

Visit `http://localhost:4321` to see your portfolio.

### Build

Build for production:

```bash
npm run build
```

### Preview

Preview the production build:

```bash
npm run preview
```

## Deploy to GitHub Pages

This portfolio is configured to deploy automatically to GitHub Pages using GitHub Actions.

### Setup Instructions

1. **Create a GitHub repository** (if you haven't already):

   ```bash
   git init
   git add .
   git commit -m "Initial commit"
   git branch -M main
   git remote add origin https://github.com/abebelagua/portfolio.git
   git push -u origin main
   ```

2. **Enable GitHub Pages**:

   - Go to your repository on GitHub
   - Click on **Settings**
   - Scroll down to **Pages** in the left sidebar
   - Under **Source**, select **GitHub Actions**
   - Save the settings

3. **Configure the base URL** (if needed):

   - If your repository is named `portfolio`, the site will be available at: `https://abebelagua.github.io/portfolio`
   - If you want it at `https://abebelagua.github.io`, rename your repository to `abebelagua.github.io` and update `astro.config.mjs`:
     ```js
     base: '/',
     site: 'https://abebelagua.github.io',
     ```

4. **Push your code**:

   ```bash
   git add .
   git commit -m "Setup GitHub Pages deployment"
   git push
   ```

5. **Wait for deployment**:
   - Go to the **Actions** tab in your GitHub repository
   - You should see a workflow running
   - Once it completes, your site will be live!

### Automatic Deployment

Every time you push to the `main` branch, GitHub Actions will automatically:

- Build your Astro site
- Deploy it to GitHub Pages

Your site will be available at: `https://abebelagua.github.io/portfolio`

## Customization

### Personal Information

Edit `src/data/portfolio.ts` to customize:

- **Personal Info**: Update `personalInfo` object with your name, title, bio, and profile image
- **Projects**: Modify the `projects` array with your own projects
- **Social Links**: Update `socialLinks` array with your social media profiles
- **Resume**: Add your resume PDF to the `public` folder and update `resumeUrl`

### Styling

The portfolio uses Tailwind CSS. You can customize colors, fonts, and styles by:

1. Modifying Tailwind classes in components
2. Updating the gradient colors in `src/layouts/Layout.astro`
3. Adjusting component styles in individual component files

### Adding Images

- **Profile Image**: Add your profile image to `public/` folder and reference it in `portfolio.ts`
- **Project Images**: Add project images to the `public` folder and reference them in the projects array
- **Resume**: Add your resume PDF to `public/resume.pdf`

## Project Structure

```
portfolio/
├── .github/
│   └── workflows/
│       └── deploy.yml          # GitHub Actions workflow
├── public/                      # Static assets (images, resume, etc.)
├── src/
│   ├── components/             # Reusable components
│   │   ├── Contact.astro
│   │   ├── Footer.astro
│   │   ├── Hero.astro
│   │   ├── Navigation.astro
│   │   ├── Projects.astro
│   │   └── Skills.astro
│   ├── data/                    # Data files
│   │   └── portfolio.ts
│   ├── layouts/                 # Layout components
│   │   └── Layout.astro
│   ├── pages/                   # Pages
│   │   └── index.astro
│   └── styles/                  # Global styles
│       └── global.css
├── astro.config.mjs
└── package.json
```

## Technologies Used

- [Astro](https://astro.build/) - Web framework
- [Tailwind CSS](https://tailwindcss.com/) - Utility-first CSS framework
- [TypeScript](https://www.typescriptlang.org/) - Type safety
- [GitHub Pages](https://pages.github.com/) - Free hosting

## License

MIT
