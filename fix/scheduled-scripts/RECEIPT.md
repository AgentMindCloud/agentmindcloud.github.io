# Receipt — scheduled scripts as Grok Bot routines

Checked 2026-10-09 14:23:10 +07 (Asia/Ho_Chi_Minh). Quotes below were copied from the HTML bodies fetched at 2026-10-09 14:20:43 +07 and confirmed still HTTP 200 at 14:23:10 +07. Neither required URL redirected.

| URL | HTTP | Redirects | Final URL | ETag |
| --- | --- | --- | --- | --- |
| https://cursor.com/help/grok-bot/routines | 200 | 0 | https://cursor.com/help/grok-bot/routines | `"31bf03d49705927bcb0f6286605b4814"` |
| https://cursor.com/docs/grok-bot/computers | 200 | 0 | https://cursor.com/docs/grok-bot/computers | `"34437da4185f0bd92ba32f6844dfe4ae"` |
| https://agentmindcloud.github.io/fix/scheduled-scripts/ | 404 | 0 | same | — |
| https://agentmindcloud.github.io/fix/ | 200 | 0 | same | “More fixes” is present. `scheduled-scripts` is not linked. |

The computers URL is live. Its title is “Manage Grok Bot computers”. No replacement URL was needed. Sleep wording on that page is the automatic-termination FAQ, not a cron guide.

| Case | Grade | Evidence |
| --- | --- | --- |
| 1. Page returns 200 at the publish path and is linked from /fix/ | UNVERIFIED | Pending the publisher. At 2026-10-09 14:23:10 +07, `https://agentmindcloud.github.io/fix/scheduled-scripts/` and `.../index.html` returned HTTP 404, 0 redirects. `https://agentmindcloud.github.io/fix/` returned HTTP 200 and its “More fixes” line does not include this page. The file to copy is `fix/scheduled-scripts/index.html`. |
| 2. Every step cites routines or computers; both return 200; quotes match live wording | PASS | Both URLs HTTP 200, 0 redirects, at 14:20:43 +07 and again at 14:23:10 +07. Labels **When to run**, **Timezone**, and **Test** are on the live routines page. Cost note is live: “Each run spends usage, so a routine that runs often spends more than one that runs rarely. An hourly schedule, a short interval, or a Slack trigger on a busy channel can use a week of usage in a day.” Sleep line, from the computers FAQ: “No. The 30 days count from when the computer went to sleep after its last use. A computer that is awake, because a Bot is working or the member is using Grok Bot, is never terminated by this setting.” |
| 3. Desk walkthrough (no Grok Bot, no usage spent) | PASS | No routine was created and Test was not pressed. The page’s steps use When to run, Timezone, and Test as the desktop labels on the live routines page. Example path `~/scripts/report.sh` and the chat block are labeled Example. The page contains the exact sentence “Not yet run end to end on a Grok Bot”. It does not claim a tested output. |
| 4. No invented sleep timer or always-on setting; reliability is only a link | PASS | The page gives no sleep duration. The “30 days” sentence is quoted as the inactive-termination count and is labeled as such. The page says the computers page does not describe a setting that keeps the computer awake. Misfires go to `https://agentmindcloud.github.io/fix/` in one paragraph. Missed-wake, skip, and catch-up steps are not repeated. |
| 5. Exactly one @jana_solos CTA | PASS | One anchor, text “Follow @jana_solos for Grok Bot fixes”, href `https://x.com/jana_solos`. The handle appears once. |
| 6. (removed 2026-10-09) | — | Source-ask link and reply draft removed from the public page. |

Case 3 fail rule in force: the page claims a tested output it did not get. It does not. The example output caption says it was not captured from a Grok Bot chat.
