# background-remove

A powerful React + Vite application that removes backgrounds from images directly in your browser. Utilizing machine learning models via Transformers.js, this tool ensures complete local processing—your files never leave your device.

## Key Features

- 🚀 One-click image background removal
- 🎨 Customize with transparent, colored, or image backgrounds
- 💾 Download options for transparent or modified backgrounds
- 🏃‍♂️ Fully browser-based—no server uploads required
- 🔒 Privacy-first—everything runs locally on your device
- ⚡ Optional WebGPU acceleration for enhanced performance

## Technical Approach

This app employs a cross-browser background removal technique, with optional WebGPU acceleration for improved efficiency.

### Standard Processing (Works on All Browsers)

- Utilizes RMBG-1.4, a high-performance background removal model
- Ensures compatibility with all modern browsers
- Processes images efficiently using WebAssembly
  
### WebGPU-Enhanced Processing (For Supported Browsers)
- Enables MODNet for users with WebGPU-compatible browsers
- Can be activated via a dropdown menu
- Uses GPU acceleration for potentially faster performance

Both approaches rely on Transformers.js to run AI models directly in the browser, eliminating the need for server-side processing.

## How It Works

1. **Upload an Image**: Select any image file
2. **Choose a Model**:
   - RMBG-1.4 is the default for maximum compatibility
   - MODNet is available if WebGPU support is detected
3. **Remove the Background**: The AI model processes the image and generates an alpha mask
4. **Customize the Background**: Choose a solid color, another image, or keep it transparent
5. **Download the Result**: Save your processed image in your preferred format

## Getting Started

1. Clone the repository:
```bash
git clone https://github.com/JMBoulos12/background-remove.git
```

3. Start the development server:
```bash
npm run dev
```

## Browser Support

- **Default Experience**: All modern browsers (Chrome, Firefox, Safari, Edge)
- **Optional WebGPU**: Available in browsers with WebGPU support (Chrome Canary with WebGPU flags enabled)

## Technical Stack

- React + Vite for the frontend framework
- Transformers.js for ML model inference
- RMBG-1.4 as the default cross-browser model
- Optional WebGPU acceleration with MODNet
- IndexedDB (via Dexie.js) for local file management
- TailwindCSS for styling

## Credits

Inspired by the WebGPU background removal demo by @xenova.

## License

MIT License - feel free to use this in your own projects!
