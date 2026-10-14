# hype-train-rewards

A clickable prototype of **creator rewards on the Twitch mobile Hype Train**. Streamers attach their own challenges to Hype Train levels (for example, "at level 5 I drop all my guns in Fortnite"), viewers see what's next and push the train to unlock it, and the streamer marks rewards done.

Everything is simulated in the browser. Nothing connects to Twitch and no payments happen.

## Run it

It's plain HTML, CSS and JavaScript with no build step.

- Open `index.html` in a browser, or
- Serve the folder: `python3 -m http.server 8000`, then visit http://localhost:8000

## What's here

| File | What it is |
| --- | --- |
| `index.html` | The prototype: a phone with Viewer and Streamer views, a stream simulator, and the creator dashboard for editing rewards |
| `docs/spec.html` | The product spec and static mockups (setup flow, viewer screens, completion flow, edge cases, design system changes) |

## Things to try

1. **Viewer:** tap the Hype Train bar, tap a reward for details, then Gift or tap the Bits icon in chat to push the train.
2. **Streamer:** switch the phone to Streamer and tap Mark done. The viewer's pinned notice turns into "Reward done".
3. **Creator:** end the train, then edit rewards, pick a difficulty (Easy, Normal, Hard), or set how many subs each level takes. The phone updates live. Settings are saved in your browser's localStorage.

## Design

Styled with the Midnight Rail Hype Train design system (Inter, dark-only). Components used: HypeBar, HypePanel, UnlockCard, LeaderboardStrip, NoticeBar, ChatInputBar, BottomSheet, GiftTierCard, TierSelector. New pieces this feature adds are listed in `docs/spec.html` under "Design system changes".
