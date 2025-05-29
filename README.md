# ArUco 3D STL Generator

[![Live Demo](https://img.shields.io/badge/Live%20Demo-Available-brightgreen)](https://michielryvers.github.io/aruco-stl-generator/)
[![3D Printing](https://img.shields.io/badge/3D%20Printing-Ready-orange)](https://michielryvers.github.io/aruco-stl-generator/)

> 🎯 **Generate 3D printable ArUco markers with raised patterns for computer vision and tactile applications**

## ✨ Features

- 🔧 **Multiple ArUco Dictionaries**: Support for 4x4, 5x5, 6x6, and 7x7 marker types
- 📏 **Customizable Dimensions**: Adjust marker size, thickness, and protrusion height
- 🖨️ **3D Print Ready**: Optimized STL files with minimal geometry for fast printing
- 🎨 **Modern Web Interface**: Clean, responsive design built with Tailwind CSS
- ⚡ **Client-Side Processing**: No server required - runs entirely in your browser
- 📱 **Mobile Friendly**: Works on desktop, tablet, and mobile devices
- 🔍 **OpenCV.js Integration**: Uses the official OpenCV library for accurate marker generation

## 🚀 Quick Start

**[🌐 Try it now - No installation required!](https://michielryvers.github.io/aruco-stl-generator/)**

1. Choose your ArUco dictionary type
2. Enter the marker ID(s) you want to generate
3. Customize dimensions and settings
4. Click "Generate & Download STL"
5. Print and use!

## 🎛️ Configuration Options

| Parameter             | Description             | Range                              | Default |
| --------------------- | ----------------------- | ---------------------------------- | ------- |
| **Dictionary**        | ArUco marker type       | 4x4_50, 5x5_100, 6x6_250, 7x7_1000 | 4x4_50  |
| **Marker ID**         | Unique identifier(s)    | 0 to dictionary max                | 0       |
| **Size**              | Total marker dimension  | 10-200mm                           | 50mm    |
| **Base Thickness**    | Background plate height | 0.5-10mm                           | 2mm     |
| **Protrusion Height** | Raised pattern height   | 0.1-5mm                            | 0.5mm   |
| **Border Size**       | White border width      | 0-5 units                          | 1       |

## 📖 About ArUco Markers

ArUco markers are square fiducial markers widely used in:

- **Computer Vision**: Camera pose estimation and object tracking
- **Robotics**: Navigation and localization systems
- **Augmented Reality**: Marker-based AR applications
- **3D Scanning**: Reference points for photogrammetry
- **Educational Projects**: Teaching computer vision concepts

This generator creates **tactile versions** with raised black patterns, perfect for:

- Applications requiring physical texture
- Low-light environments where visual detection is challenging
- Educational demonstrations
- Prototyping and testing

## 🛠️ Technical Details

### Technologies Used

- **Frontend**: Vanilla JavaScript, HTML5, Tailwind CSS
- **3D Graphics**: Three.js for geometry generation
- **Computer Vision**: OpenCV.js for marker pattern generation
- **Export**: STLExporter for 3D printing compatibility

### STL File Structure

- **Base Layer**: Flat surface for stability
- **Raised Patterns**: Black bits extruded upward
- **Optimized Geometry**: Minimal polygons for faster processing
- **Print-Ready**: Designed for FDM and SLA printers

## 🖨️ 3D Printing Tips

### Recommended Settings

- **Layer Height**: 0.2mm or finer for clean details
- **Infill**: 15-20% (markers are mostly solid anyway)
- **Supports**: Not required for standard orientations

### Print Orientation

- Place markers flat on the build plate
- Black patterns face up for best detail resolution
- No supports needed for standard configurations

## 🔧 Local Development

To run locally:

```bash
# Clone the repository
git clone https://github.com/michielryvers/aruco-stl-generator.git
cd aruco-stl-generator

# Serve with any static file server
# Python
python -m http.server 8000

# Node.js
npx serve .

# Or simply open index.html in your browser
```

## 🚀 Development & Deployment

### Quick Start (Zero Setup)

Just open `index.html` in your browser! The app automatically uses Tailwind CDN for local development.

### Custom CSS Development

If you want to modify the Tailwind styles:

```bash
# Install dependencies
npm install

# Build custom CSS (one-time)
npm run build-css

# Build custom CSS (watch mode for development)
npm run dev
```

### Architecture

- **Local Development**: Uses Tailwind CDN (fast, no build required)
- **Production**: Uses custom built CSS (optimized, smaller bundle)
- **Auto-Detection**: JavaScript automatically detects environment and loads appropriate CSS

The project automatically builds optimized CSS for production via GitHub Actions when deployed.

## 🙏 Acknowledgments

- [OpenCV.js](https://docs.opencv.org/4.x/d5/d10/tutorial_js_root.html) for computer vision functionality
- [Three.js](https://threejs.org/) for 3D graphics and STL export
- [Tailwind CSS](https://tailwindcss.com/) for styling
- The computer vision community for ArUco marker specifications

---

**[🌐 Live Demo](https://michielryvers.github.io/aruco-stl-generator/) | [📧 Report Issues](https://github.com/michielryvers/aruco-stl-generator/issues)**
