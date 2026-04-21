# Formation 2026 Goal Tracker

Shared goal dashboard for Andre Barros and Matias (Formation DS · FanDuel).

## Opening the tracker

Navigate to the GitHub Pages URL shared with you. No install required.

## First-time sync setup (both users)

You need a GitHub Personal Access Token to share goal data via a private Gist.

1. Go to **GitHub → Settings → Developer Settings → Fine-grained tokens → Generate new token**
2. Set expiry to 1 year
3. Under **Permissions → Account permissions → Gists** → set to **Read and write**
4. Copy the token

5. In the tracker, click the **⚙ gear icon** (top right)
6. Enter your **display name** and paste your **PAT**
7. **Andre only:** click **New Gist** to create the shared store → copy the Gist ID → send to Matias via Teams
8. **Matias:** paste the Gist ID Andre sent you, then click **Save & sync**

The tracker will now sync between your devices every 30 seconds. A toast notification will appear when the other person saves changes.

## Figma Make design source

See `figma-make-prompt.md` for instructions on generating the companion Figma Make file.
Once generated, paste the URL into the `FIGMA_MAKE_URL` constant at the top of `index.html`.
