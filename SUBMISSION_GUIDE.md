# Browser Extension Submission Guide

## Creating the Extension Package

### Required Files (already copied to /sip-extension-build/)
- `manifest.json` (version 1.1.0)
- `index.html`
- `script.js`
- `style.css`
- `icons/` folder (with icon16.png, icon32.png, icon48.png, icon128.png)
- `fonts/` folder
- `assets/` folder (if exists)

### Excluded from package:
- `.git` folder
- `README.md` and other documentation
- `screenshots/` folder (use separately for store listing)
- Development files

## Creating the ZIP file

**On Linux/Mac:**
```bash
cd /home/bryan/sip-extension-build
zip -r ../sip-v1.1.0.zip *
```

**On Windows:**
```bash
# Right-click the sip-extension-build folder
# Select "Compress to ZIP file" or use 7-Zip
```

**Verify the ZIP contains:**
- manifest.json in the root
- All HTML, CSS, JS files
- icons/ folder with all icon sizes
- fonts/ and assets/ folders

---

## Firefox Add-ons Submission

### 1. Prepare Materials
- [ ] Extension ZIP file (`sip-v1.1.0.zip`)
- [ ] Screenshots from `/screenshots/` folder (select 3-5 best ones)
- [ ] Release notes from `RELEASE_NOTES_v1.1.0.md`

### 2. Login & Upload
1. Go to https://addons.mozilla.org/developers/
2. Login with your Firefox account
3. Find your "Sip" extension in "My Add-ons"
4. Click "New Version"
5. Upload `sip-v1.1.0.zip`

### 3. Version Details
**Version Number:** 1.1.0

**Release Notes:**
```
Major feature update with 9 color schemes, social links integration, and enhanced customization.

New Features:
• 8 new color schemes (Nord, Gruvbox, Tokyo Night, Dracula, Solarized, Kanagawa, Ayu, Monochrome)
• Social links integration with 10 platforms
• Customizable footer layout (left/center/right sections)
• Click-to-toggle time format
• Show seconds option for clock
• Link behavior control (same window/new tab/new window)
• Keyboard shortcuts visibility toggle
• Help documentation integrated into settings

UI Improvements:
• Color scheme dropdown selector
• Better responsive design
• Enhanced settings organization (6 tabs)
• Developer credits section

All existing settings and customizations preserved on update.
```

### 4. Review Process
- **Automated validation**: Immediate (checks manifest, file structure)
- **Human review**: 1-3 days typically
- **Status updates**: Check email and AMO dashboard

---

## Chrome Web Store Submission

### 1. Prepare Materials
- [ ] Extension ZIP file (`sip-v1.1.0.zip`)
- [ ] Store listing images (1280x800 screenshots)
- [ ] Small promotional tile: 440x280 (optional)
- [ ] Large promotional tile: 920x680 (optional)
- [ ] Marquee promotional tile: 1400x560 (optional)

### 2. Login & Upload
1. Go to https://chrome.google.com/webstore/devconsole
2. Login with your Google account
3. Find "Sip" extension
4. Click on the extension name
5. Click "Package" tab
6. Click "Upload New Package"
7. Upload `sip-v1.1.0.zip`

### 3. Store Listing Updates

**Detailed Description:**
```
Transform your browser's new tab into a beautiful, personalized workspace with Sip. 

🎨 9 BEAUTIFUL COLOR SCHEMES
Choose from Catppuccin, Nord, Gruvbox, Tokyo Night, Dracula, Solarized, Kanagawa, Ayu, or Monochrome - each with both light and dark modes (18 total combinations).

✨ KEY FEATURES
• 9 stunning color schemes with light & dark modes
• Modern glassmorphism UI with ambient glow effects
• Quick links organized in customizable categories (up to 8 categories, 10 links each)
• Real-time weather with OpenWeather API integration
• Social links integration for 10 popular platforms
• Customizable footer layout (Weather, Social Links, Quotes, or Blank)
• Smart search with 9 search engine options
• Click clock to toggle between 12h/24h format
• Optional seconds display
• Control link opening behavior (same window/new tab/new window)
• Keyboard shortcuts with toggle visibility
• All settings persist locally - no data collection

🔒 PRIVACY FIRST
No data collection or tracking. All preferences stored locally on your device.

🎯 PERFECT FOR
• Developers needing quick access to tools
• Anyone who values beautiful, functional design
• Users wanting a personalized browsing experience
• Privacy-conscious individuals

⌨️ KEYBOARD SHORTCUTS
• / - Focus search
• 1-9 - Switch search engine
• Esc - Clear search

New in v1.1.0: Major feature update with 8 new color schemes, social links, footer customization, and enhanced settings.
```

**Short Description (132 chars max):**
```
A cozy new tab page with 9 beautiful color schemes, social links, customizable footer, and extensive personalization options.
```

### 4. Upload Screenshots
Upload 3-5 screenshots from `/screenshots/themes/` showing different color schemes in both light and dark modes.

Recommended screenshots:
1. Catppuccin Dark (default)
2. Nord Light
3. Tokyo Night Dark
4. Settings panel
5. Gruvbox Light

### 5. Category & Language
- **Category**: Productivity
- **Language**: English

### 6. Privacy Practices
- **Single Purpose**: New Tab replacement
- **Permission Justification**: "search" permission used to integrate with browser's default search engine
- **Data Usage**: No user data collected or transmitted
- **Host Permissions**: None required

### 7. Submit for Review
- Click "Submit for Review"
- Review typically takes 1-3 business days
- Check email for status updates

---

## Post-Submission

### Monitor Reviews
- Check both Firefox AMO and Chrome Web Store dashboards daily
- Respond to any reviewer questions within 24 hours

### Update Documentation
Once approved:
- [ ] Update README.md with store links
- [ ] Announce on GitHub releases
- [ ] Update any external documentation

### GitHub Release
```bash
cd /home/bryan/Sip-StartPage
git tag v1.1.0
git push origin v1.1.0
```

Then create a GitHub release:
1. Go to https://github.com/bgibson72/Sip-StartPage/releases
2. Click "Create a new release"
3. Tag: v1.1.0
4. Title: "Sip v1.1.0 - Major Feature Update"
5. Copy content from RELEASE_NOTES_v1.1.0.md
6. Attach `sip-v1.1.0.zip` as release asset

---

## Quick Checklist

**Before Submission:**
- [x] Version updated in manifest.json (1.1.0)
- [x] Description updated in manifest.json
- [x] All code tested in both Firefox and Chrome
- [x] Screenshots organized and ready
- [x] Release notes prepared
- [ ] Extension ZIP created
- [ ] All permissions justified

**Firefox AMO:**
- [ ] ZIP uploaded
- [ ] Release notes added
- [ ] Version submitted

**Chrome Web Store:**
- [ ] ZIP uploaded
- [ ] Store listing updated
- [ ] Screenshots uploaded
- [ ] Privacy practices documented
- [ ] Version submitted

**After Approval:**
- [ ] Git tag created (v1.1.0)
- [ ] GitHub release published
- [ ] README updated with store links
- [ ] Social media announcement (optional)

---

Good luck with the submission! Both stores typically approve within 1-3 business days for updates to existing extensions.
