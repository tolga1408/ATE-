# 🔥 ATEŞ — Hand on Fire

A real-time, browser-based card game where **every card in your hand is burning**.
Play fast, chain combos, survive as long as you can. Built as a single
self-contained `index.html` — no frameworks, no backend, no build step.

> **ATEŞ** (Turkish for "Fire") — inspired by the Cardburners mechanic.

---

## 🎮 How to Play

- Start with **5 cards** and **3 lives** (🔥🔥🔥).
- Every card has a **fuse bar** that drains in 5–10 seconds.
- **Click / tap** a card to play it before it burns out.
- Let it burn → **lose a life**.
- Play 3+ cards within 2 seconds → **2× COMBO** multiplier.
- Play a card with **< 1 s** left on its fuse → **🔥 FIRE CHAIN** (double points).
- Every 30 seconds, fuses get shorter → game gets harder.

### Card Types
| Card | Effect |
|------|--------|
| **1–9** | Number cards. Points = face value. |
| 🔥 **Fire** | Instantly refills ALL fuse timers. |
| ❄️ **Freeze** | Pauses all fuses for 3 seconds. |
| 💣 **Bomb** | Only 3 seconds to play, or lose a life immediately. |
| ⭐ **Star** | 15 points + auto-triggers combo. |

Press **Space** to pause. Score saves locally to `localStorage`.

---

## 🚀 Deploy to GitHub Pages in Under 5 Minutes

You only need a free GitHub account.

### Step 1 — Create the repository
1. Sign in at <https://github.com>.
2. Click **+ → New repository**.
3. Name it (for example) **`ates`** or **`ATE-`** to match the original.
4. Set it to **Public**, check **"Add a README"** if you want, then **Create**.

### Step 2 — Upload `index.html`
1. Click **Add file → Upload files**.
2. Drag `index.html` (and this `README.md`) into the browser.
3. Click **Commit changes**.

> Or via CLI:
> ```bash
> git clone https://github.com/<your-user>/ates.git
> cd ates
> # copy index.html and README.md into this folder
> git add .
> git commit -m "Add ATEŞ game"
> git push origin main
> ```

### Step 3 — Enable GitHub Pages
1. Open the repo → **Settings → Pages**.
2. Under **Build and deployment → Source**, pick **Deploy from a branch**.
3. Choose **Branch: `main`** and folder **`/ (root)`** → **Save**.
4. Wait ~30–60 seconds. GitHub will show a green box with your URL, e.g.:
   ```
   https://<your-user>.github.io/ates/
   ```
5. Open that URL — your game is live. 🔥

### Step 4 — (Optional) Custom domain
- Add a `CNAME` file containing your domain (e.g. `ates.example.com`).
- Add a `CNAME` DNS record at your registrar pointing to `<your-user>.github.io`.

---

## 🌐 Where to Submit ATEŞ After Deployment

Once your GitHub Pages URL is live, submit the game to these **5 portals**:

1. **[CrazyGames](https://developer.crazygames.com/)** — Largest HTML5 portal, revshare on ads. Submit at `developer.crazygames.com`.
2. **[Poki](https://developers.poki.com/)** — Major casual portal; needs a 2-line SDK include (already noted as a `TODO` in the code).
3. **[itch.io](https://itch.io/game/new)** — Indie-friendly, instant publish, no review queue. Upload the ZIP or link the GitHub Pages URL.
4. **[Newgrounds](https://www.newgrounds.com/projects/games)** — Classic browser-game audience, great for niche traction.
5. **[GameDistribution](https://gamedistribution.com/)** — Distributes your game across thousands of partner sites with revshare.

**Bonus tier (worth trying):**
- **Kongregate** (`kongregate.com/games_for_your_site`)
- **Y8 / Y8 Studio**
- **Armor Games Studios** (more curated)
- **Reddit**: `r/incremental_games`, `r/WebGames`, `r/playmygame`

---

## 💰 Monetization TODOs (in code)

Look for these comments in `index.html` — they're hooks for the next steps:

```js
// TODO: Add Google AdSense leaderboard banner below game container
// TODO: Add "Remove Ads" button linking to /premium
// TODO: Submit to CrazyGames API for portal integration
// TODO: Add Poki SDK (2 lines) for Poki.com submission
```

For Poki, you literally only need:

```html
<script src="//game-cdn.poki.com/scripts/v2/poki-sdk.js"></script>
<script>PokiSDK.init().then(() => PokiSDK.gameLoadingFinished());</script>
```

---

## 🛠 Tech

- **Pure HTML + CSS + Vanilla JS** — no frameworks, no npm, no build.
- `requestAnimationFrame` for smooth fuse-bar animation.
- All CSS animations and DOM elements — no `<canvas>`.
- High score via `localStorage`.
- Web Share API with clipboard fallback for the share button.

## 🧩 Config

Tweak game feel at the top of the inline `<script>`:

```js
const CONFIG = {
  gameName: "ATEŞ",
  startLives: 3,
  startFuseMin: 5,
  startFuseMax: 10,
  comboWindow: 2000,
  difficultyInterval: 30000,
  fuseReductionPerLevel: 0.5,
};
```

## 📜 License

MIT — Do whatever you want. A "made with ATEŞ" mention is appreciated. 🔥
