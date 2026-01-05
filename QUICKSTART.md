# Quick Reference

## Your Hugo site is ready! 

### Site Structure Created:
- ✅ Hugo configuration ([hugo.toml](hugo.toml))
- ✅ Ananke theme installed (themes/ananke)
- ✅ Content directories (content, static, layouts, etc.)
- ✅ Sample homepage ([content/_index.md](content/_index.md))
- ✅ First blog post ([content/posts/first-post.md](content/posts/first-post.md))
- ✅ GitHub Actions workflow ([.github/workflows/hugo.yml](.github/workflows/hugo.yml))

### Before deploying, update hugo.toml:

Replace these placeholder values:
```toml
baseURL = 'https://USERNAME.github.io/REPOSITORY/'
```

With your actual GitHub info, for example:
```toml
baseURL = 'https://yourusername.github.io/website-aicc/'
```

### Test Locally:

Since Hugo is installed but may not be in this terminal's PATH, you have two options:

**Option 1: Open a new terminal**
```powershell
hugo server -D
```
Then visit: http://localhost:1313

**Option 2: Use the full path or reload PATH**
Close and reopen VS Code, or run:
```powershell
refreshenv  # If using Chocolatey
# OR
$env:Path = [System.Environment]::GetEnvironmentVariable("Path","Machine") + ";" + [System.Environment]::GetEnvironmentVariable("Path","User")
hugo server -D
```

### Deploy to GitHub Pages:

1. Update `baseURL` in [hugo.toml](hugo.toml)
2. Commit your changes:
   ```powershell
   git add .
   git commit -m "Set up Hugo site"
   git push
   ```
3. Enable GitHub Pages in your repository:
   - Go to Settings → Pages
   - Source: **GitHub Actions**

The site will automatically build and deploy!

### Creating New Content:

```powershell
# New blog post
hugo new posts/my-new-post.md

# New page
hugo new about.md
```

### File Locations:
- **Blog posts**: `content/posts/`
- **Pages**: `content/`
- **Images**: `static/images/`
- **Configuration**: `hugo.toml`
