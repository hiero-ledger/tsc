# TSC Voting Procedures Proposal

## Summary

This proposal establishes standardized voting procedures for the Hiero Technical Steering Committee (TSC) to improve decision-making efficiency while maintaining transparency and adherence to charter requirements.

## Motivation

Sometimes the TSC struggles to achieve qourum around key decisions or requires additional time outside of a meeting to deliberate on a decision. Asynchronous voting through Github Pull Requests would enable both flexibility and a solution for voting outside of the short meeting window.  

## Proposal Details

## Voting Methods

### 1. In-Meeting Votes

- **When Used**: For decisions during TSC meetings with quorum present
- **Threshold**: Simple majority of members present
- **Recording**: Documented in meeting minutes with vote counts

### 2. Asynchronous Votes via GitHub Pull Request

- **When Used**:
  - When [quorum](https://github.com/hiero-ledger/hiero/blob/main/technical-charter.md?plain=1#L206) cannot be achieved in meetings
  - When voting must be completed before next TSC meeting
  - When a TSC member requests async voting due to inability to attend meeting
  - For charter-mandated votes requiring 2/3 majority [per Charter section 4. iii](https://github.com/hiero-ledger/hiero/blob/main/technical-charter.md?plain=1#L209)
- **Location**: Pull requests in the `proposals/` directory
- **Notification**: All TSC members must be notified via:
  - GitHub PR mention (@username)
  - Slack notification in TSC channel

## Voting Process for In-Meeting Votes

### Step 1: Proposal Introduction
- Present the proposal during TSC meeting
- Allow for discussion and clarification

### Step 2: Call for Vote
- TSC Chair or designee calls for vote
- Confirm [quorum](https://github.com/hiero-ledger/hiero/blob/main/technical-charter.md?plain=1#L206) is present

### Step 3: Voting
- Members vote verbally or via meeting platform
- Record each member's vote

### Step 4: Resolution
- Tally votes and announce result
- Document in meeting minutes with vote counts

## Voting Process for Asynchronous Votes

### Step 1: Discussion (Optional)

- Create a GitHub Discussion for complex proposals requiring discussion
- Label with "tsc-discussion"
- No formal timeline - continue until consensus on proposal language

### Step 2: Proposal Creation

1. Create a new file in `proposals/` directory following the template
2. File naming convention: `YYYY-MM-DD-brief-description.md`
3. Open a Pull Request with the finalized proposal
4. **Proposal is immutable once PR is opened** - no changes allowed
5. Link to discussion issue if one exists

### Step 3: Voting Period

- **Duration**: 14 calendar days maximum
- **Purpose**: Voting only (discussion happens in issue, not PR)
- **Voting Method**:
  - Approve PR = "Yes" vote
  - Request Changes = "No" vote
  - No response = Abstention
- **Comments**: Brief rationale only - substantive discussion in linked issue

### Step 4: Resolution

- **Passing Threshold**:
  - Standard decisions: >50% of eligible voting members
  - Charter-specified decisions: As defined in charter (e.g., 2/3 for license exceptions)
- **Early Resolution**: Vote concludes immediately when:
  - More than 50% of eligible members vote "Yes" (proposal passes)
  - More than 50% of eligible members vote "No" (proposal fails)
  - Mathematically impossible to change outcome
- **Quorum**: Minimum participation of 50% of eligible voting members
- **Recording**: 
  - If passed: Merge PR, then create follow-up PR to add voting record
  - If failed: Close PR with comment summarizing results

## Voting Eligibility

### Prerequisites

- All TSC members must have a GitHub account to participate in voting

### Active Voting Members

- All TSC members listed in README.md
- Have not missed the required number of consecutive TSC meetings defined in the [charter](https://github.com/hiero-ledger/hiero/blob/main/technical-charter.md?plain=1#L171)
- Have GitHub account with appropriate repository access

### Eligibility Tracking

- Maintain eligibility status in `tsc-voting-eligibility.md`
- Update after each meeting
- Include:
  - Member name
  - GitHub username
  - Voting status (active/suspended)
  - Last meeting attended

## Special Voting Scenarios

### Tied Votes

- **Resolution**:
  - If tied: Proposal fails

## Templates

### Proposal Template

See [proposal-template.md](./proposal-template.md) for the standard proposal format. This voting procedures proposal itself follows this template.

### Voting Record Template

For passed proposals only, create a follow-up PR to append the voting record to the merged proposal. This creates a permanent record while maintaining the immutability of proposals during voting.

**Usage for Passed Proposals:**
1. After merging the proposal PR, create a new PR
2. Add a new `## Voting Record` section at the end of the proposal document
3. Fill in the template from [voting-record-template.md](./voting-record-template.md)
4. Title the PR: "Add voting record to [proposal name]"
5. This administrative PR can be merged without formal voting

For failed proposals, the voting results are documented in the closing comment of the PR.

### TSC Voting Eligibility Example

See [tsc-voting-eligibility-example.md](./tsc-voting-eligibility-example.md) for an example of how to track member voting eligibility.

## Impact

- **Technical impact**: Leverages GitHub's existing PR review system for voting infrastructure
- **Community impact**: Increases transparency through public voting records
- **Timeline considerations**: 14-day maximum voting period balances thoroughness with efficiency

## Alternatives Considered

1. **Email-based voting**: Rejected due to lack of transparency and difficulty tracking votes
2. **Dedicated voting platform**: Rejected due to additional tooling complexity
3. **Status quo (meeting-only votes)**: Rejected due to ongoing quorum challenges

## Proposed Charter Modifications

To implement this proposal effectively, the following charter modification is recommended:

### Meeting Attendance Requirement

Modify section 3(ix)(d)(d) to reduce reinstatement requirement from two meetings to one:

> Any TSC member, including permanent members, that misses three (3) consecutive meetings shall be automatically suspended from eligibility to vote, i.e. no longer considered an active member, until having attended a meeting. For avoidance of doubt, the suspended TSC member shall be eligible to vote in the meeting following their absence.

### Voting Threshold Clarification

Add explicit language that standard decisions require >50% of eligible voting members (currently implied but not stated).

Note: These changes are not proposed as part of this proposal, but are included for completeness and should be considered for a future charter amendment.

## Review

This procedure should be reviewed after 6 months of implementation and adjusted based on TSC experience.

---

*Note: This proposal follows the format defined in [proposal-template.md](./proposal-template.md) and serves as the first example of the asynchronous voting process it establishes. As the foundational governance proposal, this PR may be amended based on feedback during the voting period to ensure the process is properly established, bypassing the immutable rule defined in proposal itself.*
