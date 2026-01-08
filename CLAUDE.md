# BetterMoney Landing Page

## Project Overview

Landing page for BetterMoney - a Bitcoin-focused wealth protection consultancy targeting high-net-worth individuals and families in Brazil. The site communicates the "Blindagem Patrimonial para o Século XXI" (Patrimonial Protection for the 21st Century) concept.

## Tech Stack

- **Static Site Generator**: Jekyll 4.3
- **Hosting**: GitHub Pages
- **Languages**: HTML, CSS, Liquid templating
- **Fonts**: Eurostile (primary/headings), IBM Plex Sans (secondary/body)

## Project Structure

```
new-page/
├── _includes/
│   ├── header.html      # Navigation with logo and menu
│   └── footer.html      # Footer with links and copyright
├── _layouts/
│   └── default.html     # Main layout with font imports
├── assets/
│   ├── css/
│   │   └── style.css    # All styles (variables, components, responsive)
│   ├── images/
│   │   ├── partners/    # Partner photos and company logos
│   │   ├── logo-*.svg   # Brand logos (horizontal, white variants)
│   │   └── *.png        # Various images including bitcoin-coin-dark.png
│   └── js/
│       └── main.js      # Mobile menu toggle
├── _config.yml          # Jekyll configuration
├── Gemfile              # Ruby dependencies
└── index.html           # Main landing page content
```

## Running Locally

```bash
cd /home/vmabellini/RiderProjects/bettermoney/new-page
bundle install
bundle exec jekyll serve
```

Site runs at `http://localhost:4000`

## Design Decisions

- **Monochromatic theme**: Black background with white/gray text, no accent colors
- **Typography**: Uppercase headings for strength, Eurostile font for modern tech feel
- **Layout inspiration**: strike.me (clean, dark, Bitcoin-focused)
- **Background image**: Bitcoin coin in hero section, grayscale, 35% opacity, constrained to container

## Page Sections

1. **Hero**: Main value proposition with CTA buttons and trust indicators
2. **Problem**: Three pain points (inflation, surveillance, confisco)
3. **Pillars**: Three pillars of individual sovereignty (psychological, financial, physical)
4. **Services**: Service cards with pricing
5. **Stats**: Key metrics
6. **About**: Founder bio (Bernardo Braga) and team
7. **Partners**: Individual specialists and partner companies
8. **Image**: Full-width Bitcoin image section
9. **FAQ**: Common questions
10. **CTA**: Final call-to-action with contact form placeholder

## Key CSS Classes

- `.container` - Max-width 1200px centered container
- `.section` - Standard section padding
- `.section--gray` - Dark gray background variant
- `.btn--primary` / `.btn--secondary` - Button styles
- `.hero__bg-image` - Positioned Bitcoin background in hero

## Content Source

All content extracted from PDF: `BLINDAGEM-PATRIMONIAL-PARA-O-SECULO-XXI.pdf`
Partner images extracted from PDF page 8 using `pdfimages`

## Publishing to GitHub Pages

1. Create GitHub repository
2. Push code to main branch
3. Enable GitHub Pages in Settings > Pages > Source: GitHub Actions
4. Site deploys automatically on push

## Notes

- Ruby 4.0 requires explicit gems: logger, csv, base64, bigdecimal (added to Gemfile)
- Eurostile font uses local() references - ensure font is installed or add web font files
- All text in Portuguese (pt-BR)
