# Receipt — Grok Bot email: what the docs say today

Build date: 2026-10-09, Asia/Ho_Chi_Minh.
Page file: `fix/email/index.html`.
Shape: docs-gap. No official Grok Bot email page returned HTTP 200.
No email was sent or received. No usage was spent. No X post, pull request, or payment was made.

## Step 0

First-hop HTTP codes, recorded in Asia/Ho_Chi_Minh:

| URL | When | HTTP |
| --- | --- | --- |
| `https://cursor.com/help/grok-bot/email` | 2026-10-09 15:51:21 +07 | 404 |
| `https://cursor.com/docs/grok-bot/email` | 2026-10-09 15:51:21 +07 | 404 |
| `https://cursor.com/help/grok-bot/inbox` | 2026-10-09 15:51:21 +07 | 404 |
| `https://cursor.com/help/grok-bot` | 2026-10-09 15:51:21 +07 | 307 to `/help` |
| `https://cursor.com/help` | 2026-10-09 15:51:50 +07 | 200 |
| `https://cursor.com/docs/grok-bot` | 2026-10-09 15:51:22 +07 | 200 |

Result: no official email page. The help index and the docs index do not link a Grok Bot email article. The help index’s only path containing “email” is `https://cursor.com/help/account-and-billing/change-email` (HTTP 200 at 2026-10-09 15:55:24 +07), which is the Cursor account email address.

Web search, same day, for an official Cursor Grok Bot email doc: two searches via the Cursor web search tool during 15:51–15:53 +07. Results were live help and docs pages (get help, FAQs, sign-in, how-tos, connect plugins, get started, computers). None was `cursor.com/help/grok-bot/email` or `cursor.com/docs/grok-bot/email`. Exa’s search tool returned a rate-limit error. Bright Data’s search tool returned HTTP 401, so it contributed no results.

Pages quoted on the how-to, each HTTP 200 when fetched:

| Page | When | HTTP |
| --- | --- | --- |
| `https://cursor.com/help/grok-bot/routines` | 2026-10-09 15:51:50 +07 | 200 |
| `https://cursor.com/docs/grok-bot/work` | 2026-10-09 15:51:50 +07 | 200 |
| `https://cursor.com/help/grok-bot/get-help` | 2026-10-09 15:51:50 +07 | 200 |
| `https://cursor.com/docs/grok-bot/settings` | 2026-10-09 15:51:50 +07 | 200 (visible text has no “email”) |
| `https://cursor.com/help/grok-bot/connect-plugins` | 2026-10-09 15:53:28 +07 | 200 |
| `https://cursor.com/help/grok-bot/faqs` | 2026-10-09 15:53:28 +07 | 200 |
| `https://cursor.com/help/account-and-billing/change-email` | 2026-10-09 15:55:24 +07 | 200 |
| `https://cursor.com/help/grok-bot/onboarding` | 2026-10-09 15:56:04 +07 | 200 |
| `https://cursor.com/docs/grok-bot/use-cases` | 2026-10-09 15:56:04 +07 | 200 |

Cited quote URLs were requested again at 2026-10-09 15:57:15 +07 and each returned 200, including `https://x.com/jana_solos` and `https://x.com/petergyang/status/2108412799684915576`.

`https://agentmindcloud.github.io/fix/` returned 200 at 2026-10-09 15:53:28 +07. Its “More fixes” line does not include this page. `https://agentmindcloud.github.io/fix/email/` returned 404 at that same time.

## Grades

| Case | Grade | Evidence |
| --- | --- | --- |
| 1. `/fix/email/` returns 200 and is linked from `/fix/` | UNVERIFIED | Pending the publisher. The live URL returned 404 at 2026-10-09 15:53:28 +07, and the live `/fix/` page does not link it. The file to copy is `fix/email/index.html`. |
| 2. Step 0 is recorded with the date and its result | PASS | The page’s “Step 0, the check” section records 2026-10-09, the 404s, the 307, the index 200s, and the result that no official email page was found. |
| 3. Every factual line quotes or links a live official page that returned 200 | PASS | Routine trigger, chat setup, email-file attachments, Gmail plugin behavior, onboarding, starter prompts, account email, and support contact are each inside a quotation whose footer links the page fetched at HTTP 200. The 404 URLs are plain text, not links. |
| 4. No addresses, setup screens, or send/receive behavior unless an official page states them | PASS | The support address `hi@cursor.com` appears only inside the Get help quotation. Gmail “draft and send,” one mailbox, disconnect, and the Plugins sidebar sentence appear only inside Connect plugins and Onboarding quotations. Starter-prompt lines about drafting and not sending appear only inside Use cases quotations. The page gives no Bot email address of its own. |
| 5. The page carries the honest end-to-end statement | PASS | The page contains the exact sentence “Not yet run end to end: no email was sent or received while building this page.” |
| 6. Exactly one @jana_solos CTA, and the outage is not covered | PASS | The anchor text “Follow @jana_solos for Grok Bot fixes” and the URL `https://x.com/jana_solos` each appear once. The page text has no “174136”. |
| 7. A desk reviewer can explain what is documented and what is not | PASS | The opening line says Cursor has not published a Grok Bot email help page. The body quotes the routine trigger, email-file attachments, the Gmail plugin, the use-case prompts, and the account-email pages, then tells the reader to ask the Bot in chat and, if mail seems broken, to use Get help. |

## What a reviewer can tell @petergyang

Cursor has not published a help page at the email URLs. A routine’s published description includes an email among the events that can start it, and the published setup line is to ask the Bot in chat. A chat can take email files as attachments. A connected Gmail plugin, on the Connect plugins page, can search and read mail, draft and send, and apply labels, on one mailbox at a time. Starter prompts on the use-cases page mention connecting email and returning drafts. The account email address is a separate page, and it cannot be changed. Support, if mail seems broken, is the Get help page.
