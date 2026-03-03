# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

This is a static HTML presentation for LUMIA, a premium media platform proposal for influencers. The presentation is a single-page slideshow with 13 slides targeting Korean-speaking audiences.

## Architecture

**Single-file structure**: The entire presentation lives in `index.html` containing:
- CSS design system with CSS custom properties (`:root` variables)
- 13 slide sections with unique IDs (`#slide-1` through `#slide-13`)
- JavaScript navigation system (keyboard, touch, click)
- Responsive scaling using CSS transforms (base: 1280x720px)

**Design System**:
- Brand color: `oklch(51.4% .228 250)` defined as `--accent`
- Typography: Noto Sans KR (Google Fonts)
- Icons: Font Awesome 6.4.0

**Key CSS patterns**:
- `.slide` - Base slide container with transition animations
- `.slide.active` - Currently visible slide
- Animation keyframes: `fadeInUp`, `fadeInLeft`, `fadeInRight`, `scaleIn`, `bounceIn`
- Phone mockup UI system: `--pm-*` CSS variables for in-slide phone preview

**Navigation**:
- Arrow keys, Space, touch swipe, click navigation
- Progress bar, page dots, page number display
- Viewport scaling via `scalePresentation()` function

## Development

Open `index.html` directly in a browser - no build step required. The presentation auto-scales to fit any viewport while maintaining 16:9 aspect ratio.

## Assets

- `main.png` - OG image for social sharing
- `photo_2026-02-28 19.53.13.jpeg` - Curator post example image (slide 9)
- `index_web.html` - Alternative version of the presentation
