Bastion Brief



## Problem
>Consultants brief each client on current threats using European cybersecurity agency reports, mixed with each client's own incident notes and policies. Client-uploaded files can contain hidden instructions or personal data, and a careless AI tool can be tricked into leaking or obeying them

## Who it is for
>Threat-intelligence assistant for client security teams that stays safe even when a document tries to hijack it.
## Signature feature
>Quarantine view that shows which uploaded pages were flagged as injection attempts or PII, and why.

## Hardest problem (my interview story)
>Prompt-injection and personal-data safety. Uploaded documents are scanned for injection patterns and PII (emails, phone numbers, Aadhaar-like numbers) and redacted before indexing, and retrieved text is passed to the model as quoted data, never as instructions. A red-team set of 80 poisoned documents measures how often the model is hijacked.

## Dataset
| Source | Link | Documents | Pages | Licence / terms |
|---|---|---|---|---|
| <ENISA Threat Landscape 2026_Final.pdf> | <https://www.enisa.europa.eu/sites/default/files/2026-09/ENISA%20Threat%20Landscape%202026_Final.pdf> | <.pdf> | <101> | <© European Union Agency for Cybersecurity (ENISA), 2026> |

## 10 real questions
See [docs/QUESTIONS.md](docs/QUESTIONS.md).

## Run it
```bash
python -m venv .venv && source .venv/bin/activate   # Windows: .venv\Scripts\activate
pip install -r requirements-dev.txt
cp .env.example .env                                 # Windows: copy .env.example .env
uvicorn app.main:app --reload
curl localhost:8000/health
```

## Live link
<Added in Week 2>
