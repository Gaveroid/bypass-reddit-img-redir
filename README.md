# Bypass Reddit image redirect

A Manifest V3 Chrome extension that stops Reddit's image CDN from redirecting direct image links to their media viewer.

## What this extension does

Reddit's CDN checks if the request's "Accept" header contains "text/html". If it does, it respnods with a 307 to the media viewer page. This extension sets "Accept" headers to "image/*" only when being sent to those hosts so the CDN serves the raw file. This is done with Manifest V3--no scripts, no collecting of your data.

## Install (unpacked)
1. Clone this repo
2. Open `chrome://extensions`
3. Enable "Developer mode" in the top right
4. Click "Load unpacked" and select the cloned folder.

Now when you navigate directly to an image served by redd.it, such as by right clicking on an image and selecting "Open image in new tab", the image will be loaded directly in the tab rather than through Reddit's media viewer.

If I missed any alternate domains or if there are any other media/file types that Reddit's CDN handles that this negatively impacts, please write up an issue on this repo and let me know.