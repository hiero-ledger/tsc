# TSC Voting Procedures Proposal

## Overview

This proposal establishes standardized voting procedures for the Hiero Technical Steering Committee (TSC) to improve decision-making efficiency while maintaining transparency and adherence to charter requirements.

## Voting Methods

### 1. In-Meeting Votes
- **When Used**: For decisions during TSC meetings with quorum present
- **Threshold**: Simple majority of members present
- **Recording**: Documented in meeting minutes with vote counts

### 2. Asynchronous Votes via GitHub Pull Request
- **When Used**: 
  - When quorum cannot be achieved in meetings
  - For decisions requiring extended review/discussion
  - For charter-mandated votes (e.g., license exceptions)
- **Location**: Pull requests in the `proposals/` directory
- **Notification**: All TSC members must be notified via:
  - GitHub PR mention (@username)
  - Slack notification in TSC channel

## Voting Process

### Step 1: Discussion (Optional)
- Create a GitHub Issue for complex proposals requiring discussion
- Label with "tsc-discussion"
- No formal timeline - continue until consensus on proposal language

### Step 2: Proposal Creation
1. Create a new file in `proposals/` directory following the template
2. File naming convention: `YYYY-MM-DD-brief-description.md`
3. Open a Pull Request with the finalized proposal
4. **Proposal is immutable once PR is opened** - no changes allowed
5. Link to discussion issue if one exists

### Step 3: Voting Period
- **Duration**: 7 calendar days maximum
- **Purpose**: Voting only (discussion happens in issue, not PR)
- **Voting Method**: 
  - Approve PR = Yes vote
  - Request Changes = No vote
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
- **Recording**: Merge PR if passed, close if failed

## Voting Eligibility

### Prerequisites
- All TSC members must have a GitHub account to participate in voting

### Active Voting Members
- All TSC members listed in README.md
- Have not missed 3 consecutive TSC meetings
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

### Urgent Decisions
- **Definition**: Time-sensitive matters requiring faster resolution
- **Process**: 
  - 3 calendar days total
  - Requires explicit "URGENT" label on PR
  - Must document urgency rationale

### Lazy Consensus
- **When Used**: Minor procedural changes, documentation updates
- **Process**: 
  - 3 calendar days review period
  - Assumed approval if no objections
  - Any TSC member can request full vote

### Tied Votes
- **Resolution**: 
  - TSC Chair breaks tie
  - If Chair abstained/absent: Defer to next meeting
  - If still tied: Proposal fails

## Templates

### Proposal Template
```markdown
# [Proposal Title]

**Date**: YYYY-MM-DD
**Author**: [Name] (@github-username)
**Type**: [Standard | Urgent | Charter-Required]

## Summary
Brief description of the proposal

## Motivation
Why this decision is needed

## Proposal Details
Detailed description of what is being proposed

## Impact
- Technical impact
- Community impact
- Timeline considerations

## Alternatives Considered
Other options that were evaluated

## Vote Threshold
- [ ] Standard (>50% of eligible voting members)
- [ ] Charter-specified (define requirement)
```

### Voting Record Template
```markdown
## Voting Record

**Voting Period**: YYYY-MM-DD to YYYY-MM-DD
**Eligible Voters**: X
**Votes Required**: Y

### Results
- **Yes**: X votes
  - @member1
  - @member2
- **No**: Y votes
  - @member3
- **Abstain**: Z members
  - @member4

**Decision**: [Passed | Failed]
```

### Example: tsc-voting-eligibility.md
```markdown
# TSC Voting Eligibility

Last Updated: YYYY-MM-DD

## Active Voting Members

| Member | GitHub Username | Status | Last Meeting Attended |
|--------|----------------|--------|----------------------|
| Jane Doe | @janedoe | Active | 2024-01-15 |
| John Smith | @jsmith | Active | 2024-01-15 |
| Alice Johnson | @alicej | Active | 2024-01-08 |
| Bob Wilson | @bwilson | Suspended | 2023-12-01 |

## Suspension Notes
- Bob Wilson: Suspended due to missing 3 consecutive meetings (2023-12-15, 2024-01-08, 2024-01-15)

## Eligibility Rules
- Missing 3 consecutive TSC meetings results in automatic voting suspension
- Reinstatement occurs upon attendance at next TSC meeting
```


## Appendix: Rationale

This proposal addresses several key challenges:

1. **Quorum Issues**: Asynchronous voting allows participation regardless of meeting attendance
2. **Transparency**: GitHub PRs provide public record of all decisions
3. **Efficiency**: Clear timelines prevent decision delays
4. **Flexibility**: Multiple voting methods accommodate different decision types
5. **Compliance**: Maintains charter requirements while improving process

## Proposed Charter Modifications

To implement this proposal effectively, the following charter modification is recommended:

### Meeting Attendance Requirement
Modify section 3(ix)(d)(d) to reduce reinstatement requirement from two meetings to one:

> Any TSC member, including permanent members, that misses three (3) consecutive meetings shall be automatically suspended from eligibility to vote, i.e. no longer considered an active member, until having attended a meeting. For avoidance of doubt, the suspended TSC member shall be eligible to vote in the meeting following their absence.

### Voting Threshold Clarification
Add explicit language that standard decisions require >50% of eligible voting members (currently implied but not stated).

## Review

This procedure should be reviewed after 6 months of implementation and adjusted based on TSC experience.