#
```

### Option 2: Deploy to GitHub Pages

1. Fork or copy this repository to your GitHub account.
2. Go to **Settings → Pages**.
3. Under **Branch**, select `main` and folder `/` (root).
4. Click **Save**.
5. Your app is live at `https://<your-username>.github.io/<repo-name>/`

### Option 3: Netlify / Vercel / Cloudflare Pages

Drag-and-drop the project folder to any static site host. No build step needed.

## 📦 Dependencies (via CDN)

| Library ↕▾ | Purpose ↕▾ | CDN ↕▾ |
|---|---|---|
| −[pdf-lib](https://pdf-lib.js.org/) | PDF merge & extract | unpkg.com |
| −[browser-image-compression](https://github.com/Donaldcwl/browser-image-compression) | Image compression | jsdelivr.net |
| −[lamejs](https://github.com/zhuker/lamejs) | MP3 encoding | cdnjs.cloudflare.com |
| [pdf.js](https://mozilla.github.io/pdf.js/) | PDF rendering (included but optional) | cdnjs.cloudflare.com |
⚙

## ⚠️ Limitations

- **Video→MP3**: Only works with browser-supported video codecs (H.264/AAC for MP4, VP8/VP9/Opus for WebM). Some MKV files may not be decodable depending on the browser.
- **Website→MP3**: Google Translate TTS endpoint is used for speech synthesis. It is a free, unofficial endpoint and may be rate-limited. Long texts take time — approximately 200 characters per TTS request with a 300ms delay between requests.
- **File size**: While there is no hard limit, browser memory will constrain very large files. For best results, keep video files under ~500 MB.
- **CORS**: Website fetching relies on public CORS proxies (allorigins, corsproxy.io). If a site blocks proxies, fetching may fail.

## 🔒 Privacy

All file processing happens **locally in your browser**. Your PDFs, images, and videos never leave your device. The only network calls are:

- Fetching website content (when using the Website→MP3 tool)
- Google Translate TTS API (for text-to-speech)
- CDN library loading

## 📁 Project Structure

```

```

## 🛠️ Tech Stack

- **HTML5 / CSS3 / Vanilla JavaScript** — No frameworks, no build step
- **Web Audio API** — Audio processing and encoding
- **MediaRecorder API** — Capturing audio streams
- **Canvas API** — Image resizing
- **File API** — File reading and manipulation
- **DOMParser** — HTML text extraction

## 📄 License

MIT — Use, modify, and distribute freely.

```

</B
