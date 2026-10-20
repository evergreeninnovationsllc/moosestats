[README.md](https://github.com/user-attachments/files/33741100/README.md)
# Interactive Hockey Player Roster

This is a standalone roster component designed to be linked from or embedded in an existing Canva Website Editor site.

## Files
- `index.html` — responsive dark hockey roster with search, position filters, and click-to-expand player profiles.
- `players.json` — sample roster data. Replace the sample players with your 30–60 real players.

## Add or update players
Edit `players.json`. Keep the same field names:
- `id`: unique identifier, such as `player-04`
- `number`, `name`, `position`
- `shoots`, `height`, `weight`, `hometown`
- `photo`: full public HTTPS URL to a player headshot, or `""` for initials placeholder
- `bio`: player biography
- `season`: any key/value stats you want to show
- `career`: any key/value stats you want to show

Example:
{
  "id": "player-04",
  "number": 24,
  "name": "Casey Example",
  "position": "F",
  "shoots": "R",
  "height": "5'11\"",
  "weight": "175 lb",
  "hometown": "Detroit, MI",
  "photo": "https://your-image-host.example/player24.jpg",
  "bio": "A fast forward with a strong two-way game.",
  "season": {"GP": 32, "G": 14, "A": 20, "PTS": 34, "PIM": 12},
  "career": {"GP": 65, "G": 25, "A": 37, "PTS": 62}
}

You can use different stats for goalies and skaters. The three sample players are only demo data. Use real, public HTTPS image URLs for photos.

## Publish with GitHub Pages
1. Sign in to GitHub and create a repository, e.g. `team-roster`.
2. Upload both `index.html` and `players.json` to the top level of the repository.
3. Open repository **Settings → Pages**.
4. Under build/deployment, select **Deploy from a branch**, choose `main` and `/(root)`, then save.
5. Wait for publishing to finish. GitHub will show the public site URL in the Pages settings. It will usually resemble `https://YOUR-USERNAME.github.io/team-roster/`.
6. Open that URL directly and test searching, filtering, and expanding cards.

Important: GitHub Pages sites are public. Do not put private, confidential, or sensitive information in the files.

## Connect it to Canva
Recommended first: add a button or roster link in Canva that opens the hosted roster URL. This is the most reliable route and preserves the rest of your Canva site.

If you want the roster to appear inside a Canva page:
1. Open your Canva website design and navigate to the roster page.
2. Check whether your editor offers **Apps → Embeds** or an embed option that accepts the published roster URL.
3. Paste the public HTTPS roster URL and publish a test copy.
4. Verify on desktop and mobile. Canva may not allow arbitrary webpages to be embedded in every website design, and embedded content can have height/scroll limitations. If it does not work, use a prominent button/link to open the roster as a separate page.

## Local preview
The page fetches `players.json`, so preview it using a local web server rather than opening `index.html` directly. If you have Python installed, run `python3 -m http.server 8000` from this folder, then visit `http://localhost:8000`.
