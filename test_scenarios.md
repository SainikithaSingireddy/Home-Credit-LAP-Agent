# Home Credit LAP Voice Agent — Test Scenarios

## Purpose
Test the voice agent's eligibility rules, conversation flow, memory, interruption handling, and handoff discipline.

## Test Matrix

| ID | Scenario | Customer Input / Test Condition | Expected Agent Behavior |
|---|---|---|---|
| T01 | Eligible customer | Residential, sole owner, originals available, ₹50 lakh, salaried with bank income, ₹1 crore market value, 10-year tenure | Capture all seven items, confirm preliminary qualification, and hand off to a senior expert |
| T02 | Agricultural property | Customer says the property is agricultural land | Disqualify immediately and end the call without further eligibility questions |
| T03 | Cash-only income | Customer receives income only in cash | Disqualify immediately and end the call |
| T04 | Original documents unavailable | Customer says original documents are unavailable and only photocopies exist | Disqualify immediately and end the call |
| T05 | Tenure below minimum | Customer requests a 2-year tenure | Disqualify immediately and end the call |
| T06 | Tenure above maximum | Customer requests a 20-year tenure | Disqualify immediately and end the call |
| T07 | Loan amount exceeds limit | Customer requests ₹90 lakh | Explain the ₹75 lakh limit and ask whether they want to proceed with ₹75 lakh; follow their answer |
| T08 | Joint ownership | Customer says the property is jointly owned with their spouse | Accept joint ownership and continue with the earliest unanswered item |
| T09 | Existing property loan | Customer says they already have a loan against the property | Stop fresh-loan qualification, explain the specialist follow-up, and end the call |
| T10 | EMI reduction | Customer wants to reduce an existing EMI | Stop fresh-loan qualification, explain the specialist follow-up, and end the call |
| T11 | Out-of-order answers | Customer gives property type, ownership, and market value before being asked all three | Store all clear answers and ask only the earliest unanswered item |
| T12 | Busy customer | Customer says they are busy or in a meeting | Ask for a convenient callback time, thank them, and end without claiming a callback was scheduled |
| T13 | Wrong person | Person says the intended customer is unavailable or this is the wrong number | Apologize and end without revealing loan-offer details |
| T14 | Contradictory property answer | Customer says residential, then clearly corrects it to agricultural | Use the latest clear answer; disqualify immediately |
| T15 | Multiple facts in one response | Customer gives ownership, document availability, loan amount, and tenure together | Record all clear facts and ask only the earliest unanswered item |
| T16 | Ambiguous document availability | Customer says the original papers are “probably somewhere” | Ask for clarification; do not assume originals are available |
| T17 | Interest-rate diversion | Customer asks for the exact interest rate before qualification is complete | Do not invent a rate; explain that the senior expert will provide it and resume the checklist |
| T18 | Interruption | Customer interrupts to ask which property documents are needed | Answer briefly using verified information, then resume at the earliest unanswered item |

## Test Evidence Rules

- Record the actual outcome of each test.
- Link the corresponding recording and transcript when available.
- Mark tests as **Passed**, **Failed**, or **Not tested** based on evidence.
- Do not report expected behavior as an observed result.
- Existing recordings must remain associated with the prompt version that produced them.

## Scope Notes

- The market-value question has no minimum eligibility threshold specified in the assignment.
- Joint ownership is permitted.
- The ₹75 lakh limit requires an alternative-offer question, not automatic disqualification.
- Final qualification and senior-expert handoff are permitted only after all seven checklist items pass.
- Callback and specialist follow-up are conversational commitments only; do not claim they were technically scheduled.