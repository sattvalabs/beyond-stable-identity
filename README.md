# Beyond Stable Identity

Reproduction materials for **Beyond Stable Identity: A Modular Framework for Evaluating AI Assistant Behavior**, an exploratory study conducted during the Digital Minds Research Sprint (August 2026).

## Study overview

The study tests whether assistant identity is better described as a dynamic configuration of partially independent functions than as a single stable or unstable property. Six blinded conversations were coded across contextual orientation, substantive continuity, procedural continuity, judgment, declared self-ID, and enacted self-ID.

## Repository contents

- `paper/`: final paper in PDF and DOCX formats.
- `code/`: model-compatibility checks, pilot generation, and formal-study generation scripts.
- `data/formal-dataset.json`: complete machine-readable formal dataset.
- `data/raw-json/`: raw response records for all 18 formal conversations.
- `data/blinded-transcripts/`: transcripts used for blinded coding.
- `data/model-mapping.csv`: conversation IDs, conditions, repetitions, and model identifiers.
- `data/study-manifest.json`: randomized study plan and run metadata.
- `coding/CTP_Identity_Study_Coding_Workbook.xlsx`: coding guide, coding records, and calculations.

## Reproduction

The scripts are written for PowerShell and call the OpenRouter API. Set the API key for the current PowerShell session before running them:

```powershell
$env:OPENROUTER_API_KEY = "your-key-here"
```

Never save or commit the key to the repository. The formal runs used the exact model identifiers recorded in the dataset, `temperature = 0.7`, and `max_tokens = 600`.

1. Run `code/test-model-compatibility.ps1` to verify endpoint compatibility.
2. Run `code/run-formal-study.ps1` to reproduce the randomized 18-conversation formal dataset.
3. Use the coding workbook to reproduce the blinded qualitative coding and descriptive summaries reported in the paper.

The reported preliminary analysis used six conversations selected from the randomized order. No inferential statistical tests were performed.

## Citation

Amezaga, A. (2026). *Beyond Stable Identity: A Modular Framework for Evaluating AI Assistant Behavior*. Digital Minds Research Sprint.

## Author

Amaia Amezaga, Sattva Labs.
