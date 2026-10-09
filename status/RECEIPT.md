# Receipt — Grok Bot public status checker

Build date: 2026-10-09  
Check window: 2026-10-09 08:07:52–08:09:53 Asia/Ho_Chi_Minh (ICT, UTC+7)  
Artifact: `status/index.html` (plain static HTML, no build step)  
Ask: https://x.com/MajorBaguette/status/2108237106061410766

The published URL and the hub index are not in this workspace. The publisher copies `status/index.html` into `status/` on AgentMindCloud/agentmindcloud.github.io and adds the hub link.

## Grades

| # | Condition | Grade | Evidence |
| --- | --- | --- | --- |
| 1 | `https://agentmindcloud.github.io/status/` returns HTTP 200 and answers “Is Grok Bot down?” from the live Cursor Status Grok Bot component (linked and quoted). | UNVERIFIED | Live-200 of the published URL is pending publish. The local page is titled “Is Grok Bot down?” and quotes the component. Exact quote and timestamp are below. |
| 2 | Probe table includes the four URLs; each was fetched on the build date; codes match a second pass. | PASS | Four URLs fetched 2026-10-09. Pass at 08:07:52 ICT and two passes at 08:09:53 ICT all returned HTTP 200 with no redirect. Raw codes below. |
| 3 | If Grok Bot is Operational, the page does not claim a platform outage and points personal failures to `/fix/`. | PASS | Page answer is “No.” State quoted as Operational. Section “Platform vs personal” says a personal failure is not a platform outage and links `https://agentmindcloud.github.io/fix/`. |
| 4 | Page states it cannot see one account, one computer, or one bot. | PASS | Section “What this page cannot see” says it cannot see one account, one computer, or one bot runner. |
| 5 | Hub index links to `/status/`. | UNVERIFIED | Hub-link check is pending publish. This workspace is the status page only. The hub index of agentmindcloud.github.io was not edited. |
| 6 | Exactly one `@jana_solos` CTA on `/status/`. | PASS | One anchor, text “Follow @jana_solos for Grok Bot fixes”, href `https://x.com/jana_solos`. No other `jana_solos` or `x.com` link in the file. |
| 7 | Handover reply template is on the page and names both `/status/` and `/fix/`. | PASS | Blockquote “Reply you can send” contains the packet template, including `https://agentmindcloud.github.io/status/` and `https://agentmindcloud.github.io/fix/`. |
| 8 | A second operator can open `/status/` plus status.cursor.com and tell @MajorBaguette whether the platform is down. | PASS | The page answers “No.”, quotes Operational, links `https://status.cursor.com/`, links the latest resolved incident that lists Grok Bot, and says to trust the live Cursor page if they differ. Opening the public `/status/` URL itself is the publisher’s live-200 check (condition 1). |

## Exact status quote

Fetched from the live Grok Bot row on https://status.cursor.com/ during the check window. The status page was fetched again at 08:09:53 ICT (HTTP 200, `Content-Length: 124712`, same length as the 08:07:52 fetch).

Visible text on the Grok Bot component:

```
Operational
```

Surrounding markup:

```html
<div data-component-id="sm5wkcnqkvr9"
     class="component-inner-container status-green showcased"
     data-component-status="operational"
     data-js-hook="">

   <span class="name" role="heading" aria-level="2">
      Grok Bot
   </span>

  <span class="component-status" title="">
    Operational
  </span>

  <button type="button" class="tool icon-indicator fa fa-check status-icon-button" aria-label="Operational" data-js-hook="tooltip" data-original-title="Operational"></button>
```

Component object from https://status.cursor.com/api/v2/summary.json (HTTP 200). Page `updated_at` was `2026-10-09T00:11:35.742Z`. Page status was `{"indicator": "none", "description": "All Systems Operational"}`.

```json
{
  "id": "sm5wkcnqkvr9",
  "name": "Grok Bot",
  "status": "operational",
  "created_at": "2026-08-17T16:57:56.065Z",
  "updated_at": "2026-10-08T20:51:06.836Z",
  "position": 14,
  "description": null,
  "showcase": true,
  "start_date": "2026-08-10",
  "group_id": null,
  "page_id": "0tp9ssgtptvs",
  "group": false,
  "only_show_if_degraded": false
}
```

