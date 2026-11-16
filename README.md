# YT Freedom Player

A lightweight, responsive video interface hosted on GitHub Pages. It uses YouTube's official embedded player.

## Features

- Open a YouTube video using its URL or 11-character video ID.
- Responsive embedded player.
- Local recent-history and favorites stored in the current browser.
- Optional Google sign-in button using Google Identity Services.

## Google sign-in setup

1. Create an OAuth 2.0 **Web application** client in Google Cloud Console.
2. Add this exact authorized JavaScript origin: `https://10574084-cmd.github.io`
3. Copy the OAuth client ID (it ends in `.apps.googleusercontent.com`).
4. In `index.html`, replace `PON_AQUI_TU_GOOGLE_OAUTH_CLIENT_ID` in `CLIENT_ID` with that client ID.
5. Commit the change and open the GitHub Pages site.

Never put a client secret, password, or private key in this repository. This sign-in only identifies the user to this app; it does not grant YouTube API permissions or sign the user into YouTube.

## Important limitations

- Video playback is provided by YouTube's official embed. Videos that disallow embedding, require age/account verification, or are unavailable in a region/network may not play here.
- This project does not proxy YouTube traffic or bypass school, network, account, or platform restrictions.
- Search, comments, likes, subscriptions, and posting comments are not implemented. Those require approved YouTube API access and the appropriate user authorization.
- History and favorites are local to this browser and are not synced between devices.

## GitHub Pages

The repository's Pages workflow/deployment settings can publish `index.html` from the configured branch. Keep the existing Actions workflow intact.
