# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a personal academic homepage for 朱正瑞 (Zhengrui Zhu), a PhD candidate at Fudan University's School of Microelectronics. The site is a single-page static website hosted on GitHub Pages at https://zhengruizhu.github.io.

## Repository Structure

- `index.html` - Main homepage with all content (single-file application)
- `photo.png` - Profile photo displayed in the header
- `朱正瑞_复旦大学_微电子学院_直博.pdf` - CV/Resume (source document, not deployed)

## Development Workflow

### Preview Locally
Simply open `index.html` in a browser:
```bash
# Windows
start index.html

# Or use any local server
python -m http.server 8000
# Then visit http://localhost:8000
```

### Deploy to GitHub Pages
```bash
git add index.html photo.png
git commit -m "Update homepage"
git push origin main
```

Changes are live within 1-2 minutes at https://zhengruizhu.github.io.

## HTML Structure

The `index.html` file is organized into semantic sections:

1. **Header** - Profile photo, name, title, contact links (email, GitHub, Google Scholar)
2. **About Me** - Brief introduction
3. **Research Interests** - Grid layout of research areas
4. **Education** - Academic background with courses
5. **Publications** - Academic papers (currently template)
6. **Projects** - Research/development projects (currently template)
7. **Awards & Honors** - Recognition and achievements (currently template)
8. **Skills** - Technical skills as tags
9. **Contact** - Detailed contact information
10. **Footer** - Copyright and last updated

## Styling Details

### Color Scheme
- Primary gradient: `#667eea` to `#764ba2` (purple gradient in header)
- All section headings and accents use `#667eea`
- Card backgrounds: `#f8f9fa` (light gray)
- Main background: white

### Key Design Elements
- **Profile Photo**: 150px circular image with white background (uses `background-size: contain` to show full image without cropping)
- **Email Layout**: Uses flexbox to display two emails vertically with shared icon
- **Responsive**: Mobile-friendly with `@media (max-width: 768px)` breakpoint
- **Hover Effects**: Cards translate up 2px with shadow on hover

### Contact Links Alignment
The header contact section uses a custom layout:
- Email group uses `inline-flex` with `align-items: center` for vertical centering
- Two email addresses share a single 📧 icon
- All contact items (email group, GitHub, Google Scholar) are vertically centered using `vertical-align: middle`

## Content Update Guidelines

### Updating Profile Photo
The photo should have a white background to blend seamlessly with the circular container. If changing photo:
- Keep filename as `photo.png` or update line 226 in index.html
- Ensure photo has white/transparent background
- Photo will be contained within 150px circle without cropping

### Updating Personal Information
Key sections to update with CV information:
- Education: Lines 275-299 (currently has placeholder course lists with mixed HTML tags)
- Publications: Lines 302-320 (currently template only)
- Projects: Lines 322-351 (currently template only)
- Awards: Lines 353-367 (currently template only)

### Email Configuration
Header emails (lines 234-235) and Contact section emails (lines 385-386) should be kept in sync.

## Current State

The homepage has been customized with:
- Real profile photo with white background integration
- Actual personal information (name, university, emails, GitHub)
- Updated research interests and education background
- Contact information for Fudan University

Still using template content for:
- Publications section
- Projects section
- Awards section
- GitHub/Google Scholar links need actual URLs

## Technical Notes

### HTML Validation Issues
There are some unclosed `<p>` tags in the education section (lines 280-297) that should be `</li>` instead. These don't affect rendering but should be fixed for proper HTML5 compliance.

### Performance
The profile photo (photo.png) is 4.4MB which is large for web use. Consider optimizing to ~200-300KB for faster loading without visible quality loss.
