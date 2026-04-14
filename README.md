# AuRRa Read Me
Live: ria-bobiia.github.io/aurra

⚠️ Still in beta (actively working on recommendation accuracy and priority weighting).
- Claude's music knowledge is uneven for niche or non-English artists
- Key matching is approximate, not fully accurate

Paste a Spotify link. AuRRa reads the song's actual audio data (BPM, key, energy, mood, acousticness) and uses Claude to find songs that sound like it.

Process:
1. Connect your Spotify account via OAuth
2. Paste any Spotify track link
3. The app pulls the track's audio features from Spotify's API
4. Those features get sent to Claude with a structured prompt
5. Claude recommends 8 songs based on genre, key, BPM, texture, and energy with each recommendation linked directly to Spotify

Stack:
- Frontend - HTML, CSS, Vanilla JS
- Backend- Cloudflare Worker
- Auth - Spotify OAuth 2.0 with PKCE
- Music data - Spotify Web Dev API
- Recommendations - Anthropic Claude API

