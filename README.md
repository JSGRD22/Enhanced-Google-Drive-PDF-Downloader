# Enhanced Google Drive PDF Downloader
A powerful userscript that enables downloading view-only PDFs from Google Drive with quality control options and real-time progress tracking. 

## 🎯 Use Case
- Download PDF files from Google Drive that are in "preview" mode
- Ideal for situations where direct download is disabled
- Works with documents containing text, images, and mixed content
- Perfect for students and researchers who need to save reference materials

## ✨ Features
- **Two Quality Modes**
  - Fast Mode: Quick processing, suitable for text-heavy documents
  - High Quality Mode: Detailed processing, better for documents with images
- **Progress Tracking**
  - Real-time page processing indicators
  - Clear visual feedback during download
- **User-Friendly Interface**
  - Intuitive toggle for quality settings
  - Information tooltip with usage instructions
  - Clean, modern design matching Google Drive's aesthetic
- **Smart Processing**
  - Automatic page orientation detection
  - Maintains original document dimensions
  - Preserves image quality

## 📝 Installation Steps

1. Install a userscript manager for Firefox: [Violentmonkey](https://addons.mozilla.org/zh-CN/firefox/addon/violentmonkey)
2. Install the script:
   - Click [here](https://raw.githubusercontent.com/JSGRD22/Enhanced-Google-Drive-PDF-Downloader/refs/heads/main/script.user.js) to install
   - Or copy the script content and create a new userscript in your manager

## 🚀 How to Use

1. Open a PDF file in Google Drive

2. The download button will appear in the top-right corner
   ![Step 2: Locate Button](./resources/20250604112219.png)

3. (Optional) Select quality mode:
   - Click the info icon (ℹ️)
   - Toggle between Fast/High Quality
   ![Step 3: Quality Settings](./resources/20250604112251.png)

4. Click "Download PDF"
   - Make sure to scroll through the document first to load all pages
   - Wait for the processing to complete

## ⚠️ Important Notes
- **Document Loading**: Scroll through the entire document before downloading to ensure all pages are loaded
- **Processing Time**: High Quality mode may take longer, especially for large documents
- **Browser Compatibility**: Tested on Firefox 159.0
- **UserScript Manager**: Only tested on Violentmonkey

## 🔧 Troubleshooting

Common issues and solutions:

| Issue | Solution |
|-------|----------|
| Can not see Download button | Make sure to use the latest version of Firefox, Violentmonkey and this script |
| Missing pages | Scroll through entire document first |
| Slow processing | Switch to Fast mode for quicker results |
| Download fails | Refresh page and try again |
| Blank pages | Make sure images are fully loaded |

## 🆕 Version History

### v2.1 (Current)
- Replace dynamic jspdf loading with `@require` and use `@grant unsafeWindow` so that jspdf can be successfully loaded
- Define `@inject-into content` to fix script not injecting at all in Violentmonkey
- Narrow `@match` scope to `https://drive.google.com/file/*` URLs only to prevent unnecessary injection in normal Drive pages. This fixes preview-related instability

### v2
- Added quality mode toggle
- Improved progress indicators
- Enhanced error handling

### v1
- Basic download functionality
- Fixed page orientation issues
- Added processing status messages

## 📄 License
MIT License - feel free to modify and distribute

## 🤝 Contributing
Contributions are welcome! Please feel free to submit a [Pull Request](https://github.com/JSGRD22/Enhanced-Google-Drive-PDF-Downloader/pulls)

## 🙏 Credits
- Uses [jsPDF](https://github.com/MrRio/jsPDF) library

---

For issues and feature requests, please [create an issue](https://github.com/JSGRD22/Enhanced-Google-Drive-PDF-Downloader/issues)
