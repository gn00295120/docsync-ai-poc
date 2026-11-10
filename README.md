# DocSync AI PoC — Missing Authorization (CWE-862)

This repository demonstrates the missing authorization vulnerability in
`deriv-com/deriv-smartcharts` and `deriv-com/derivatives-smarttrader`'s
DocSync AI workflow.

The workflow is triggered by `issue_comment` and checks only the comment
text (`startsWith(body, '@docbot')`), never the commenter's identity.

## How to reproduce

1. Create a pull request in this repo
2. Post a comment: `@docbot update only readme <any text>`
3. Observe the workflow fires and pushes a commit — with NO identity check

## DocSync AI Update

Updated by DocSync AI from PR comment.
Content: Security research PoC — attacker-controlled text written without identity check (CWE-862)
Timestamp: 2026-11-10T14:03:44Z
