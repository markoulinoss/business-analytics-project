# Internet Cafe Game buyer 

Three skills that find, review and match new games to an internet cafe's
customers and write a purchase shortlist email draft.

## Requires
- Built-in web search (turn it on in the chat's tools/settings).

## Install
Upload each skill under Customize → Skills:
- skills/data-explorer.zip
- skills/game-reviewer.zip
- skills/matchmaker.zip

## Run
1. Start a new chat, attach the files from `sample-inputs/` (or your own),
   and write: "Run the game pipeline for November 2026. Area: Athens."
2. Answer the checkpoint "Add or remove any games?".
3. Copy the final email draft into your email app yourself.

## Inputs
| File | Used by | Required |
|---|---|---|
| owned_games.csv | data-explorer | yes |
| store_specs.csv | game-reviewer | yes |
| customers.csv | matchmaker | yes |
| questionnaire_responses.csv | matchmaker | no |
| lessons.md | all | no |

All data is fictional/anonymized.
