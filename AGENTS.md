# JabilliCloud Kitchen - AGENTS.md

## What
Cloud kitchen ordering website for JabilliCloud Kitchen in LB Nagar, Hyderabad. Menu, ordering via WhatsApp/call, location, meal packages.

## Tech Stack
- Single-page HTML/JS/CSS (no framework, no build step)
- All in index.html (HTML + CSS + JS + menu data)
- Google Maps embed
- Vercel + GitHub Pages hosting

## Key Files
- index.html - Everything (menu data in const MENU array, 3D effects, search, tabs)
- vercel.json - Cache headers for Vercel

## Menu Data Structure
MENU is an array of objects: {cat:"Category Name", icon:"emoji", items:[{n:"Name", p:price, t:"v|nv|e", tag:"optional"}]}
- t: "v" = veg, "nv" = non-veg, "e" = egg
- IMPORTANT: Tabs use t.cat (the category name), NOT t.label

## How to Deploy
```
# GitHub Pages
git push origin main

# Vercel (both needed for both to update)
vercel --yes --prod
```

## How to Add Menu Items
Edit MENU array in index.html. Example:
```
{cat:"New Category", icon:"new_emoji", items:[
  {n:"Item Name", p:99, t:"v", tag:"New"},
]}
```

## Features
- Category tabs filter menu (uses t.cat property)
- 3D Effects toggle (bottom-right button, saves to localStorage)
- Hi-Fi 3D: mouse parallax, per-card rotations, glow shadows
- Search across all items
- WhatsApp + Call FABs
- Google Maps embed

## Known Issues
1. Vercel caching: vercel.json has no-cache headers. If changes dont appear, hard refresh (Ctrl+Shift+R).
2. 3D toggle position: Bottom-right, above FABs. If FABs overlap, adjust .toggle-3d bottom value.

## .gitignore
None needed (single HTML file, no secrets)
