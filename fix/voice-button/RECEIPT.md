# Receipt — Grok Bot voice-chat action-button setup

Checked 2026-10-09, Asia/Ho_Chi_Minh. Page: `fix/voice-button/index.html`. Publish path (not this repo): `https://agentmindcloud.github.io/fix/voice-button/`.

Wording is from the live pages fetched that morning. Where an earlier summary differed, the page follows the live sentence and the difference is noted below.

## Grades

| Case | Grade | Evidence |
| --- | --- | --- |
| 1. Live at the publish path and linked from `/fix/` | UNVERIFIED | Pending publish. This file is the page the publisher copies. It is not on GitHub Pages yet. |
| 2. Every step links Apple's Action Button guide or Cursor's voice-chat help; each link is HTTP 200 and matches live wording | PASS | Fetches below. Update steps use the “How do I update Grok Bot?” section the voice-chat page links to. Quotes in the HTML match those fetches. |
| 3. Says a one-press voice call isn't documented; no invented deep link or URL scheme | PASS | The page says “A one-press voice call isn't documented” in the lede and again under “The closest path.” The HTML has no `grok://`, custom scheme, or deep link. |
| 4. On-device Shortcuts check recorded, or the unchecked statement with no Shortcuts step | PASS | The page states, exactly: “Not yet checked on a device: we have not confirmed whether Grok Bot exposes Shortcuts actions”. It gives no Shortcuts-app step. |
| 5. A reader can follow only the page from the Action Button to a voice chat | PASS | Desk-verified, not device-verified. Walkthrough below. No iPhone was available. |
| 6. (removed 2026-10-09) | — | Source-ask link and reply draft removed from the public page. |
| 7. Exactly one CTA, “Follow @jana_solos for Grok Bot fixes”, linking `https://x.com/jana_solos` | PASS | That string and `https://x.com/jana_solos` each appear once, on the same link. `/fix/` adding a link to this page, while keeping its own single CTA, is the publisher's edit and is still outstanding with case 1. |

## HTTP evidence

