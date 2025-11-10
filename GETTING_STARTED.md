# 🎂 Step-by-Step Getting Started Guide

Follow these steps to get your bakery application up and running!

## Step 1: Install Dependencies

Open your terminal/command prompt in the project directory and run:

```bash
npm install
```

**What this does:** Downloads and installs all the required packages (Next.js, React, Three.js, etc.)

**Expected time:** 2-5 minutes depending on your internet speed

**What to expect:** You'll see a lot of package names scrolling by. Wait until it says "added X packages" or similar.

---

## Step 2: Create Required Directories (Optional)

The app will create these automatically, but you can create them manually if you prefer:

```bash
npm run setup
```

Or manually:
```bash
mkdir -p public/models
mkdir -p data
```

**What this does:** Creates folders where 3D models and data will be stored

**Note:** If you skip this, the folders will be created automatically when you first upload a model.

---

## Step 3: Start the Development Server

Run this command:

```bash
npm run dev
```

**What this does:** Starts the Next.js development server

**What to expect:** You should see output like:
```
▲ Next.js 14.0.4
- Local:        http://localhost:3000
- Ready in 2.3s
```

**Important:** Keep this terminal window open! The server needs to keep running.

---

## Step 4: Open the Application

1. Open your web browser (Chrome, Firefox, Edge, or Safari)
2. Go to: **http://localhost:3000**
3. You should see the home page with:
   - "Bakers" title
   - Two cards: "Design Your Cake" and "Admin Panel"

**If you see an error:**
- Make sure the dev server is still running (Step 3)
- Check that port 3000 isn't being used by another application
- Try refreshing the page

---

## Step 5: Upload Your First 3D Model (Admin Panel)

Before you can design cakes, you need to upload some 3D models:

1. **Click "Go to Admin →"** on the home page (or go to http://localhost:3000/admin)

2. **Click "Upload Model"** button (top right)

3. **Fill in the form:**
   - **Model File:** Click to select a GLTF or GLB file from your computer
   - **Name:** Give it a name (e.g., "Chocolate Base Layer")
   - **Type:** Choose from dropdown:
     - `base` - Bottom/base of the cake
     - `layer` - Middle layers
     - `decoration` - Decorative elements
     - `topping` - Top decorations
     - `frosting` - Frosting/icing
   - **Category:** Enter a category (e.g., "Chocolate", "Vanilla", "Strawberry")
   - **Price:** Enter price in dollars (e.g., 5.99)
   - **Nutritional Information:** Fill in all the values:
     - Calories (kcal)
     - Protein (grams)
     - Carbs (grams)
     - Fat (grams)
     - Sugar (grams)
     - Fiber (grams) - Optional
     - Sodium (mg) - Optional

4. **Click "Upload Model"**

5. **Success!** You should see your model appear in the "Uploaded Models" section

**Repeat this step** to upload more models (different layers, decorations, etc.)

---

## Step 6: Design Your First Cake

1. **Go back to the home page** (click "Home" or go to http://localhost:3000)

2. **Click "Start Designing →"** (or go to http://localhost:3000/design)

3. **You'll see three sections:**
   - **Left side:** Component Library (your uploaded models)
   - **Center:** 3D Canvas (where you build your cake)
   - **Right side:** Nutritional Panel (shows nutrition info)

4. **Build your cake:**
   - **Browse** the Component Library on the left
   - **Filter** by type using the buttons (All, Bases, Layers, etc.)
   - **Drag a component** from the library
   - **Drop it** onto the 3D canvas in the center
   - **Watch it appear** in 3D!

5. **Interact with the 3D view:**
   - **Rotate:** Click and drag
   - **Zoom:** Scroll with mouse wheel
   - **Pan:** Right-click and drag (or middle mouse button)

6. **Add more components:**
   - Keep dragging and dropping to build your cake
   - Each component appears stacked on top
   - The nutritional panel updates automatically

7. **Check your nutrition:**
   - Look at the right panel to see:
     - Total calories
     - Protein, carbs, fat, sugar
     - Progress bars showing % of daily values
     - Total price

8. **Save your cake:**
   - Click "Save Cake" button (top right)
   - Enter a name for your cake
   - Click "Save"
   - Your design is now saved!

---

## Step 7: Test Everything Works

✅ **Checklist:**

- [ ] Home page loads correctly
- [ ] Admin panel loads
- [ ] Can upload a 3D model
- [ ] Model appears in the list
- [ ] Design page loads
- [ ] Component library shows uploaded models
- [ ] Can drag and drop components
- [ ] 3D viewer shows the cake
- [ ] Can rotate/zoom the 3D view
- [ ] Nutritional panel updates
- [ ] Can save a cake design

---

## Troubleshooting

### ❌ "npm install" fails
- **Solution:** Make sure you have Node.js 18+ installed
- Check: `node --version` in terminal
- Download from: https://nodejs.org/

### ❌ "Port 3000 is already in use"
- **Solution:** Close other applications using port 3000, or:
- Change port: `npm run dev -- -p 3001`
- Then use: http://localhost:3001

### ❌ 3D models don't appear
- **Check:** File format is GLTF or GLB
- **Check:** File uploaded successfully in admin panel
- **Check:** Browser console for errors (F12)

### ❌ Drag and drop doesn't work
- **Check:** You're dragging from Component Library
- **Check:** Dropping on the 3D canvas area
- **Try:** Refreshing the page

### ❌ "Module not found" errors
- **Solution:** Run `npm install` again
- Make sure you're in the project directory

---

## Next Steps After Setup

1. **Upload more models:**
   - Create or download more GLTF/GLB cake models
   - Upload them through the admin panel
   - Organize by type and category

2. **Customize the design:**
   - Edit colors in `tailwind.config.js`
   - Modify components in the `components/` folder
   - Adjust styling in `app/globals.css`

3. **Add features:**
   - User authentication
   - Database integration (replace JSON files)
   - Export cake designs as images
   - Share functionality

4. **Deploy:**
   - Build for production: `npm run build`
   - Deploy to Vercel, Netlify, or your preferred hosting

---

## Quick Reference Commands

```bash
# Install dependencies
npm install

# Start development server
npm run dev

# Build for production
npm run build

# Run production server
npm start

# Run setup script
npm run setup

# Check for linting errors
npm run lint
```

---

## Need Help?

- Check the main `README.md` for detailed documentation
- Review code comments in the component files
- Check browser console (F12) for error messages
- Ensure all dependencies are installed correctly

---

**You're all set! 🎉 Start designing amazing cakes!**

