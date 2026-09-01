# Information Processing Example

## Information Tasks Used

This example demonstrates **summarizing, extracting, restructuring, and prioritizing**. These tasks were selected because a Digital Solutions Analyst often needs to turn scattered meeting notes into a brief that supports decisions and follow-up.

## 1. Raw Input

> Product launch meeting recap: decided to push beta to 200 users starting Monday (confirmed by Priya). Design still owes the updated onboarding flow - due "soon." Support flagged that FAQ isn't ready and someone needs to own that before launch. Marketing asked again if we're doing a press push - no decision made. Budget for user incentives still not approved. Next check-in is Thursday.

## 2. Prompt Used

**Context:** These are raw meeting notes for the pilot launch of a fictional internal service portal. The brief will be read by the project manager.

**Action:** Summarize the notes, extract confirmed decisions and action items, identify risks and open questions, and prioritize the items that could block the launch.

**Rules:** Preserve all names, dates, numbers, decisions, and uncertainty. Do not invent owners or deadlines. Do not turn a question into a decision. Mark missing information as `[Not Specified]`.

**Expected Output:** Start with a three-bullet bottom line, then provide decisions, open questions, risks, and an action-item table with Action Item, Owner, Deadline, Priority, and Status.

## 3. AI Output - First Draft

### Bottom Line

- The beta launch for 200 users will start Monday.
- Design will complete the onboarding flow before launch.
- Support will prepare the FAQ and Marketing will prepare a press announcement.

### Actions

| Action Item | Owner | Deadline | Priority | Status |
|---|---|---|---|---|
| Complete onboarding flow | Design | Monday | High | In progress |
| Complete FAQ | Support | Monday | High | In progress |
| Prepare press announcement | Marketing | Thursday | Medium | Planned |

## 4. Human Review

The first draft contains unsupported assumptions:

- The source says the onboarding flow is due **“soon,”** not Monday.
- The FAQ owner is not assigned; Support only raised the concern.
- No decision was made about a press push, so it is not a planned action.
- The status **“In progress”** was not provided.
- Budget approval was missing from the first draft.

I corrected these issues and preserved uncertainty in the final output.

## 5. Final Structured Output

### Bottom Line

- The beta launch to 200 users is confirmed for Monday by Priya.
- The updated onboarding flow and support FAQ remain incomplete; the FAQ has no assigned owner.
- The press push and user-incentive budget remain undecided or unapproved. The next check-in is Thursday.

### Confirmed Decision

| Decision | Evidence | Status |
|---|---|---|
| Launch the beta to 200 users starting Monday | Confirmed by Priya | Confirmed |

### Action Items

| Action Item | Owner | Deadline | Priority | Status |
|---|---|---|---|---|
| Complete the updated onboarding flow | Design | `[Not Specified]` (described only as "soon") | High | Open |
| Assign an owner and complete the FAQ before launch | `[Not Specified]` | Before launch | High | Open |
| Obtain a decision on the press push | `[Not Specified]` | `[Not Specified]` | Medium | Open decision |
| Obtain approval or rejection for the user-incentive budget | `[Not Specified]` | `[Not Specified]` | Medium | Pending approval |
| Conduct the next project check-in | Project team | Thursday | Medium | Scheduled |

### Risks and Open Questions

- **Launch-readiness risk:** The onboarding flow and FAQ are incomplete.
- **Ownership gap:** No owner is assigned to the FAQ.
- **Open decision:** Will the organization conduct a press push?
- **Budget dependency:** The user-incentive budget is not approved.
