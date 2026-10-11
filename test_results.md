# Test Results

## T01 — Eligible Customer
- **Status:** Tested
- **Observed behavior:** The agent collected the required eligibility details for a residential property, sole ownership, available original documents, a ₹50 lakh requested loan, salaried income credited to a bank account, ₹1 crore property value, and a 10-year tenure.
- **Assessment:** The observed result matched the expected preliminary qualification flow, with senior expert handoff indicated in the conversation.

## T02 — Agricultural Property
- **Status:** Tested
- **Observed behavior:** When the customer stated that the property was agricultural land, the agent explained that it did not qualify for the offer and ended the call.
- **Assessment:** Passed. The agent did not continue the remaining eligibility questions.

## T03 — Cash-Based Income
- **Status:** Tested
- **Observed behavior:** The customer stated that their self-employed income was received entirely in cash. The agent disqualified the customer under the stated eligibility rules.
- **Assessment:** The observed behavior matched the expected disqualification flow.

## T04 — Original Documents Unavailable
- **Status:** Tested
- **Observed behavior:** The customer had only photocopies of the property documents. The agent explained that original documents were required and that the customer did not qualify under this condition.
- **Assessment:** The observed behavior matched the expected disqualification flow.

## T09 — Existing Property Loan / EMI Reduction
- **Status:** Tested
- **Observed behavior:** The customer stated that they already had a loan against the property and wanted to reduce their EMI. The agent directed the customer to a loan-transfer specialist.
- **Assessment:** The observed behavior matched the expected specialist-routing flow.

## T12 — Busy Customer / Callback Request
- **Status:** Tested
- **Observed behavior:** The customer said they were busy and requested a callback tomorrow at 11 AM. The agent acknowledged the requested time and ended the call.
- **Assessment:** The observed behavior matched the expected callback-request flow. This does not confirm that an actual callback was technically scheduled.

## Overall Summary

Six test calls were reviewed to evaluate preliminary qualification, disqualification conditions, callback handling, and specialist routing. The observed behavior for each call was documented for review against the intended prompt rules. The results cover only the six scenarios listed above.
