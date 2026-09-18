# Waitlist inbox — LIVE on production

**Time (Asia/Hebron / IDT):** 2026-09-18 ~10:52 IDT  
**Agent role:** executor subagent (waitlist ship)

## Inbox chosen

**(a) GitHub Issues** on `dan116is/overnight-company` with label `waitlist`.

- New-issue URL (on live page CTA):  
  `https://github.com/dan116is/overnight-company/issues/new?labels=waitlist&title=Overnight%20waitlist%3A%20`
- Issues list (inbox):  
  `https://github.com/dan116is/overnight-company/issues?q=is%3Aissue+label%3Awaitlist`
- No invented email. No Vercel email secrets used.

## Proof of test receive

| Field | Value |
|-------|--------|
| Issue | **#1** |
| Title | Overnight waitlist: TEST receive verification |
| URL | https://github.com/dan116is/overnight-company/issues/1 |
| Label | `waitlist` |
| Created | 2026-09-18T07:49:01Z (= **10:49 IDT**) |
| Author | dan116is (via GitHub MCP `issue_write`) |

**Verified:** issue exists OPEN; label applied; body readable via `issue_read`.

## Live page updated?

**Yes.** Shipped to GitHub + Vercel production.

| Field | Value |
|-------|--------|
| Commit | https://github.com/dan116is/overnight-company/commit/e8362ce0df527babfa9a4c12ee7ea744b71e4f1e |
| Message | Waitlist: GitHub Issues inbox (label waitlist) |
| Path | root `index.html` on `main` (repo has no `landing/` tree) |
| Prior blob SHA | `16b87b5399a08ea550e586a4669e19fd7c6979a5` |
| New blob SHA | `34a2793167ee58df34660457d39859c735baedd7` |
| Live URL | https://overnight-company.vercel.app/ |
| Vercel deploy | `dpl_4HDE9uuSJXahaaTsuNduS83ZaDeG` (production READY) |
| Curl verify | HTTP 200 · size 9020 · contains `issues/new?labels=waitlist` · no `localStorage` |

Waitlist CTA on page points to GitHub Issues. No localStorage-only claim as the only path.

## Blockers / notes

- Vercel project `overnight-company` (`prj_kytH6bF3va0H79Kd2GEOO4orTpo4`) has **link: null** — Git push does not auto-redeploy; used `deploy_to_vercel` with `teamId=dan116is`.
- `deploy_to_vercel` with `teamId=team_RXvLDL0iNva2X2bNpr8M8Ori` returned **403** scope auth; slug `dan116is` worked.
- Optional follow-up: link GitHub repo to Vercel for future auto-deploys (`create_git_project` does not reconnect existing unlinked same-name project).
