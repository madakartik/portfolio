# Three.js Spotlight Demo

This is an interactive Three.js WebGL application that demonstrates advanced spotlight lighting techniques with real-time parameter controls.

## Features

- Interactive spotlight with adjustable parameters
- Real-time shadow casting and receiving
- 3D model loading (Lucy statue)
- Multiple texture projection options
- Circular light animation
- GUI controls for all lighting parameters

## Directory Structure

```
threejs-spotlight-demo/
├── index.html              # Main HTML file
├── main.css                # Stylesheet
├── server.py               # Python HTTP server
├── README.md               # This file
├── build/
│   └── three.module.js     # Three.js core library
├── jsm/
│   ├── libs/
│   │   └── lil-gui.module.min.js
│   ├── loaders/
│   │   └── PLYLoader.js
│   └── controls/
│       └── OrbitControls.js
├── textures/
│   ├── disturb.jpg
│   ├── colors.png
│   └── uv_grid_opengl.jpg
└── models/
    └── ply/
        └── binary/
            └── Lucy100k.ply
```

## How to Run

### Option 1: Python HTTP Server (Recommended)

1. Navigate to the project directory:
   ```bash
   cd threejs-spotlight-demo
   ```

2. Start the server:
   ```bash
   python3 server.py
   ```

3. Open your browser and visit: `http://localhost:8080`

### Option 2: Node.js HTTP Server

If you have Node.js installed:

```bash
cd threejs-spotlight-demo
npx http-server -p 8080 --cors
```

### Option 3: PHP Server

If you have PHP installed:

```bash
cd threejs-spotlight-demo
php -S localhost:8080
```

## Controls

The GUI panel on the right allows you to adjust:

- **Map**: Select different texture projections for the spotlight
- **Color**: Change the spotlight color
- **Intensity**: Adjust light brightness (0-500)
- **Distance**: Set light falloff distance (0-20)
- **Angle**: Control spotlight cone angle (0 to π/3)
- **Penumbra**: Adjust edge softness (0-1)
- **Decay**: Set light attenuation (1-2)
- **Focus**: Control shadow sharpness (0-1)
- **Shadows**: Toggle shadow rendering on/off

## Camera Controls

- **Left Mouse**: Rotate around the scene
- **Right Mouse**: Pan the camera
- **Mouse Wheel**: Zoom in/out

## Requirements

- Modern web browser with WebGL support
- Local HTTP server (due to CORS restrictions)
- Internet connection for initial setup (to download dependencies)

## Troubleshooting

1. **Black screen**: Make sure you're serving the files through an HTTP server, not opening the HTML file directly in the browser.

2. **Missing textures/models**: Ensure all files were downloaded correctly and the directory structure matches the above.

3. **Console errors**: Check the browser developer console for any missing file errors.

## License

This demo uses Three.js which is licensed under the MIT License.
