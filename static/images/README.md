# How to Add Your Images

## Required Images

To complete your personal portfolio website, add the following images to the `static/images/` folder:

### 1. Profile Photo (`profile.jpg`)
- **Purpose:** Your professional headshot for About page and site branding
- **Recommended size:** 800x800 pixels (square)
- **Format:** JPG or PNG
- **Tips:** 
  - Use a professional, well-lit photo
  - Clear background or blurred
  - Friendly, approachable expression

### 2. Hero Banner (`hero-banner.jpg`)
- **Purpose:** Large banner image for homepage
- **Recommended size:** 1920x600 pixels (wide)
- **Format:** JPG or PNG
- **Ideas:**
  - Photo of you speaking/presenting
  - Lisbon cityscape
  - Abstract AI/technology themed image
  - Composite image with your photo

### 3. Podcast Banner (`podcast-banner.jpg`)
- **Purpose:** Header image for podcast page
- **Recommended size:** 1920x600 pixels (wide)
- **Format:** JPG or PNG
- **Ideas:**
  - Podcast recording setup
  - Event photos from previous episodes
  - Branded graphic with podcast name
  - Lisbon venue photo

## Where to Place Images

```
static/
  └── images/
      ├── profile.jpg          (Your headshot)
      ├── hero-banner.jpg      (Homepage banner)
      └── podcast-banner.jpg   (Podcast page banner)
```

## How to Add Images

### Method 1: Using File Explorer
1. Open File Explorer
2. Navigate to: `C:\Users\z004vw2z\projects\aicc-website\website-aicc\static\images\`
3. Copy your images into this folder
4. Rename them to match the names above

### Method 2: Using PowerShell
```powershell
# Copy your images to the images folder
Copy-Item "C:\path\to\your\photo.jpg" "static\images\profile.jpg"
Copy-Item "C:\path\to\your\banner.jpg" "static\images\hero-banner.jpg"
Copy-Item "C:\path\to\your\podcast.jpg" "static\images\podcast-banner.jpg"
```

## Free Image Resources (If You Need Placeholders)

While you prepare your own images, you can use placeholders from:

- **Unsplash:** https://unsplash.com (Free high-quality photos)
  - Search for: "professional headshot", "lisbon", "podcast", "technology"
- **Pexels:** https://pexels.com (Free stock photos)
- **Placeholder Services:**
  - `https://via.placeholder.com/800x800.png?text=Your+Photo`

## Image Optimization Tips

To keep your site fast:

1. **Compress images** before uploading:
   - Use TinyPNG.com or Squoosh.app
   - Target: Under 200KB for profile, under 500KB for banners

2. **Correct dimensions:**
   - Don't upload massive files (like 4000x4000px)
   - Resize to recommended dimensions first

3. **Use appropriate formats:**
   - JPG for photos (smaller file size)
   - PNG for images with transparency
   - WebP for best compression (Hugo can convert)

## After Adding Images

Once you've added your images:

1. Preview locally:
   ```powershell
   hugo server -D
   ```

2. Check that images appear correctly on:
   - Homepage (/)
   - About page (/about)
   - Podcast page (/podcast)

3. Commit and push:
   ```powershell
   git add static/images/
   git commit -m "Add profile and banner images"
   git push
   ```

## Additional Images

Feel free to add more images:

- **Blog post images:** `static/images/posts/post-name.jpg`
- **Guest photos:** `static/images/guests/guest-name.jpg`
- **Event photos:** `static/images/events/event-date.jpg`

Reference them in markdown as:
```markdown
![Alt text](/images/posts/your-image.jpg)
```
