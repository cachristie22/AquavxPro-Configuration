# 📋 Media Types Quick Reference

## All Supported Media in One Place

Your website now supports **images, videos, and YouTube embeds** - all using the same `images` array!

## Quick Examples

### 1. Regular Image (PNG, JPG, GIF)
```json
"images": [
  {
    "id": "diagram_1",
    "url": "images/wiring-diagram.png",
    "alt": "Wiring Diagram"
  }
]
```
**Result:** Image with rounded corners and shadow

---

### 2. Self-Hosted Video (MP4, MOV, WebM)
```json
"images": [
  {
    "id": "demo_video",
    "url": "videos/installation-demo.mp4",
    "alt": "Installation Demo"
  }
]
```
**Result:** Video player with play/pause, volume, fullscreen controls

---

### 3. YouTube Video
```json
"images": [
  {
    "id": "youtube_tutorial",
    "url": "https://www.youtube.com/watch?v=dQw4w9WgXcQ",
    "alt": "Tutorial Video"
  }
]
```
**Result:** Embedded YouTube player + "Open in YouTube" link

---

## Mix & Match Example

```json
{
  "title": "Installation Guide",
  "content": [
    "Follow the steps below to install your Aquavx Pro system."
  ],
  "images": [
    {
      "id": "product_photo",
      "url": "images/aquavx-pro.jpg",
      "alt": "Aquavx Pro Unit"
    },
    {
      "id": "tutorial_video",
      "url": "https://www.youtube.com/watch?v=VIDEO_ID",
      "alt": "Installation Video Tutorial"
    },
    {
      "id": "wiring_diagram",
      "url": "images/wiring-diagram.png",
      "alt": "Wiring Diagram"
    },
    {
      "id": "closeup_demo",
      "url": "videos/wiring-closeup.mp4",
      "alt": "Wiring Close-up Demonstration"
    }
  ]
}
```

**Result:** Shows all 4 items in order - photo, YouTube embed, diagram, video

---

## Auto-Detection Rules

The website automatically detects what to render based on the URL:

| URL Contains | Renders As |
|--------------|------------|
| `youtube.com` or `youtu.be` | YouTube embed with player |
| `.mp4`, `.mov`, `.webm`, etc. | HTML5 video player |
| `.png`, `.jpg`, `.gif`, etc. | Image |

**No special configuration needed - just paste the URL!**

---

## File Organization

```
your-website/
├── index.html
├── app.js
├── content_updated.json
├── images/
│   ├── aquavx-pro.jpg
│   ├── wiring-diagram.png
│   └── installation-photo.png
└── videos/
    ├── demo.mp4
    └── tutorial.mp4
```

**YouTube videos don't need local files - just paste the URL!**

---

## Supported Formats

### Images:
✅ PNG, JPG, JPEG, GIF, WebP, SVG

### Self-Hosted Videos:
✅ **MP4** (recommended - works everywhere)  
✅ WebM (good for web)  
✅ OGG (open source)  
⚠️ MOV (Safari/iOS only)  
⚠️ AVI, MKV (limited support)

### YouTube:
✅ Any public or unlisted YouTube video  
✅ Works with all YouTube URL formats

---

## Features Comparison

| Media Type | Playback | Bandwidth | Best For |
|-----------|----------|-----------|----------|
| **Images** | Instant | Minimal | Diagrams, photos, screenshots |
| **Self-hosted Video** | Player controls | Your server | Short clips, private content |
| **YouTube** | Full player | YouTube's servers | Long videos, public tutorials |

---

## Quick Tips

### Images:
- Keep under 500KB for fast loading
- Use PNG for diagrams, JPG for photos
- Add descriptive alt text for accessibility

### Self-Hosted Videos:
- Keep under 50MB
- Use MP4 format (H.264 codec)
- 720p resolution is good balance

### YouTube:
- No file size limit!
- Great for long tutorials
- Users can "Open in YouTube" for full features

---

## Common Patterns

### Before/After Comparison:
```json
"images": [
  {"id": "before", "url": "images/before.jpg", "alt": "Before Installation"},
  {"id": "after", "url": "images/after.jpg", "alt": "After Installation"}
]
```

### Tutorial with References:
```json
"images": [
  {"id": "video", "url": "https://youtu.be/VIDEO_ID", "alt": "Video Tutorial"},
  {"id": "ref1", "url": "images/reference-1.png", "alt": "Reference Diagram 1"},
  {"id": "ref2", "url": "images/reference-2.png", "alt": "Reference Diagram 2"}
]
```

### Step-by-Step with Videos:
```json
"subsections": [
  {
    "title": "Step 1: Preparation",
    "content": ["Gather your materials:"],
    "images": [{"id": "s1", "url": "images/materials.jpg", "alt": "Required Materials"}]
  },
  {
    "title": "Step 2: Installation",
    "content": ["Watch the installation process:"],
    "images": [{"id": "s2", "url": "videos/install.mp4", "alt": "Installation Demo"}]
  },
  {
    "title": "Step 3: Testing",
    "content": ["Test your setup:"],
    "images": [{"id": "s3", "url": "https://youtu.be/VIDEO", "alt": "Testing Tutorial"}]
  }
]
```

---

## Files Updated

✅ **app.js** - Auto-detects images, videos, and YouTube URLs  
✅ **index.html** - Styling for all media types  

## Guides Available

📖 [VIDEO_SUPPORT.md](computer:///mnt/user-data/outputs/VIDEO_SUPPORT.md) - Self-hosted videos  
📖 [YOUTUBE_GUIDE.md](computer:///mnt/user-data/outputs/YOUTUBE_GUIDE.md) - YouTube embeds  
📖 [IMAGE_GUIDE.md](computer:///mnt/user-data/outputs/IMAGE_GUIDE.md) - Images  

---

**🎯 Bottom Line:** Just add the URL to the `images` array - the website figures out what it is and renders it correctly!