| Page | Time (Asia/Ho_Chi_Minh) | HTTP |
| --- | --- | --- |
| `https://cursor.com/help/grok-bot/voice-chat` | 2026-10-09 09:50:31 | 200 |
| `https://cursor.com/help/grok-bot/mobile` | 2026-10-09 09:50:31 | 200 |
| `https://support.apple.com/guide/iphone/use-and-customize-the-action-button-iphe89d61d66/ios` | 2026-10-09 09:50:31 | 200 |
| `https://cursor.com/help/grok-bot/how-to` (anchor `#how-do-i-update-grok-bot`, the link on the voice-chat page) | 2026-10-09 09:51:16 | 200 |
| `https://cursor.com/changelog` (linked from the update answer's word “changelog”) | 2026-10-09 09:53:00 | 200 |
| `https://agentmindcloud.github.io/fix/voice-button/` | 2026-10-09 09:53:00 | 404 |
| `https://agentmindcloud.github.io/fix/` | 2026-10-09 09:53:00 | 200, and the body does not contain `voice-button` |

## Live wording quoted

### Voice chat — `https://cursor.com/help/grok-bot/voice-chat` — 200 at 09:50:31

How do I start a voice chat?

> Open the chat with the Bot.
> Leave the message box empty.
> Choose Start voice chat. It is the waveform button in the message box.
> Allow microphone access if your computer or phone asks.
> The call shows Connecting… on desktop or Calling… on the phone, then the Bot starts talking.
> Start voice chat shows only when the message box is empty. If the box is empty and you still don't see it, update Grok Bot. See How do I update Grok Bot?

The “How do I update Grok Bot?” link target in the HTML is `/help/grok-bot/how-to#how-do-i-update-grok-bot`.

What can I do during a voice chat? (limit)

> Only one voice chat runs at a time. If you start another one, Grok Bot asks End the current voice chat? Choose End and Chat to switch.

How is a voice chat different from voice typing?

> Voice typing turns your speech into text in the message box. You read it, edit it, and send it like any other message. The Bot replies in text.
> On desktop, choose Start voice input in the message box. You can also press Cmd+D on Mac or Ctrl+D on Windows and Linux, or hold the keys while you talk.
> On the phone, tap Start dictation.
> A voice chat is a live conversation. The Bot answers out loud and keeps listening until you hang up.
> On the phone, stop dictation before you start a voice chat.

The key mark is a `<kbd>`: the Mac slot is `Cmd+D`, the alternate slot is `Ctrl+D`, then the sentence continues “on Mac or” and a second `<kbd>` shows `Ctrl+D` “on Windows and Linux”.

Can I voice chat in a group chat?

> No. Voice chat works with one Bot at a time. Open that Bot's own chat to start a call.
> Voice chat isn't available with a teammate's Team Bot.

The article text contains no “Action button”, no “Action Button”, no “widget”, no “deep link”, and no URL scheme. The only “shortcut” strings are `<link rel="shortcut icon">`.

### Mobile — `https://cursor.com/help/grok-bot/mobile` — 200 at 09:50:31

> Use Grok Bot on your phone with the same account and cloud computer as desktop. Grok Bot is available on iOS and Android.
> Install the current Grok Bot mobile app from the App Store on iOS or Google Play on Android.
> Sign in on mobile with the same Cursor account you use on desktop or web.

The article text contains no Action Button, no Shortcuts steps, no widget, and no “Start voice chat”. The only “shortcut” strings are the favicon link.

### Action Button — Apple — 200 at 09:50:31

> On supported models, iPhone has an Action button in place of the Ring/Silent switch. You can choose which function you want the Action button to perform when you press it.
> To perform the action assigned to the Action button, press and hold the Action button.
> Go to the Settings app on your iPhone.
> Tap Action Button.
> To choose an action (like Silent Mode), swipe to the action you want to use—its name appears below the dots.
> If there are additional options for the selected action, the Menu button appears below the action; tap it to see the list of options.
> For the Controls, Shortcut, and Accessibility actions, you need to tap the button below the action and select a specific option—otherwise the Action button does nothing.
> Shortcut: Open an app or run your favorite shortcut.

“the Menu button” is the `alt` of the icon that sits in that sentence (`alt="the Menu button"`). “Go to the Settings app” is followed by a Settings-app icon, then “on your iPhone.”

### How do I update Grok Bot? — 200 at 09:51:16

> The desktop app checks for updates on its own. When one is ready, the account menu shows New update available. Choose Install, then Restart to update. Your Bots keep working in the cloud while the app restarts.
> To check yourself, open Settings, go to Updates, and choose Check for Updates. If an update is ready, choose Restart to Update. Automatic Updates installs updates while you're away.
> Phone updates come from the App Store or Google Play. Product changes are listed on the changelog.

The changelog href on that page is `https://cursor.com/changelog`, HTTP 200 at 09:53:00.

## Where the live pages differ from the earlier summary

- The summary said “press.” Apple's live guide says “press and hold the Action button.”
- The action that can open an app is named Shortcut: “Open an app or run your favorite shortcut.” Apple does not name Grok Bot.
- The voice control is “Choose Start voice chat. It is the waveform button in the message box.” It “shows only when the message box is empty.”
- Desktop keys are “Cmd+D on Mac or Ctrl+D on Windows and Linux” for Start voice input. The page separates that from a voice chat, which “answers out loud and keeps listening until you hang up.”
- Limits, in the live sentences: “Only one voice chat runs at a time.” “No. Voice chat works with one Bot at a time.” “Voice chat isn't available with a teammate's Team Bot.”

## Case 5 desk walkthrough

Desk-verified, not device-verified. No iPhone in this build.

1. Apple: Settings → Action Button → swipe to Shortcut → tap the button below the action and select the option that opens the Grok Bot app. Quoted from the Action Button guide.
2. Apple: press and hold the Action button. That performs the assigned action (open the app). It is not a voice call.
3. Cursor: “Open the chat with the Bot.” “Leave the message box empty.” “Choose Start voice chat. It is the waveform button in the message box.” “Allow microphone access if your computer or phone asks.” The phone then shows “Calling…”.
4. If the waveform button is missing with an empty box, update from the App Store, as “Phone updates come from the App Store or Google Play.”

That is Action Button press (Apple: press and hold), then open the Bot, then Start voice chat.

## Case 1 detail

UNVERIFIED pending publish. At 2026-10-09 09:53:00 +07, `https://agentmindcloud.github.io/fix/voice-button/` returned HTTP 404. `https://agentmindcloud.github.io/fix/` returned HTTP 200 and its HTML did not contain `voice-button`. The publisher copies this page into `fix/voice-button/` and links it from `/fix/` without adding a second CTA there.
