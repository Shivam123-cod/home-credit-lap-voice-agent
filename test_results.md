# Home Credit LAP Voice Agent — Test Results

## Testing Summary

The AI voice agent was tested using customer scenarios covering eligibility decisions, conversational handling, and business-rule compliance.

Results are based on the actual conversations reviewed so far. Tests marked Pending still require transcript and recording review.

## Test Cases

| Test ID | Scenario | Expected Result | Actual Result | Status |
|---|---|---|---|---|
| TC-01 | Eligible customer | Collect all required details and provide preliminary screening outcome | Agent collected all eight required fields, clarified the unclear occupation answer, and provided the appropriate expert follow-up message | Pass |
| TC-02 | Agricultural property | Disqualify customer | To be reviewed | Pending |
| TC-03 | Cash income | Disqualify customer | To be reviewed | Pending |
| TC-04 | Original documents unavailable | Disqualify customer | To be reviewed | Pending |
| TC-05 | Tenure of 2 years | Disqualify customer | To be reviewed | Pending |
| TC-06 | Tenure of 20 years | Disqualify customer | To be reviewed | Pending |
| TC-07 | Requested loan of ₹90 lakh | Offer ₹75 lakh and continue only if accepted | To be reviewed | Pending |
| TC-08 | Joint ownership | Accept ownership and continue eligibility checks | To be reviewed | Pending |
| TC-09 | Existing property loan | Route to the appropriate specialist | To be reviewed | Pending |
| TC-10 | Answers provided out of order | Remember answers and ask only for missing information | To be reviewed | Pending |
| TC-11 | EMI-reduction enquiry | Route to the appropriate specialist | To be reviewed | Pending |
| TC-12 | Customer is busy | Ask for a callback time, confirm it, and end the call without continuing eligibility screening | Agent requested a callback time, confirmed tomorrow at 11 AM, and ended politely | Pass |
| TC-13 | Eligible customer after prompt update | Use the corrected greeting and complete eligibility screening | Greeting was correct; agent clarified occupation, collected the required information, and provided the appropriate expert follow-up message | Pass |

## Additional Observations

- The greeting no longer speaks literal placeholder variables.
- The agent correctly clarified an unclear occupation response.
- The agent collected the required eligibility information in the updated eligible-customer test.
- Further testing is needed to verify all disqualification and specialist-routing scenarios.

## Evaluation Criteria

- Correct application of eligibility rules
- Collection of all required information
- Appropriate handling of ambiguous answers
- Correct handling of out-of-order answers
- No unnecessary repetition of answered questions
- Correct disqualification and specialist routing
- Professional communication
- No unsupported promises about loan approval or interest rates

## Note

A test should be marked Passed only when the actual transcript and recording support the expected behavior.
