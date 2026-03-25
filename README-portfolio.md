# Outreachy 2026 Portfolio - Ibrahim Jamiu

Professional portfolio website showcasing contributions to the Fedora Project during Outreachy May 2026 application phase.

**Live Site:** `https://yourusername.github.io/outreachy-2026-portfolio`

---

## 🚀 Setup Instructions

### Step 1: Create GitHub Repository

1. Go to GitHub and create a new repository
2. Name it: `outreachy-2026-portfolio`
3. Make it **Public**
4. Do NOT initialize with README (we have our own files)
5. Create repository

### Step 2: Upload Your Files

**Required files:**
- `index.html` - The portfolio website
- `styles.css` - Styling
- `profile.jpg` - Your profile picture (150x150px recommended)

**Upload methods:**

**Option A: Web Interface (Easiest)**
1. Click "uploading an existing file"
2. Drag all 3 files (index.html, styles.css, profile.jpg)
3. Commit: "Initial portfolio setup"

**Option B: Git Command Line**
```bash
git clone https://github.com/yourusername/outreachy-2026-portfolio.git
cd outreachy-2026-portfolio

# Add your files
cp /path/to/index.html .
cp /path/to/styles.css .
cp /path/to/profile.jpg .

git add .
git commit -m "Initial portfolio setup"
git push origin main
```

### Step 3: Enable GitHub Pages

1. Go to repository **Settings**
2. Scroll to **Pages** section (left sidebar)
3. Under "Source", select **main branch**
4. Click **Save**
5. Wait 1-2 minutes
6. Your site will be live at: `https://yourusername.github.io/outreachy-2026-portfolio`

---

## ✏️ How to Update Your Portfolio

### Updating Existing Contributions

**To update contribution links:**

1. Open `index.html`
2. Find the contribution card you want to update
3. Replace `#issuecomment-XXXXX` with your actual comment number

**Example:**
```html
<!-- BEFORE -->
<a href="https://github.com/fedora-infra/fedora-interns/issues/116#issuecomment-XXXXX">

<!-- AFTER -->
<a href="https://github.com/fedora-infra/fedora-interns/issues/116#issuecomment-123456">
```

**To update your profile links:**

Find this section in `index.html`:
```html
<a href="https://github.com/yourusername" class="contact-link" target="_blank">
```

Replace `yourusername` with your actual GitHub username.

Do the same for:
- Email (already correct: woyin365@gmail.com)
- GitHub link
- Matrix link (already correct)
- Dev.to blog link

### Adding New Contributions

**Step 1: Update the Stats**

Find this in `index.html`:
```html
<div class="stat-card">
    <div class="stat-number">6</div>
    <div class="stat-label">Contributions</div>
</div>
```

Change the number from 6 to 7 (or however many total contributions you have).

**Step 2: Remove the Placeholder Card**

Find and delete this entire block:
```html
<div class="contribution-card placeholder">
    <div class="placeholder-content">
        <svg>...</svg>
        <h3>More Contributions Coming</h3>
        <p>Additional project contributions...</p>
    </div>
</div>
```

**Step 3: Add Your New Contribution**

Copy this template and add it BEFORE the closing `</div>` of the contributions-grid:

```html
<div class="contribution-card">
    <div class="contribution-header">
        <div class="contribution-number">07</div>
        <div class="contribution-status completed">Completed</div>
    </div>
    <h3 class="contribution-title">YOUR CONTRIBUTION TITLE</h3>
    <p class="contribution-description">
        Brief description of what you did and why it matters.
    </p>
    <div class="contribution-meta">
        <span class="meta-tag">TYPE (e.g., Code, Documentation)</span>
        <span class="meta-date">DATE</span>
    </div>
    <div class="contribution-links">
        <a href="GITHUB_ISSUE_URL" target="_blank">
            <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                <path d="M21 15a2 2 0 0 1-2 2H7l-4 4V5a2 2 0 0 1 2-2h14a2 2 0 0 1 2 2z"></path>
            </svg>
            View Issue
        </a>
        <a href="YOUR_WORK_URL" target="_blank">
            <svg width="16" height="16" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2">
                <path d="M18 13v6a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2V8a2 2 0 0 1 2-2h6"></path>
                <polyline points="15 3 21 3 21 9"></polyline>
                <line x1="10" y1="14" x2="21" y2="3"></line>
            </svg>
            View Work
        </a>
    </div>
</div>
```

**Customize:**
- Change `07` to your actual contribution number
- Replace `YOUR CONTRIBUTION TITLE` with the actual title
- Replace the description
- Update the type tag and date
- Add your URLs

### Updating Your Highlighted Contribution

If you want to change which contribution is highlighted:

1. Find the "Highlighted Contribution" section
2. Update the title, description, and links

```html
<h3 class="highlight-title">YOUR NEW HIGHLIGHT TITLE</h3>
<p class="highlight-description">
    Why this contribution is significant...
</p>
```

---

## 📸 Profile Picture Guidelines

