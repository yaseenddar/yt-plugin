# YouTube Sentiment Analysis Chrome Extension

A Chrome extension that analyzes YouTube comments and provides sentiment insights using a Flask-powered machine learning backend.

## Repository

Extension Repository:

[yt-plugin GitHub Repository](https://github.com/yaseenddar/yt-plugin?utm_source=chatgpt.com)

A small chrome plugin to detect youtube comment sentiments
==============================
Snaps:
![alt text](image-4.png)
![alt text](image.png)

![alt text](image-1.png)

![alt text](image-2.png)

![alt text](image-3.png)
---

## Installation

### Option 1: Clone the Repository

```bash
git clone https://github.com/yaseenddar/yt-plugin.git
cd yt-plugin
```

### Option 2: Download ZIP

1. Visit the GitHub repository.
2. Click **Code** → **Download ZIP**.
3. Extract the ZIP file to a local folder.

---

## Load the Extension in Chrome

### Step 1: Open Extensions Page

Open Chrome and navigate to:

```text
chrome://extensions
```

### Step 2: Enable Developer Mode

Turn on **Developer mode** using the toggle in the top-right corner.

### Step 3: Load the Extension

1. Click **Load unpacked**.
2. Browse to the downloaded/cloned `yt-plugin` folder.
3. Select the folder containing:

```text
manifest.json
popup.html
popup.js
```

### Step 4: Verify Installation

You should now see:

```text
YouTube Sentiment Analysis
Version 1.0
```

listed in Chrome Extensions.

---

## Start the Backend Server

The extension requires the Flask backend to be running locally.

Start the backend:

```bash
cd yt-comment-sentiment-analysis/flask_app
python app.py
```

The backend API should be available at:

```text
http://localhost:5000
```

---

## Using the Extension

1. Open any YouTube video.
2. Click the **YouTube Sentiment Analysis** extension icon.
3. Start comment analysis.
4. The extension will:

   * Fetch YouTube comments
   * Send them to the Flask backend
   * Receive sentiment predictions
   * Display analytics and visualizations

---

## Required Permissions

The extension uses the following permissions:

| Permission                   | Purpose                                       |
| ---------------------------- | --------------------------------------------- |
| tabs                         | Access information about the current tab      |
| activeTab                    | Interact with the currently open YouTube page |
| scripting                    | Inject scripts when needed                    |
| http://localhost:5000/*      | Communicate with the Flask backend            |
| https://www.googleapis.com/* | Access YouTube-related API services           |

---

## Troubleshooting

### Extension Not Appearing

* Ensure Developer Mode is enabled.
* Verify that `manifest.json` exists in the selected folder.
* Reload the extension from `chrome://extensions`.

### Failed to Connect to Backend

Make sure:

```text
http://localhost:5000
```

is running before opening the extension.

### Changes Not Reflecting During Development

After modifying extension files:

1. Go to `chrome://extensions`
2. Click **Reload** on the extension card.
3. Refresh the YouTube page.

---

## Development Workflow

```bash
git clone https://github.com/yaseenddar/yt-plugin.git

# Load unpacked extension in Chrome

# Start backend
cd yt-comment-sentiment-analysis/flask_app
python app.py
```

The Chrome extension acts as the frontend, while the Flask application handles sentiment prediction, word cloud generation, and trend analysis.
