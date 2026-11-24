# Hyper Arcade

## Live website

The public arcade website is available at:
https://georgebraxington.github.io/hyper-arcade/

## Put it on a website

`index.html` is the website's home page. It already includes the arcade styles,
games, and scripts, including the refreshed Snake, Pong, and Breakout graphics,
so it does not need a build step or extra files.

1. Upload `index.html` to a static website host.
2. Keep the filename `index.html` so it opens as the site's home page.
3. Open the website's HTTPS address and try the games on desktop and mobile.

Ask a parent or teacher to help choose a hosting service and review the site
before publishing it publicly.

## Important limits

- Player profiles, coins, scores, quest progress, game settings, and owner tools
  are saved in each visitor's browser. They are not shared between visitors or
  devices.
- Click the player button in the upper-right corner to open the full Player Hub
  in a side panel without leaving the arcade page. Friends & Profiles is near
  the top of that panel.
- Profiles & Friends lets people create nicknamed profiles and use the Add
  friend button beside a profile for local play on the same device. The button
  changes to Remove friend when connected. The multiplayer prompt only selects
  a local profile; it does not send an online invitation or find other website
  visitors. Use nicknames, not personal contact information.
- Players can download a private JSON backup from the Player Hub and restore it
  later in a browser that allows local storage. The backup includes player
  progress, quests, settings, and supported game records, but not Owner/Admin
  accounts or custom games. Keep the file private and do not upload it publicly.
- The Owner/Admin tools are a local convenience feature, not secure website
  accounts. Do not use them to protect private information or important data.
- Shared accounts, a real online leaderboard, and secure administration need a
  server and are not included in this static website.
- Online profiles, cross-device friend requests, and multiplayer invitations
  need a secure backend and are not included in this static website.

## Secure online accounts (future upgrade)

For a Vercel-hosted site, Supabase is a good next option to learn: it provides
sign-in and a database, while database security rules control what each role can
change. The current arcade is not connected to Supabase, so its local Admin
tools are still not secure online accounts.

Ask a parent or teacher to help create and configure a Supabase project before
connecting real player or Admin data. Never put a Supabase **service-role key**
or any other secret key in `index.html`; browser code can be seen by visitors.
