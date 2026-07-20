# Thru Content Generator — iPhone

Same tool as the desktop version — branded X/Twitter post images (PNG, JPEG) and animated GIFs matching Thru's site style — but iOS Safari needs a couple of extra steps that desktop browsers don't.

## Getting the file open

Local `.html` files don't reliably run their JavaScript when opened straight from the Files app on iOS — Quick Look often just shows a static preview. The reliable path is to host it and open it as a real URL:

1. Push `thru-content-generator.html` to a **public** GitHub repo (via the web upload UI — no CLI needed)
2. Open the file in the repo, click **Raw**, copy that URL
3. Prepend `https://htmlpreview.github.io/?` to the raw URL, e.g.:
   ```
   https://htmlpreview.github.io/?https://raw.githubusercontent.com/USERNAME/REPO/main/thru-content-generator.html
   ```
4. Paste that full link into **Safari** (not Chrome — some canvas/worker behavior is more consistent in Safari on iOS)

Bookmark or add it to your Home Screen once it loads, so you don't have to re-paste the link every time.

## Using it on a small screen

The layout stacks vertically on phone-width screens: form fields on top, live canvas preview below as you scroll. Inputs are sized to avoid the auto-zoom-on-focus that iOS Safari triggers on small text fields, so typing shouldn't jump the page around.

## Saving images — this part is different from desktop

iOS Safari mostly ignores the normal "download" behavior for images generated in-browser. So on iPhone, tapping **Download PNG / JPEG / GIF** does this instead:

1. Opens the image in a **new tab**
2. **Long-press the image**
3. Tap **Save to Photos** (or **Save to Files**)

You'll see a reminder of this on-screen automatically when the tool detects it's running on iOS.

## GIF export on iPhone

GIF encoding needs an internet connection (it fetches the encoder from cdnjs.cloudflare.com the first time you tap the button) and takes a few seconds longer than PNG/JPEG. A status line under the buttons shows encoding progress — wait for "done" before switching away from Safari.

## If a download button seems to do nothing

- Check Safari hasn't blocked the pop-up — go to **Settings → Safari → Block Pop-ups** and either turn it off for this, or tap **allow** if prompted
- Make sure you're in Safari, not viewing through the Files/Quick Look preview or another in-app browser
