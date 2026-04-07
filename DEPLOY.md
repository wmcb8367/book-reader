# Squarespace Deployment Instructions

## Quick Start (5 minutes)

### 1. Upload Audio Files
1. In Squarespace, go to **Settings → Files**
2. Upload all 4 audio files from `audiobook/` folder:
   - 01-preface.mp3
   - 02-prologue-part-1.mp3
   - 02-prologue-part-2.mp3
   - 02-prologue-part-3.mp3
3. Copy the URL for each file (right-click → Copy Link)

### 2. Upload Book Content
1. Go to **Settings → Files**
2. Upload `RCDM-v2.1.md`
3. Copy the URL

### 3. Create the Page
1. Go to **Pages → +** (Add Page)
2. Choose **Blank Page**
3. Name it: "Race Course Decision Making - Reader"
4. Add a **Code Block**
5. Paste the entire contents of `index.html`

### 4. Update Audio URLs
In the code block, find this section (around line 180):
```javascript
const audioFiles = {
    'preface': 'https://YOUR-SITE.squarespace.com/s/01-preface.mp3',
    // etc...
};
```

Replace `YOUR-SITE.squarespace.com/s/` with the actual URLs you copied in step 1.

### 5. Update Book URL
Find this line (around line 270):
```javascript
fetch('RCDM-v2.1.md')
```

Replace with the URL you copied in step 2.

### 6. Save & Publish
1. Click **Save**
2. Click **Publish** (top right)
3. Visit your new page!

## For Ollama Integration (Later)

The AI chat currently tries to connect to `localhost:11434`. To make this work from the web:

1. Set up Cloudflare Tunnel (I can help with this)
2. Replace `localhost:11434` with your tunnel URL
3. Update CORS settings

For now, the page works beautifully with:
- ✅ Full book text
- ✅ Audio player with chapters
- ❌ AI chat (needs Ollama tunnel setup)

Want me to walk you through it on the screen sharing? I can guide you step by step!
