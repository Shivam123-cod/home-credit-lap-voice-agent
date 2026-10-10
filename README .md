# Home Credit Loan Against Property (LAP) Voice Agent

## Project Overview
This project implements an AI voice agent using Retell AI for the Home Credit Loan Against Property (LAP) qualification process.

The agent calls existing customers to inform them about a special loan offer of up to ₹75,00,000 and conducts a preliminary eligibility check.

## Objectives
- Inform customers about the Loan Against Property offer.
- Collect the required property and financial information.
- Check preliminary eligibility based on the defined business rules.
- Handle customer responses given in different orders.
- Identify disqualifying conditions.
- Route existing loan or EMI-reduction enquiries to the appropriate specialist.
- Arrange follow-up with a senior loan expert for eligible customers.

## Eligibility Checklist
The agent collects the following information:

1. Property type
2. Ownership status
3. Availability of original property documents
4. Requested loan amount
5. Occupation
6. Income mode
7. Property market value
8. Repayment tenure

## Business Rules
- Maximum offer: ₹75,00,000.
- Accepted property types: residential, commercial, and industrial.
- Agricultural property is not eligible.
- Sole and joint ownership are accepted.
- Original property documents must be available.
- Salaried and self-employed customers can qualify.
- Cash income is a disqualifying condition.
- Repayment tenure must be between 3 and 15 years.
- If the requested amount exceeds ₹75,00,000, the agent offers the maximum amount as an alternative.
- Existing property loan or EMI-reduction enquiries follow a separate specialist route.
- The agent must not confirm eligibility until all required checklist items have been collected and checked.
- The agent must not invent interest rates.

## Technology Used
- Retell AI
- AI voice agent and conversational prompting
- Voice call recordings and transcripts
- Manual scenario-based testing

## Project Structure
```text
home-credit-lap-voice-agent/
├── recordings/
├── transcripts/
├── test_results/
├── system_prompt.txt
├── README.md
└── approach_document.md
```

## Testing
The agent is tested against customer scenarios covering:
- Eligible customers
- Agricultural property
- Cash income
- Missing original documents
- Invalid repayment tenure
- Loan amounts above the maximum offer
- Joint ownership
- Existing loan enquiries
- EMI-reduction enquiries
- Out-of-order customer responses

Test recordings and transcripts are maintained in their respective folders.

## Test Results
The `test_results/` directory contains the documented results of the scenario-based tests.

## System Prompt
The complete system prompt used to configure the agent is available in `system_prompt.txt`.

## Limitations
- The agent performs preliminary qualification only; it does not make a final lending decision.
- Final eligibility, applicable interest rates, and loan terms must be confirmed by the appropriate loan expert.
- Speech recognition and ambiguous customer responses may require clarification.

## Disclaimer
This is an AI voice agent assignment demonstrating conversational design and preliminary qualification logic. It does not constitute a final loan approval or a binding financial offer.

## Call Logs and Recordings

Call logs, recording URLs, and call metadata exported from Retell AI are provided in `retell_call_logs.csv`.

Test audio recordings and conversation transcripts are available in this repository.

The CSV contains the public log URLs, scrubbed recording URLs, and recording URLs for the corresponding calls.

The public log URLs provide access to call execution logs, while the scrubbed recording URLs can be used to access the call recordings and conversation content.

## Deliverables

- System prompt: `system_prompt.txt`
- Test results: `test_results.md`
- Approach document: `approach_document.md`
- Call logs and recording URLs: `retell_call_logs.csv`
- Test recordings: Audio files (`.wav`)
- Test transcripts: Text files (`.txt`)
