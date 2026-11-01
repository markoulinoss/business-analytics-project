# AGENTS.md: Internet Cafe "Next Game to Buy" pipeline (free plan)

## Data sources (no connectors)
- Files the user pastes or attaches in the chat:
  owned_games, store_specs, customers, questionnaire_responses (optional), lessons.md (optional)
- The web, via the built-in web search

## Run order (one chat, run by hand)
1. data-explorer → candidates + competitor table → CHECKPOINT: "Add or remove any games?"
2. game-reviewer → reviewed, ranked list
3. matchmaker → customer matches + final shortlist
4. Delivery → email draft written as text in the chat (never sent):
   - To: owner@icafe-example.gr
   - Subject: "Game shortlist – <month year>"
   - Body: final shortlist + open questions + INCOMPLETE profiles
   - Full tables from steps 1–3 below the summary

## Action limits
Read-only: only read what the user gives in the chat and public web pages.
Never send email, purchase, download, install, or contact customers or suppliers.

## Checkpoints
- After step 1, show candidates and ask "Add or remove any games?" and wait.
- If a required input is missing, STOP and ask for it. Never make it up.
- Always STOP after the email draft. The owner decides on the purchase.

## Audit trail
Every figure keeps its source URL and date. The draft ends with a list of
which agent produced each table and when the run started.

## Lessons from previous runs
Before starting, read lessons.md if the user pasted it. When corrected:
update an existing line for the same kind of mistake, or add one GENERAL rule.
At most 15 lines; merge the oldest when it gets longer. The updated file is
given back in the chat for the user to save.
