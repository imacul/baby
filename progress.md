Original prompt: Add more games for my nephew
Current prompt: Add a GitHub Actions upload speed test after switching router networks

## Notes
- Reworked the single-game page into a small game hub.
- Kept `index.html` as the deployment entrypoint.
- Left `baby_tap_pop_game.html` as a redirect so old links still land on the app.
- Added a manual GitHub Actions workflow at `.github/workflows/upload-speed.yml` that uploads a test payload and reports Mbps in the job summary.

## TODO
- Verify the new games in a browser.
- Push the updated files and redeploy to Vercel.
- If the balloons feel too fast or too small on mobile, tune their size and drift.
- Decide whether you want the upload test to run on a GitHub-hosted runner or a self-hosted runner on your own network. The current workflow measures the runner's network, not a home router directly.

## Gotchas
- The project depends on `Tone.js` from a CDN, so network access is required at runtime.
- Vercel should keep serving `index.html` at the root.
- A GitHub-hosted Actions runner will not measure your phone/router speed; it measures GitHub's cloud runner path.
