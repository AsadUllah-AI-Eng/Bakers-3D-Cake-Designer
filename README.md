# Bakers - Custom Cake Designer 🎂

A modern, interactive web application for customizing cakes with 3D visualization, drag-and-drop functionality, and nutritional profile tracking.

## Features

- 🎨 **3D Cake Visualization**: View your custom cake in real-time 3D using React Three Fiber
- 🖱️ **Drag & Drop Interface**: Easily add components to your cake by dragging from the component library
- 📊 **Nutritional Profile**: Track calories, protein, carbs, fat, sugar, and more with visual progress bars
- 🎯 **Component Library**: Organize cake components by type (base, layer, decoration, topping, frosting)
- 👨‍💼 **Admin Panel**: Upload and manage 3D models (GLTF/GLB format) with nutritional information
- 💾 **Save Designs**: Save your custom cake designs for later
- 🎨 **Modern UI**: Beautiful, responsive design with Tailwind CSS

## Tech Stack

- **Next.js 14** - React framework with App Router
- **React Three Fiber** - 3D rendering library
- **Three.js** - 3D graphics library
- **@dnd-kit** - Drag and drop functionality
- **Zustand** - State management
- **Tailwind CSS** - Styling
- **TypeScript** - Type safety

## Getting Started

### Prerequisites

- Node.js 18+ installed
- npm or yarn package manager

### Installation

1. Install dependencies:
```bash
npm install
```

2. Create necessary directories:
```bash
mkdir -p public/models data
```

3. Run the development server:
```bash
npm run dev
```

4. Open [http://localhost:3000](http://localhost:3000) in your browser

## Usage

### For Users (Designing Cakes)

1. Navigate to the **Design** page from the home screen
2. Browse the **Component Library** on the left
3. **Drag and drop** components onto the 3D canvas
4. View your cake in **3D** - rotate, zoom, and pan to see all angles
5. Check the **Nutritional Panel** on the right to see calories, macros, and price
6. Click **Save Cake** to save your design

### For Admins (Uploading Models)

1. Navigate to the **Admin Panel** from the home screen
2. Click **Upload Model**
3. Select a **GLTF or GLB** 3D model file
4. Fill in the details:
   - Name
   - Type (base, layer, decoration, topping, frosting)
   - Category
   - Price
   - Nutritional information (calories, protein, carbs, fat, sugar, etc.)
5. Click **Upload Model**

## 3D Model Requirements

- **Format**: GLTF or GLB files
- **Size**: Recommended under 10MB for best performance
- **Optimization**: Use compressed textures and optimized geometry
- **Positioning**: Models should be centered at origin (0,0,0)

## Project Structure

```
bakers/
├── app/
│   ├── api/              # API routes
│   │   ├── models/       # Model management endpoints
│   │   └── cakes/        # Cake saving endpoints
│   ├── admin/            # Admin panel page
│   ├── design/           # Cake designer page
│   ├── layout.tsx        # Root layout
│   ├── page.tsx          # Home page
│   └── globals.css       # Global styles
├── components/
│   ├── CakeCanvas.tsx    # Drag-and-drop canvas
│   ├── CakeViewer.tsx    # 3D viewer component
│   ├── ComponentLibrary.tsx  # Component browser
│   ├── DndProvider.tsx   # Drag-and-drop context
│   └── NutritionalPanel.tsx  # Nutrition display
├── lib/
│   ├── api.ts            # API client functions
│   ├── store.ts          # Zustand state store
│   ├── types.ts          # TypeScript types
│   └── utils.ts          # Utility functions
├── public/
│   └── models/           # Uploaded 3D models (created at runtime)
└── data/
    ├── models.json       # Model metadata (created at runtime)
    └── cakes.json        # Saved cakes (created at runtime)
```

## Data Storage

The application uses JSON files for data storage (located in the `data/` directory):
- `models.json` - Stores metadata about uploaded 3D models
- `cakes.json` - Stores saved custom cake designs

For production, consider migrating to a proper database (PostgreSQL, MongoDB, etc.).

## Customization

### Colors

Edit `tailwind.config.js` to customize the color scheme:
- Primary colors: Pink/Purple gradient
- Cake-specific colors: Cream, Chocolate, Strawberry, Vanilla

### Component Types

Component types are defined in `lib/types.ts`. You can add new types by:
1. Updating the `CakeComponent` type
2. Adding new options to the admin panel dropdown
3. Adding new filter buttons in the ComponentLibrary

## Troubleshooting

### 3D Models Not Loading

- Ensure models are in GLTF or GLB format
- Check browser console for errors
- Verify model files are accessible in `public/models/`

### Drag and Drop Not Working

- Ensure you're dragging from the Component Library
- Drop zone is the 3D canvas area
- Check browser console for errors

### Upload Fails

- Check file size (should be reasonable)
- Verify all required fields are filled
- Check server logs for errors

## Future Enhancements

- [ ] User authentication and accounts
- [ ] Share cake designs with others
- [ ] Export cake designs as images
- [ ] Advanced 3D model positioning controls
- [ ] Color customization for components
- [ ] Recipe generation from custom cakes
- [ ] Integration with ordering system
- [ ] Mobile app version

## License

This project is open source and available for customization.

## Support

For issues or questions, please check the code comments or create an issue in your repository.

---

Made with ❤️ for bakers and cake lovers everywhere!
