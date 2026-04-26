# 🎨 Art Across Time — Teacher Guide
### A PA Standards-Aligned Art Education Adventure

---

## What Is This?

**Art Across Time** is a standalone, browser-based 8-bit art education game for middle school students. Players travel through 6 historical worlds and discover 36 famous masterworks — each with rich descriptions, fascinating true stories, and Pennsylvania State Art Standards tags.

**No installation. No login. No internet account.** Just open `index.html` in any browser.

---

## Quick Start

1. **Double-click** `index.html` to open in any web browser
2. Press **SPACE** or **ENTER** (or tap **▶ PRESS START**)
3. Choose a world with arrow keys or click
4. Navigate paintings with **← →** arrow keys
5. Press **ENTER** to view a painting with facts

> **Chromebook users:** Works perfectly in Chrome. All keyboard shortcuts active.

---

## The 6 Worlds (36 Total Paintings)

| World | Period | PA Standards |
|-------|--------|-------------|
| 🏛️ Renaissance Florence | 1400–1600 CE | 9.2.8.A · 9.3.8.A |
| 🗼 Impressionist Paris | 1860–1890 CE | 9.1.8.B · 9.2.8.C |
| 🌷 Dutch Golden Age | 1600–1700 CE | 9.2.8.A · 9.1.8.B |
| ⛩️ Edo Japan & Ukiyo-e | 1600–1868 CE | 9.2.8.B · 9.1.8.C |
| 🏺 Ancient Egypt | 3100–30 BCE | 9.2.8.A · 9.2.8.B |
| 🎷 Harlem Renaissance | 1920–1940 CE | 9.2.8.C · 9.3.8.B |

---

## Keyboard Navigation (Full Chromebook Support)

| Key | Action |
|-----|--------|
| `SPACE` / `ENTER` | Start game / Select / Open painting |
| `← → ↑ ↓` | Navigate worlds and paintings |
| `ESC` | Go back / Close modal |
| `CTRL + T` | Open Teacher Panel |
| `TAB` | Cycle through buttons (accessibility) |

---

## Teacher Panel

Access the Teacher Panel by:
- Clicking **👩‍🏫 TEACHER** button on the title screen
- Pressing **CTRL + T** anytime

**Default PIN: `art1234`**
*(Change this in Settings after first login)*

### What Teachers Can Do:

#### ➕ Add Artwork
Add your own paintings to any world:
- Paste an **image URL** from any open-access source
- **Upload an image file** (PNG/JPG/GIF — up to 5MB, embedded in export)
- Fill in title, artist, year, medium, location, source, description
- Add up to 4+ fun facts (one per line, start with emoji for style!)
- Tag a PA Standard

#### 📋 Manage
- View all 36+ artworks
- Filter by world
- Delete any artwork (custom or built-in)

#### 📂 Import / Export
- **Import JSON** — Paste a JSON array of artwork objects for bulk import (great for sharing between teachers)
- **Export Current JSON** — Download all artwork data as a JSON file
- **Download HTML Game** — Export a complete standalone `.html` file with all your customizations embedded. Share via Google Classroom, email, or USB drive.

#### ⚙️ Settings
- Change the Teacher PIN
- Reset student progress (clears all "discovered" badges)

---

## Adding Artworks: JSON Format

When importing via JSON, use this format:

```json
[
  {
    "worldId": "harlem",
    "title": "Nightlife",
    "artist": "Archibald Motley Jr.",
    "year": "1943",
    "medium": "Oil on canvas",
    "location": "Art Institute of Chicago",
    "source": "Art Institute of Chicago Open Access",
    "url": "https://www.artic.edu/iiif/2/[image-id]/full/843,/0/default.jpg",
    "description": "A vibrant Harlem nightclub scene...",
    "paStandard": "9.2.8.C – Art as Social Commentary",
    "facts": [
      "🎷 Motley painted the electric energy of Chicago's South Side jazz scene...",
      "🌈 His use of electric lighting was revolutionary in the 1940s...",
      "⭐ Fact three here...",
      "💡 Fact four here..."
    ]
  }
]
```

**Valid worldId values:** `florence`, `paris`, `dutch`, `japan`, `egypt`, `harlem`

---

## Open Access Image Sources

All built-in images come from these public domain / open access collections:

