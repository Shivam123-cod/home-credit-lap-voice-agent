# Approach Document: Home Credit LAP AI Voice Agent

## 1. Understanding the Requirement

The objective is to build an AI voice agent using Retell AI that contacts existing Home Credit customers and conducts a preliminary eligibility check for a Loan Against Property (LAP) offer of up to ₹75,00,000.

The agent must collect the required information, apply the specified business rules, handle natural conversations, and direct eligible customers toward a follow-up with a senior loan expert.

## 2. Agent Design

The agent uses a conversational approach rather than asking every question in a rigid order.

Its responsibilities are to:
- Introduce itself and explain the purpose of the call.
- Confirm that the customer can speak.
- Explain the LAP offer.
- Collect the required eligibility information.
- Remember answers already provided.
- Ask for missing information without unnecessarily repeating questions.
- Clarify ambiguous or contradictory answers.
- Identify disqualifying conditions.
- Route existing loan or EMI-reduction enquiries appropriately.
- Explain the next step without promising loan approval.

## 3. Eligibility Information

The agent tracks eight required fields:

1. Property type
2. Ownership status
3. Availability of original property documents
4. Requested loan amount
5. Occupation
6. Income mode
7. Property market value
8. Repayment tenure

The agent should collect these fields even when the customer provides the answers in a different order.

## 4. Business Rule Implementation

| Condition | Expected agent behaviour |
|---|---|
| Residential property | Continue eligibility checks |
| Commercial property | Continue eligibility checks |
| Industrial property | Continue eligibility checks |
| Agricultural property | Disqualify |
| Sole ownership | Accept |
| Joint ownership | Accept |
| Original documents unavailable | Disqualify |
| Salaried occupation | Acceptable |
| Self-employed occupation | Acceptable |
| Cash income | Disqualify |
| Bank-based income | Acceptable |
| Tenure below 3 years | Disqualify |
| Tenure above 15 years | Disqualify |
| Tenure from 3 to 15 years | Acceptable |
| Requested amount above ₹75 lakh | Offer ₹75 lakh as an alternative |
| Existing property loan or EMI-reduction request | Route to the appropriate specialist |

The agent must not assume eligibility when required information is missing or unclear.

## 5. Conversation Memory and Error Handling

The agent is instructed to remember information provided during the current call.

When customers provide multiple answers together, the agent should record all clear answers and ask only for the missing information.

If a customer corrects an earlier answer, the corrected answer should replace the previous value.

If speech recognition produces an unclear or unexpected answer, the agent should ask a short clarification question instead of making an assumption.

## 6. Testing Strategy

Scenario-based testing is used to evaluate the agent's responses to different customer situations.

The scenarios cover:
- A potentially eligible customer
- Agricultural property
- Cash income
- Missing original documents
- Repayment tenure below the permitted range
- Repayment tenure above the permitted range
- A requested amount exceeding ₹75 lakh
- Joint ownership
- Existing property loan enquiries
- EMI-reduction enquiries
- Answers provided out of order

Additional tests should evaluate busy customers, ambiguous responses, interruptions, and contradictory information.

## 7. Evaluation Criteria

Each test should be reviewed for:
- Correct application of the business rules
- Completeness of information collection
- Correct handling of out-of-order answers
- Avoidance of unnecessary repeated questions
- Appropriate clarification of ambiguous answers
- Correct handling of disqualifying conditions
- Appropriate routing of specialist enquiries
- Accurate and professional communication
- Avoidance of unsupported promises or invented interest rates

Actual results should be recorded from the call transcripts and recordings.

## 8. Limitations and Improvements

Speech recognition errors and ambiguous customer responses can affect the conversation. The agent should clarify uncertain information before proceeding.

Further improvements can include more adversarial test scenarios, systematic evaluation of every eligibility rule, and improved handling of interruptions and conflicting answers.

The agent performs preliminary qualification only. Final eligibility, loan approval, and applicable interest rates must be confirmed by the appropriate loan expert.

## 9. Deliverables

The project deliverables include:
- Complete system prompt
- Call recordings
- Call transcripts
- Scenario-based test results
- README documentation
- This approach document
- Published agent or demonstration link, where available