# Golden Dataset & Reliability Contract

## Golden Dataset Spec

| # | Input | Expected Output | Edge Case? | Judge Type |
|---|-------|----------------|-----------|-----------|
TC01	| Claim: Annuitant requests scheduled monthly payment. Policy: Contract active, annuitant alive, payment schedule confirmed. Evidence: Valid identity and bank details. |	Approve. Process monthly annuity payment according to contract terms. No exception.|	NO	|RULE |
TC02	| Claim: Beneficiary requests death benefit. Policy: Death benefit payable upon annuitant's death. Evidence: Valid death certificate and beneficiary identity documents.	Approve. Validate beneficiary entitlement and initiate death benefit processing.	| NO	| BOTH |
TC03	| Claim: Annuitant requests withdrawal of $50,000. Policy: Contract permits withdrawals up to available surrender value of $30,000. Evidence: Valid identity and withdrawal request.	Partial approval / exception. Maximum eligible withdrawal is $30,000, subject to applicable charges and contract provisions. Explain shortfall. |	NO	| BOTH |
TC04	| Claim: Beneficiary submits death claim. Policy: Contract identifies a named primary beneficiary. Evidence: Death certificate uploaded, but beneficiary documentation is missing.	Hold. Request missing beneficiary documentation before processing payment.	|NO	|RULE |
TC05	| Claim: Annuitant requests scheduled payment. Policy: Contract is active. Evidence: System receives conflicting dates of birth across identity documents and policy records.	Escalate. Flag identity mismatch and route to claims operations for verification. Do not release payment.	| YES	| BOTH |
TC06	| Claim: Beneficiary submits death benefit claim. Policy: Primary beneficiary predeceased the annuitant; contingent beneficiary is listed. Evidence: Death certificates for both parties have conflicting dates.	Escalate. Verify sequence of deaths and beneficiary entitlement before determining payment recipient.	|YES|	LLM|
TC07	|Claim: Annuitant requests surrender of contract. Policy: Contract has a surrender charge during the applicable surrender period. Evidence: Surrender request is valid and contract value is available.	Approve subject to calculation. Calculate net surrender value after applicable surrender charges and disclose the calculation.	|NO	|RULE|
TC08	|Claim: Beneficiary requests payment following annuitant's death. Policy: Contract contains a provision for continued spousal payments. Evidence: Marriage certificate provided, but contract provisions require further interpretation.	Escalate. Determine whether the surviving spouse qualifies for continued payments under the contract. |	YES	|LLM|
TC09	|Claim: Annuitant requests a change to payment destination. Policy: Contract permits payment destination changes. Evidence: New bank account submitted, but account ownership cannot be verified.	Hold. Request bank account ownership verification before changing payment instructions.	|YES	|BOTH
TC10	|Claim: Two separate claims submitted for the same annuitant and contract. Policy: Contract permits only one applicable death benefit payment. Evidence: Duplicate claim references with matching death certificate and claimant information.	Flag duplicate and hold processing. Link claims, investigate duplication, and prevent duplicate payment. | YES | BOTH |

**Adversarial rows included:** __
**Coverage gaps identified by partner:**

## Confidence UX Design

**Approach:** show uncertainty / tiered confidence / human-in-loop trigger

**High confidence (>90%):**
**Medium confidence (70-90%):**
**Low confidence (<70%):**

**User control surface:**

## Reliability Contract

| Metric | Target | Measurement | Alert Threshold |
|--------|--------|-------------|-----------------|
| Accuracy | | | |
| Hallucination rate | | | |
| Latency (p95) | | | |
| Drift velocity | | | |

## HITL Architecture
<!-- When does a human step in? What's the escalation path? -->

## Red-Team Findings
*What failure mode did your partner find that you missed?*