**Recommended specs:**
- **Size:** 150x150 pixels (or larger, it will be resized)
- **Format:** JPG, PNG, or WebP
- **File name:** `profile.jpg` (or update the HTML to match your filename)
- **Style:** Professional headshot or avatar

**To update your profile picture:**
1. Save your image as `profile.jpg`
2. Upload it to the repository (replace the old one)
3. The site will automatically update

**Alternative:** If you want a different filename:
- Upload your image (e.g., `my-photo.png`)
- In `index.html`, find: `<img src="profile.jpg"`
- Change to: `<img src="my-photo.png"`

---

## 🎨 Customization Options

### Changing Colors

Edit `styles.css` and modify the color variables:

```css
:root {
    --primary: #51A2DA;        /* Main blue color */
    --primary-dark: #294172;   /* Darker blue */
    --success: #10b981;        /* Green for completed */
}
```

### Adding More Skills

Find the Skills Section in `index.html` and add more skill tags:

```html
<span class="skill-tag">New Skill</span>
```

### Hiding Sections

To hide a section (like the placeholder), add `style="display: none;"`:

```html
<div class="contribution-card placeholder" style="display: none;">
```

---

## 🔄 Publishing Updates

After making changes to `index.html` or `styles.css`:

**Method 1: GitHub Web Interface**
1. Go to the file on GitHub
2. Click the pencil icon (Edit)
3. Make your changes
4. Scroll down and click "Commit changes"
5. Wait 1-2 minutes, refresh your portfolio site

**Method 2: Git Command Line**
```bash
# Make your edits locally
git add index.html styles.css
git commit -m "Update contributions"
git push origin main
```

GitHub Pages automatically rebuilds your site within 1-2 minutes.

---

## ✅ Submission Checklist

Before submitting to GitHub Issue #121:

- [ ] Profile picture uploaded and displays correctly
- [ ] All placeholder URLs replaced with actual links
- [ ] GitHub username updated everywhere
- [ ] All 6 contributions have correct comment links
- [ ] Stats numbers are accurate
- [ ] Contact links work
- [ ] Site deployed and accessible at your GitHub Pages URL
- [ ] Site looks good on mobile (test by resizing browser)

---

## 📝 Comment for GitHub Issue #121

Once your portfolio is live, post this comment:

```
Hi @jflory7,

I've created my Outreachy contributions portfolio!

🌐 **Live Portfolio:** https://yourusername.github.io/outreachy-2026-portfolio

**What I've built:**
- Professional single-page portfolio website
- Hosted on GitHub Pages (free, permanent)
- Showcases all 6 contributions with direct links
- Highlighted contribution section
- Skills demonstration
- Responsive design (works on mobile)
- Clean, professional presentation

**Features:**
- Direct links to all GitHub issues and comments
- Links to blog posts and external resources
- Organized by pre-requisites vs project contributions
- Stats dashboard showing contribution count
- Professional profile section with contact links

**Technology:**
- HTML5 + CSS3
- GitHub Pages hosting
- Responsive design
- Clean, accessible layout

This portfolio will serve as a living document throughout the application period. I'll continue updating it as I make additional contributions.

The source code is available in the repository for review.

Looking forward to your feedback!

Ibrahim
```

---

## 🆘 Troubleshooting

**Site not loading?**
- Check that GitHub Pages is enabled in Settings → Pages
- Verify the branch is set to "main"
- Wait 2-3 minutes after enabling
- Try accessing in incognito/private window

**Profile picture not showing?**
- Verify the filename matches exactly (case-sensitive!)
- Make sure it's in the root directory (same level as index.html)
- Try clearing browser cache
- Check the image file isn't corrupted

**Links not working?**
- Make sure URLs are complete (include https://)
- Check for typos in comment numbers
- Verify links in incognito window

**Styling looks broken?**
- Verify `styles.css` is uploaded
- Check the file is named exactly `styles.css` (not `style.css`)
- Clear browser cache
- Check browser console for errors (F12)

---

## 📂 File Structure

```
outreachy-2026-portfolio/
├── index.html          # Main portfolio page
├── styles.css          # Styling
├── profile.jpg         # Your photo
└── README.md           # This file (optional to upload)
```

---

## 🎯 Best Practices

1. **Update immediately after each contribution** - Don't wait until the deadline
2. **Keep descriptions concise** - 2-3 sentences max per contribution
3. **Link to actual work** - GitHub issues, blog posts, repositories
4. **Proofread** - Check for typos before committing
5. **Test on mobile** - Resize browser to check responsiveness
6. **Back up your changes** - Keep local copies of edited files

---

## 📌 Quick Reference

**Your Portfolio URL:** `https://yourusername.github.io/outreachy-2026-portfolio`  
**GitHub Repo:** `https://github.com/yourusername/outreachy-2026-portfolio`  
**GitHub Issue to Submit:** [#121](https://github.com/fedora-infra/fedora-interns/issues/121)

---

**Created:** March 25, 2026  
**Author:** Ibrahim Jamiu  
**Purpose:** Outreachy May 2026 Portfolio Submission
