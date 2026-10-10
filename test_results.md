# Home Credit LAP Voice Agent — Test Results

## Testing Summary

The AI voice agent was tested using customer scenarios designed to evaluate eligibility decisions, conversational handling, and business-rule compliance.

Each scenario should be evaluated using its actual call transcript and recording.

## Test Cases

| Test ID | Scenario | Expected Result | Actual Result | Status |
|---|---|---|---|---|
| TC-01 | Eligible customer | Complete checklist and arrange expert follow-up | To be reviewed | Pending |
| TC-02 | Agricultural property | Disqualify customer | To be reviewed | Pending |
| TC-03 | Cash income | Disqualify customer | To be reviewed | Pending |
| TC-04 | Original documents unavailable | Disqualify customer | To be reviewed | Pending |
| TC-05 | Tenure of 2 years | Disqualify customer | To be reviewed | Pending |
| TC-06 | Tenure of 20 years | Disqualify customer | To be reviewed | Pending |
| TC-07 | Requested loan of ₹90 lakh | Offer ₹75 lakh and continue only if accepted | To be reviewed | Pending |
| TC-08 | Joint property ownership | Accept ownership and continue checks | To be reviewed | Pending |
| TC-09 | Existing property loan | Route to the appropriate specialist | To be reviewed | Pending |
| TC-10 | Answers provided out of order | Remember answers and ask only for missing information | To be reviewed | Pending |
| TC-11 | EMI-reduction enquiry | Route to the appropriate specialist | To be reviewed | Pending |
| TC-12 | Customer is busy | Ask for a suitable callback time and end the call | To be reviewed | Pending |

## Evaluation Criteria

- Correct application of eligibility rules
- Collection of all required information
- Appropriate handling of ambiguous answers
- Correct handling of out-of-order answers
- No unnecessary repetition of answered questions
- Correct disqualification and specialist routing
- Professional communication
- No unsupported promises about loan approval or interest rates

## Notes

The actual result and status for each test must be updated after reviewing its transcript and recording.

Do not mark a test as Passed unless the recorded conversation supports that conclusion.