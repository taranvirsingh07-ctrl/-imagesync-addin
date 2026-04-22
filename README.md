[README.md](https://github.com/user-attachments/files/26975183/README.md)
# 🔁 ImageSync — PowerPoint Add-in
### Replace a master image across all 100+ slides in one click!

---

## 📦 What's Included

| File | Purpose |
|------|---------|
| `taskpane.html` | The main add-in UI (all logic lives here) |
| `manifest.xml` | Tells PowerPoint about your add-in |
| `README.md` | This guide |

---

## 🚀 How to Install (Step-by-Step)

### Option A — Quickest: Sideload via File Share (Windows)

1. **Host the files locally**
   - Put the `ImageSync-Addin` folder somewhere on your PC, e.g.:
     `C:\ImageSync-Addin\`

2. **Open PowerPoint** → Go to:
   `File → Options → Trust Center → Trust Center Settings → Trusted Add-in Catalogs`

3. Add this path as a **Catalog URL**:
   `C:\ImageSync-Addin\`
   ✅ Check "Show in Menu" → Click OK → Restart PowerPoint

4. In PowerPoint go to:
   `Insert → My Add-ins → Shared Folder → ImageSync`

5. The **ImageSync panel** will open on the right side! 🎉

---

### Option B — Host on a Local Web Server (Recommended for Teams)

1. Install Node.js from https://nodejs.org

2. Open a terminal in the `ImageSync-Addin` folder and run:
   ```
   npx http-server . -p 3000 --ssl
   ```

3. Open `manifest.xml` and make sure the URLs say:
   `https://localhost:3000/taskpane.html`

4. Sideload the manifest in PowerPoint:
   `Insert → My Add-ins → Upload My Add-in → Browse to manifest.xml`

---

## 🎯 How to Use

Once the panel is open in PowerPoint:

### Step 1 — Tag Your Master Image
- Click on the image you want to replace (e.g., your motorcycle photo)
- In the ImageSync panel, click **"Tag Selected Image as Master"**
- You'll see a confirmation showing which slide it was found on ✅

### Step 2 — Choose Your New Image
- Click **"Choose new image"** in the panel
- Browse and select your replacement photo from your computer
- A preview of the new image will appear

### Step 3 — Replace Everywhere!
- Click **"Replace on All Slides"**
- A progress bar shows it scanning through your slides
- Done! You'll see how many slides were updated ✅

---

## ❓ FAQ

**Q: What if I have 100 slides?**
A: No problem! The add-in loops through every single slide automatically.

**Q: Does it keep the same position and size?**
A: Yes! The replacement image inherits the exact same position, width, and height as the original.

**Q: What image formats are supported?**
A: JPG, PNG, GIF, WebP — any standard web image format.

**Q: Can I replace multiple different master images?**
A: Yes! Click Reset, then start again with a different image.

---

## 🛠 Troubleshooting

| Problem | Fix |
|---------|-----|
| "No image selected" error | Make sure you click on the image IN the slide first, then press the button |
| "0 slides replaced" | The image on other slides may be a different file — try re-inserting the same image on all slides before tagging |
| Add-in doesn't appear | Make sure the manifest.xml path is correct and PowerPoint was restarted |

---

Made with ❤️ — ImageSync v1.0
