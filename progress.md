Original prompt: Add more games for my nephew

## Notes
- Reworked the single-game page into a small game hub.
- Kept `index.html` as the deployment entrypoint.
- Left `baby_tap_pop_game.html` as a redirect so old links still land on the app.

## TODO
- Verify the new games in a browser.
- Push the updated files and redeploy to Vercel.
- If the balloons feel too fast or too small on mobile, tune their size and drift.

## Gotchas
- The project depends on `Tone.js` from a CDN, so network access is required at runtime.
- Vercel should keep serving `index.html` at the root.