| Source | URL | License |
|--------|-----|---------|
| **Met Open Access** | https://metmuseum.org | CC0 |
| **Wikimedia Commons** | https://commons.wikimedia.org | Public Domain |
| **Art Institute of Chicago** | https://www.artic.edu/open-access | CC0 |
| **Smithsonian Open Access** | https://www.si.edu/openaccess | CC0 |
| **National Gallery of Art** | https://www.nga.gov/open-access-images.html | CC0 |
| **Rijksmuseum** | https://www.rijksmuseum.nl/en/rijksstudio | CC0 |
| **Cleveland Museum of Art** | https://www.clevelandart.org/art/collection/search | CC0 |

### Finding Image URLs

**Met Museum:**  
Search at `https://www.metmuseum.org/art/collection` → Open an artwork → Right-click image → "Copy image address"

**Art Institute of Chicago:**  
Find artwork → Use IIIF URL: `https://www.artic.edu/iiif/2/{OBJECT-ID}/full/843,/0/default.jpg`

**Wikimedia Commons:**  
Search at `commons.wikimedia.org` → Click image → Use the full-resolution URL

---

## PA State Standards Alignment

This game directly supports:

| Standard | Description | Worlds |
|----------|-------------|--------|
| **9.1.8.A** | Production — materials, techniques, processes | Florence, Egypt |
| **9.1.8.B** | Production — elements and principles | All worlds |
| **9.1.8.C** | Production — vocabulary and techniques | Florence, Paris, Japan |
| **9.2.8.A** | Historical & Cultural Contexts | Florence, Dutch, Egypt |
| **9.2.8.B** | Chronological relationships | Japan, Egypt |
| **9.2.8.C** | Art movements and cross-cultural influences | Paris, Harlem |
| **9.3.8.A** | Critical Response — describe and analyze | Dutch, Japan |
| **9.3.8.B** | Critical Response — aesthetic judgment | Paris, Harlem |

---

## Sharing With Students

### Google Classroom
1. Use **Teacher Panel → Export → Download HTML Game**
2. Upload the `.html` file to Google Drive
3. Share the Drive link with students — they open it in Chrome

### USB / Local Network
The `index.html` file runs completely offline once loaded. The only internet dependency is loading painting images from museum servers.

### Make It Your Own
Before sharing, you can:
- Add local/regional artwork relevant to your curriculum
- Add your school's own student artwork
- Remove paintings not relevant to your unit
- Export your customized version and distribute that

---

## Technical Notes

- **Tested:** Chrome, Firefox, Safari, Edge · Chromebook Chrome
- **Requires:** Internet connection for painting images · No internet needed for game UI
- **Storage:** Student progress saved locally (localStorage) — doesn't sync between devices
- **File size:** ~95KB base HTML · Grows slightly when you add image files via upload
- **Images:** Uploaded image files are stored as base64 inside the HTML — URLs are referenced externally

---

## Troubleshooting

| Problem | Solution |
|---------|----------|
| Painting image won't load | Use Teacher Panel to update the URL with a working source |
| Font looks wrong | Ensure internet connection (loads Google Fonts) or the browser cached it |
| PIN forgotten | Open the file in a text editor, find `pin:'art1234'` and read/edit it |
| Progress not saving | Some browsers block localStorage in certain modes — try a regular window |
| Game looks tiny/huge | Use browser zoom (CTRL + / CTRL -) to adjust |

---

## Classroom Activity Ideas

**🗓️ Discovery Journal:** Students keep a paper journal — for each painting they view, they write one thing they noticed and one thing they wondered.

**🎨 Connections:** After exploring a world, ask: "What do these 6 paintings have in common? What's different?"

**🌍 Time Travel Challenge:** Can students visit all 36 paintings in one class period? Have them count down together.

**✍️ Fact or Fiction?** Discuss which "fascinating facts" sound most unbelievable — then research to verify.

**🏆 World Expert:** Assign groups to become "experts" on one world and teach it to the rest of the class.

---

## Credits & Sources

- **Game concept & development:** Generated with Claude (Anthropic)
- **Artwork images:** Metropolitan Museum of Art Open Access, Wikimedia Commons (Public Domain), Art Institute of Chicago Open Access, Smithsonian American Art Museum Open Access
- **Typography:** Press Start 2P (Google Fonts, SIL Open Font License)
- **PA Standards:** Pennsylvania Department of Education — Visual Arts Standards (Grades 6-8)

---

*Art Across Time — Version 1.0*  
*Built for PA Middle School Art Education*
