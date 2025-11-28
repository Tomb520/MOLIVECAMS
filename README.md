[README (1).md](https://github.com/user-attachments/files/23827262/README.1.md)
# YouTube Live Stream Viewer 🎥

An interactive web app that connects to your YouTube account, finds live streams, and automatically cycles through them every 10 seconds.

## 🌐 Live Demo

Visit: `https://YOUR-USERNAME.github.io/youtube-live-viewer/`

## ✨ Features

- 🔐 Secure YouTube OAuth authentication
- 🔍 Automatically searches for live streams
- ▶️ Auto-plays and switches between streams every 10 seconds
- ⏸️ Pause/resume auto-switching
- 📋 View full playlist of found streams
- 🖱️ Click any stream to jump directly to it
- 💾 Remembers your API credentials (stored locally in your browser)

## 🚀 Setup Instructions

### 1. Get YouTube API Credentials

1. Go to [Google Cloud Console](https://console.cloud.google.com/)
2. Create a new project (or select an existing one)
3. Click "Enable APIs and Services"
4. Search for "YouTube Data API v3" and enable it
5. Go to "Credentials" → "Create Credentials" → "OAuth client ID"
6. Choose "Web application"
7. Add your website URL to "Authorized JavaScript origins":
   - For GitHub Pages: `https://YOUR-USERNAME.github.io`
   - For local testing: `http://localhost:8000`
8. Copy the Client ID

### 2. Use the App

1. Open the website
2. Paste your Client ID in the input field
3. Click "Connect YouTube Account"
4. Authorize the app
5. Click "Find Live Streams"
6. Enjoy! The app will auto-play and switch streams every 10 seconds

## 🛠️ Local Development

To run locally:

```bash
# Using Python
python -m http.server 8000

# Then open: http://localhost:8000
```

Or use VS Code's Live Server extension.

## 📝 How to Deploy to GitHub Pages

1. Fork or clone this repository
2. Rename the HTML file to `index.html`
3. Push to your GitHub repository
4. Go to Settings → Pages
5. Select "main" branch as source
6. Your site will be live at `https://YOUR-USERNAME.github.io/youtube-live-viewer/`

## 🔒 Privacy & Security

- Your Client ID is stored only in your browser's local storage
- No data is sent to any third-party servers
- The app only requests read-only access to YouTube
- OAuth Client IDs are safe to be public (they're restricted by authorized origins)

## 🎨 Customization

You can easily customize:
- **Search query**: Change the search terms in the code (line ~186)
- **Switch interval**: Change the countdown time (line ~198)
- **Number of results**: Modify `maxResults` parameter (line ~181)
- **Video category**: Change `videoCategoryId` to filter by category

## 📚 Technologies Used

- HTML5
- CSS3 (with gradients and animations)
- Vanilla JavaScript
- YouTube Data API v3
- YouTube IFrame Player API
- Google OAuth 2.0

## ⚠️ Troubleshooting

**"No live streams found"**
- Try again, as availability varies
- Modify the search query to be broader or more specific

**"Error searching for streams"**
- Check that your Client ID is correct
- Verify your domain is in authorized origins
- Make sure YouTube Data API v3 is enabled

**"Authentication failed"**
- Clear your browser's local storage and try again
- Verify the authorized origins match your URL exactly

## 📄 License

MIT License - feel free to modify and use as you wish!

## 🤝 Contributing

Pull requests are welcome! Feel free to improve the search algorithm, UI, or add new features.

---

Made with ❤️ for exploring live content on YouTube
