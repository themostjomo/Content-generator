# 🎨 Universal Brand Content Generator

**Turn any project's visual identity into ready-to-post social media assets — right in your browser, zero install, zero backend.**

Pick a theme (or build your own from scratch), fill in a headline, and export a polished PNG, JPEG, or animated GIF sized for X/Twitter — in landscape, square, or portrait. No design software, no Figma, no template marketplace. One HTML file, opened in any browser.

<p align="center">
  <img alt="static badge" src="https://img.shields.io/badge/type-single--file%20HTML-black?style=flat-square">
  <img alt="static badge" src="https://img.shields.io/badge/dependencies-none%20to%20install-black?style=flat-square">
  <img alt="static badge" src="https://img.shields.io/badge/backend-none-black?style=flat-square">
  <img alt="static badge" src="https://img.shields.io/badge/license-MIT-black?style=flat-square">
</p>

---

## Why this exists

Every project ends up needing the same thing eventually: a consistent set of branded images for announcements, tips, milestones, quotes, and reminders — the kind of content that goes out on X/Twitter every week. Hiring a designer for every post doesn't scale, and generic Canva templates don't match your actual brand.

This tool solves that with a **theme engine** instead of a fixed template. Define your colors, borders, shadows, corners, and fonts once — as a built-in preset or fully custom — and every post you generate after that matches your brand automatically.

## ✨ Features

- **🎨 Full theme system** — background, surface, text, muted text, accent, and border colors, each with a color picker *and* a hex input for exact values
- **4 built-in style presets** to start from:
  | Preset | Vibe |
  |---|---|
  | **Neo-brutalist** | Hard offset shadows, sharp corners, monospace labels — bold and technical |
  | **Soft minimal** | Rounded corners, blurred soft shadow, clean sans-serif — calm and modern |
  | **Dark mode** | Dark background, neon accent, dotted texture |
  | **Editorial** | Serif headline, warm paper tones, restrained |
- **Independent style controls** — border weight, corner radius, shadow style, background pattern (grid / dots / none), and font pairing, so you're never stuck with a preset as-is
- **💾 Save & reuse your theme** — export the current theme as JSON with one click, paste it back in on your next project to get pixel-identical branding instantly
- **📐 Three export formats** — Landscape (1200×675), Square (1080×1080), Portrait (1080×1350)
- **🖼️ Avatar support** — upload a profile photo, rendered as a clipped circle with a pulsing accent-colored glow ring near the footer
- **✨ Animated shimmer sweep** — a diagonal light-gloss animation across the card, with an **intensity toggle** (Off / Subtle / Bold) so it fits brands that want flash and brands that don't
- **5 content templates** — Announcement, Tip/Alpha, Milestone/Stat, Quote/Testimonial, Reminder/Warning — each fully editable, with `**word**` syntax to highlight any word in your accent color
- **Exports PNG, JPEG, and animated GIF** — GIF encoding happens entirely client-side, no server round-trip
- **Mobile-ready**, including handling for iOS Safari's quirky download behavior (long-press-to-save flow built in automatically)

## 🚀 Quick start

### Desktop
Download `content-generator.html` and open it in any modern browser. That's it — no build step, no `npm install`.

### iPhone / mobile
iOS Safari needs the file hosted as a real URL rather than opened locally. See **[README-iphone.md](README-iphone.md)** for the exact steps (short version: host it via [htmlpreview.github.io](https://htmlpreview.github.io) pointed at this repo's raw file, open that link in Safari).

## 🖌️ Using the theme system

1. Pick a **Theme preset** to start, or leave it on any preset and start tweaking — the moment you touch a color, border, shadow, or font control, it switches to **Custom** automatically
2. Type or paste exact **hex codes** for any color, or use the swatch picker — they stay in sync
3. Once you're happy with a look, expand **"Save / load this theme as JSON"** and hit **Copy current theme** — paste that JSON somewhere safe
4. On your next project (or next session), paste it back into the same box and hit **Apply pasted theme** — instant, exact match

## 📝 Content fields

| Field | Notes |
|---|---|
| Post type | Loads starter copy for one of 5 templates — fully editable after |
| Tag chip | Short label (4–6 characters) in the corner of the card |
| Eyebrow | Small uppercase line above the headline |
| Headline | Wrap any word in `**word**` to render it in your accent color |
| Stat number / label | Shown only for the Milestone template |
| Body | Supporting line under the headline |
| Footer | Your handle / site, e.g. `@yourhandle · yoursite.com` |
| Avatar | Optional profile photo, shown as a pulsing circular badge |

## 🛠️ Built with

Vanilla HTML, CSS, and JavaScript — no framework, no bundler. GIF encoding via [gif.js](https://github.com/jnordberg/gif.js), loaded from cdnjs at runtime.

## 📄 License

MIT — use it, fork it, brand it, ship it.
