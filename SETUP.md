# Hugo + GitHub Pages Setup Guide

## Prerequisites

### 1. Install Hugo

**Using Scoop (Recommended for Windows):**
```powershell
# Install Scoop
Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope CurrentUser
Invoke-RestMethod -Uri https://get.scoop.sh | Invoke-Expression

# Install Hugo Extended
scoop install hugo-extended
```

**Verify Installation:**
```powershell
hugo version
```

## Initial Setup

### 2. Initialize Hugo Site

Run these commands in the project root:

```powershell
# Create a new Hugo site (this will populate the directory with Hugo structure)
hugo new site . --force

# Add a theme (using Ananke as example)
git submodule add https://github.com/theNewDynamic/gohugo-theme-ananke.git themes/ananke

# Create your first post
hugo new posts/my-first-post.md
```

### 3. Configure for GitHub Pages

1. **Update `hugo.toml`:**
   - Replace `USERNAME` with your GitHub username
   - Replace `REPOSITORY` with your repository name
   - Example: `baseURL = 'https://myusername.github.io/website-aicc/'`

2. **Test locally:**
   ```powershell
   hugo server -D
   ```
   Visit http://localhost:1313 to preview your site

### 4. GitHub Repository Setup

1. **Create a GitHub repository** (if not already done):
   - Go to https://github.com/new
   - Name it (e.g., `website-aicc`)
   - Don't initialize with README (you already have one)

2. **Push your code:**
   ```powershell
   git add .
   git commit -m "Initial Hugo site setup"
   git branch -M main
   git remote add origin https://github.com/USERNAME/REPOSITORY.git
   git push -u origin main
   ```

### 5. Enable GitHub Pages

1. Go to your repository on GitHub
2. Click **Settings** → **Pages**
3. Under "Build and deployment":
   - Source: **GitHub Actions**
4. The workflow will automatically deploy on push to main branch

## Creating Content

### Create a new post:
```powershell
hugo new posts/my-post-name.md
```

### Create a new page:
```powershell
hugo new about.md
```

## Local Development

```powershell
# Run dev server with draft content
hugo server -D

# Build for production
hugo --minify
```

## File Structure

```
website-aicc/
├── .github/
│   └── workflows/
│       └── hugo.yml          # GitHub Actions workflow
├── archetypes/               # Content templates
├── content/                  # Your content (markdown files)
├── data/                     # Data files
├── layouts/                  # Custom layouts (optional)
├── static/                   # Static files (images, css, js)
├── themes/                   # Hugo themes
├── hugo.toml                 # Main configuration
└── public/                   # Generated site (ignored by git)
```

## Popular Hugo Themes

- **Ananke** (default): https://github.com/theNewDynamic/gohugo-theme-ananke
- **PaperMod**: https://github.com/adityatelange/hugo-PaperMod
- **Stack**: https://github.com/CaiJimmy/hugo-theme-stack
- **Coder**: https://github.com/luizdepra/hugo-coder

To change themes:
```powershell
git submodule add THEME_GIT_URL themes/THEME_NAME
```
Then update `theme` in `hugo.toml`

## Troubleshooting

- **Site not updating?** Check the Actions tab in GitHub for build errors
- **404 errors?** Verify `baseURL` in `hugo.toml` matches your GitHub Pages URL
- **Theme not showing?** Make sure the theme is added as a git submodule

## Resources

- Hugo Documentation: https://gohugo.io/documentation/
- GitHub Pages: https://docs.github.com/en/pages
- Hugo Themes: https://themes.gohugo.io/
