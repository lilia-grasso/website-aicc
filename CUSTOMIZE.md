# Customization Checklist

Before deploying your personal portfolio and podcast site, customize these elements:

## ✅ Configuration ([hugo.toml](hugo.toml))

- [ ] Update `baseURL` with your GitHub username and repository name
- [ ] Change `title` to include your actual name
- [ ] Update `author` parameter with your name
- [ ] Add your social media links:
  - [ ] LinkedIn profile URL
  - [ ] GitHub username
  - [ ] Twitter/X handle
  - [ ] Email address

## ✅ About Page ([content/about.md](content/about.md))

Replace all bracketed placeholders with your information:

- [ ] Add your name and professional title
- [ ] Write your professional summary
- [ ] List your work experience (roles, companies, dates, achievements)
- [ ] Add your education details
- [ ] List your technical and professional skills
- [ ] Add projects and initiatives
- [ ] Include any awards or recognition
- [ ] Add publications or speaking engagements (if applicable)
- [ ] Update contact information

## ✅ Podcast Page ([content/podcast.md](content/podcast.md))

- [ ] Add details about your upcoming event(s):
  - [ ] Guest name and bio
  - [ ] Event date, time, and location
  - [ ] Topic/theme
  - [ ] Registration link
- [ ] Add past episodes (if you have them)
- [ ] Update venue information
- [ ] Add your social media links for the podcast
- [ ] Update FAQ with your specific answers
- [ ] Add newsletter signup link (if you have one)

## ✅ Homepage ([content/_index.md](content/_index.md))

- [ ] Add your name
- [ ] Write a brief intro about what you do
- [ ] Update the "What I Do" section with your specific roles
- [ ] Verify all links work

## ✅ Images ([static/images/](static/images/README.md))

- [ ] Add your profile photo as `profile.jpg`
- [ ] Add homepage banner as `hero-banner.jpg`
- [ ] Add podcast page banner as `podcast-banner.jpg`

See [static/images/README.md](static/images/README.md) for detailed image requirements.

## ✅ Before Deploying

1. **Test locally:**
   ```powershell
   hugo server -D
   ```
   Visit http://localhost:1313 and check:
   - [ ] All pages load correctly
   - [ ] Images appear (or placeholders if not added yet)
   - [ ] Navigation menu works
   - [ ] All links work (internal and external)

2. **Update git configuration** (if needed):
   ```powershell
   git config user.name "Your Name"
   git config user.email "your.email@example.com"
   ```

3. **Commit your changes:**
   ```powershell
   git add .
   git commit -m "Customize site with personal info and AI podcast details"
   git push
   ```

4. **Enable GitHub Pages:**
   - Go to your repository on GitHub
   - Settings → Pages
   - Source: **GitHub Actions**

## 📝 Optional Enhancements

After your basic site is live, consider:

- [ ] Add a blog post about your first podcast event
- [ ] Create individual pages for past podcast episodes
- [ ] Add a contact form (using services like Formspree or Netlify Forms)
- [ ] Set up a newsletter using Mailchimp or ConvertKit
- [ ] Add Google Analytics or similar for visitor tracking
- [ ] Create a custom domain (instead of github.io)
- [ ] Add more pages (Services, Projects, Blog categories, etc.)

## 🎨 Theme Customization

If you want to customize the Ananke theme further:

- Custom CSS: Create `static/css/custom.css`
- Custom layouts: Copy from `themes/ananke/layouts/` to `layouts/`
- Or explore other themes at https://themes.gohugo.io/

## 🚀 Ready to Deploy?

Once you've completed the checklist above:

1. Make sure all changes are committed
2. Push to GitHub: `git push`
3. GitHub Actions will automatically build and deploy
4. Your site will be live at `https://yourusername.github.io/repository-name/`

---

**Need help?** Check [SETUP.md](SETUP.md) for detailed instructions or [QUICKSTART.md](QUICKSTART.md) for quick reference.
