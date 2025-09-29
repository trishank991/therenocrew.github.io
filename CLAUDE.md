# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview
This is a static HTML website for "The Reno Crew Ltd", a property renovation and maintenance company in Auckland, New Zealand. The site is hosted on GitHub Pages.

## File Structure
- Main homepage: `index.html`
- Service pages: `deck-repair.html`, `fencing.html`, `gibstopping.html`, `home-repairs.html`, `lawn-care.html`, `painting.html`, `renovations.html`
- Assets: `reno-crew-logo.png`, `shed-project.jpg`

## Architecture
- Static HTML website with embedded CSS and JavaScript
- Each service page has consistent navigation back to main page
- Responsive design with mobile-friendly navigation
- All pages include contact forms that alert users to email directly

## Common Development Tasks

### Adding New Service Pages
Follow the existing pattern:
1. Create new HTML file with consistent header/navigation
2. Update main navigation menu in `index.html`
3. Ensure logo and "Back to Home" link point to `index.html`

### Deployment
- GitHub Pages automatically serves `index.html` as the main page
- All navigation links are correctly configured

### Testing
- Test all navigation links locally
- Verify all asset references are correct
- Check responsive design on mobile devices

## Contact Information
- Email: therenocrewltd@gmail.com
- Phone: 027 281 9609
- Service Area: Auckland, New Zealand