Plain words: **Operational**. Not Degraded, Outage, or Maintenance.

No open incident. https://status.cursor.com/api/v2/incidents/unresolved.json returned:

```json
{"page":{"id":"0tp9ssgtptvs","name":"Cursor","url":"https://status.cursor.com","time_zone":"Etc/UTC","updated_at":"2026-10-09T00:11:35.742Z"},"incidents":[]}
```

Scheduled maintenances count: 0.

Latest resolved incident whose component list includes Grok Bot (there is no newer one in the incidents feed):

- Name: Elevated errors affecting Opus 5.5
- URL: https://status.cursor.com/incidents/25l5bm6rdrb6 (HTTP 200; title “Cursor Status - Elevated errors affecting Opus 5.5”)
- id: `25l5bm6rdrb6`
- status: `resolved`
- impact: `minor`
- components: Automations, CLI, Cloud Agents, IDE, Grok Bot
- created_at: `2026-10-08T19:52:44.876Z`
- resolved_at: `2026-10-08T20:51:06.871Z`
- latest update body: `This incident has been resolved.`
- shortlink: https://stspg.io/g415ws29757p

## Raw probe codes

User-Agent: `AgentMindCloud-status-checker/1.0 (public snapshot)`. Each final URL matched the requested URL. No `redirect_url`.

### Pass 1 — 2026-10-09 08:07:52 Asia/Ho_Chi_Minh (`curl -L -w`)

| URL | HTTP | Content-Type | Size | Final URL |
| --- | --- | --- | --- | --- |
| https://status.cursor.com/ | 200 | text/html; charset=utf-8 | 124712 | https://status.cursor.com/ |
| https://cursor.com/help/grok-bot/faqs | 200 | text/html; charset=utf-8 | 269788 | https://cursor.com/help/grok-bot/faqs |
| https://docs.x.ai/grok-bot/overview | 200 | text/html; charset=utf-8 | 260006 | https://docs.x.ai/grok-bot/overview |
| https://agentmindcloud.github.io/fix/ | 200 | text/html; charset=utf-8 | 33446 | https://agentmindcloud.github.io/fix/ |

Same pass, official Statuspage JSON used only to read Cursor’s own feed (not served by this page):

| URL | HTTP |
| --- | --- |
| https://status.cursor.com/api/v2/summary.json | 200 |
| https://status.cursor.com/api/v2/components.json | 200 |
| https://status.cursor.com/api/v2/incidents.json | 200 |
| https://status.cursor.com/api/v2/incidents/unresolved.json | 200 |
| https://status.cursor.com/api/v2/scheduled-maintenances.json | 200 |

### Pass 2 and pass 3 — 2026-10-09 08:09:53 Asia/Ho_Chi_Minh

Two back-to-back fetches. Both matched pass 1.

| URL | Pass 2 | Pass 3 | Content-Type | Content-Length |
| --- | --- | --- | --- | --- |
| https://status.cursor.com/ | 200 | 200 | text/html; charset=utf-8 | 124712 |
| https://cursor.com/help/grok-bot/faqs | 200 | 200 | text/html; charset=utf-8 | 269788 |
| https://docs.x.ai/grok-bot/overview | 200 | 200 | text/html; charset=utf-8 | (no Content-Length; body received, title “Grok Bot \| SpaceXAI Docs”) |
| https://agentmindcloud.github.io/fix/ | 200 | 200 | text/html; charset=utf-8 | 33446 |

Page titles read from those responses:

- https://status.cursor.com/ — `Cursor Status`
- https://cursor.com/help/grok-bot/faqs — `Grok Bot FAQs | Cursor Docs`
- https://docs.x.ai/grok-bot/overview — `Grok Bot | SpaceXAI Docs`
- https://agentmindcloud.github.io/fix/ — `Grok Bot stuck? A fix guide from Cursor's live help`

## Not done

No X post. No pull request into Cursor or xAI repositories. No payment. No new bot. No invented outage. No status API of our own.
