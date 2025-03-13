# YouTube Subtitle Downloader (Manual Trigger) with TrustedHTML Bypass

## Overview
This user script allows you to view or download YouTube video subtitles in SRT format with a manual trigger. It fetches the most default subtitles (auto-generated or the first available track) using the YouTube API. You can either open the subtitles in a new tab or download them directly, depending on the version you are using. 

This script bypasses YouTube's TrustedHTML policy and inserts a button with a spinner into the **Polymer dropdown element** (as seen in the image below).

![Polymer Dropdown Example](https://imgur.com/dyMCBKu.png)

## Versions

- **yt_translator_restorer_open_in_newtab.js**: This version fetches subtitles and opens them in a new tab for viewing.
- **yt_translator_restorer_download.js**: This version fetches subtitles and allows you to download them directly.

## Features
- **Manual Trigger**: Click the "Transcription" button to view or download subtitles.
- **TrustedHTML Bypass**: Handles YouTube's TrustedHTML policy to extract subtitles.
- **Polymer Button with Spinner**: A button with a spinner is injected into the YouTube interface's Polymer dropdown element.
- **Google API Integration**: Uses the [YouTube Data API](https://developers.google.com/youtube/v3/docs/captions/list?hl=it) to fetch the video captions (auto-subtitles or the first available subtitle track).

## How It Works
1. The script fetches the subtitles for the current video using the YouTube API.
2. It extracts the default subtitle track (auto-generated or the first available).
3. In the **open-in-newtab** version, the subtitles are opened in a new tab for viewing.
4. In the **download** version, the subtitles are downloaded as an SRT file.
5. A spinner is displayed while the subtitles are being fetched.

## Caveats
- **Editing Polymer is horrible**: YouTube's Polymer elements can make dynamic content injection challenging. If any errors happen, please let me know.
- **Pop-up Blockers**: Ensure pop-ups are allowed for the download or new tab to work properly.
- **No Download (in open-in-newtab version)**: This version only opens subtitles in a new tab; it does not download them.

## Installation
1. Install Violentmonkey (or compatible userscript manager).
2. Add the script to your userscript manager.
3. Visit any YouTube video, click the button seen in the image above, and click the "Transcription" button to view or download subtitles.

## Credits
- Thanks to [Bret Donald](https://stackoverflow.com/questions/78081057/how-can-i-download-youtube-captions-using-javascript) for the solution that saved my life!
