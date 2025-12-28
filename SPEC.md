# Project Spec — Constructed Meaning Systems

## Purpose
Build small, production-ready automation systems using AI and n8n.
The focus is reliability, clarity, and real business workflows — not experimentation.

## First Application
A conversational booking assistant with the following capabilities:
- Accepts booking requests via chat
- Extracts structured data using AI reasoning
- Checks availability before confirming
- Stores bookings persistently
- Prevents double bookings

## Inputs
- Natural language chat messages from users
- Booking details inferred from text:
  - Name
  - Date
  - Time
  - Number of guests

## Outputs
- Confirmation message to the user
- A single, clean booking record stored in Google Sheets
- No data modification if a conflict is detected

## Constraints & Non-Goals
- The system must never overwrite or delete existing bookings
- If required data is missing or ambiguous, the system must ask follow-up questions
- The system does not handle payments, cancellations, or modifications
- Google Sheets is used as a temporary datastore, not a long-term database
- No UI beyond chat interaction is required at this stage

## Tech Stack
- n8n — automation logic and orchestration
- AI models — Gemini, Claude, Codex (reasoning and extraction)
- Google Sheets — temporary database
- GitHub — source of truth
- Vercel — future frontend only if required

## Definition of Done
- A booking can be created via chat input
- Conflicting bookings are detected reliably
- Data is stored in a clean, consistent format
- Workflow can be exported, reused, and redeployed
