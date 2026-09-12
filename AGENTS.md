# JabilliCloud Kitchen — Memory

## Overview
- **Repo:** jabillicloudkitchen/JabilliCloudKitchen
- **Local:** `C:\Users\Imtiyaz\Documents\JabilliCloudKitchen`
- **GitHub Pages:** https://jabillicloudkitchen.github.io/JabilliCloudKitchen/
- **Vercel:** https://jabillicloudkitchen.vercel.app

## Key Features
- Menu tabs use `t.cat` (not `t.label`) — shows actual category names
- 3D Effects toggle button (bottom-right, saves to localStorage)
- Hi-Fi 3D effects:
  - Mouse parallax on hero section
  - Per-card unique rotations (alternating left/right)
  - Depth translateZ on hover
  - Glow shadows with golden accent
  - Premium toggle button with gradient styling
- Location highlight text: "We are located literally just behind Kamineni Hospital"
- WhatsApp + Call FABs

## Deploy
1. `git push origin main` (GitHub Pages auto-builds)
2. `vercel --yes --prod` (Vercel deploy)

## Vercel Caching
`vercel.json` has no-cache headers for index.html:
```json
"headers": [{"source": "/", "headers": [{"key": "Cache-Control", "value": "no-cache, no-store, must-revalidate"}]}]
```
