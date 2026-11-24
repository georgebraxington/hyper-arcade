# Hyper Arcade Project Journal

This journal keeps the project's important context in the workspace so it can
be picked up in another session. Update it when a meaningful feature or
technical decision changes.

## How to work with the user

- The user is learning to code. Explain changes in clear, encouraging language,
  define unfamiliar terms, and include a useful lesson when describing how
  something works.
- Prefer small, careful improvements and preserve existing features. Do not
  overwrite or discard earlier work without a clear reason.
- Keep the user safe when discussing publishing, accounts, or personal data;
  suggest asking a parent or teacher for help when appropriate.

## Project shape

- Hyper Arcade is a static website built as a single HTML file with inline CSS
  and JavaScript. It has no build step or backend.
- `Hyper_Arcade_One_Time_Codes_Upgraded.html` is the editable main source.
- `index.html` is the static-host entry point and should be copied from the
  source after source changes. Verify that both files have matching SHA-256
  hashes before finishing.
- `README.md` explains how to publish the site and its important limitations.

## Current features and boundaries

- Player profiles, scores, coins, quests, settings, and owner tools are stored
  in the visitor's browser. They are not shared across visitors or devices.
- The Player Hub opens as a side panel. Its Friends & Profiles section is near
  the top.
- Profiles have direct Add friend / Remove friend controls, along with View and
  Switch actions. Local friends can be selected in supported multiplayer
  prompts, but this does not create online invitations or find other visitors.
- The local profile directory uses the `hyperArcadeLocalProfilesV1` local
  storage key and supports up to 12 profiles.
- Owner/Admin tools are not secure online accounts. Real shared accounts,
  online friends, and secure administration need a backend.

## Recent work

- The Player Hub was moved into an accessible sidebar, and Friends & Profiles
  was made easier to find.
- Profile rows gained direct Add friend / Remove friend buttons while keeping
  the existing View, Switch, and profile-detail actions.
- The latest browser checks covered adding/removing a friend, friend counts,
  the View action, and a phone-sized layout. `index.html` was copied from the
  source and the files' SHA-256 hashes matched.
- For browser tests, use a temporary localStorage fixture for profiles instead
  of relying on native `prompt()`, which is unsupported in the browser test
  environment.
