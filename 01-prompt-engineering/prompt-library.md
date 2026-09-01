# Prompt Library

This library contains reusable prompts for recurring Digital Solutions Analyst tasks. Each prompt follows either the C.A.R.E. framework (Context, Action, Rules, Expected Output) or the R.C.T.O. framework (Role, Context, Task, Output).

| Prompt Name | Workplace Task | Framework | Prompt | Expected Output |
|---|---|---|---|---|
| Requirements Extractor | Extract requirements from workshop notes | C.A.R.E. | **Context:** I am a Digital Solutions Analyst reviewing anonymized workshop notes for an internal service portal.<br>**Action:** Extract business requirements, user needs, constraints, assumptions, questions, and decisions.<br>**Rules:** Use only the supplied notes. Do not invent missing details. Mark missing owners or dates as `[Not Specified]`. Separate confirmed items from unconfirmed items.<br>**Expected Output:** A Markdown table with ID, category, statement, source evidence, status, owner, and follow-up question. | A traceable requirements table with gaps clearly flagged. |
| Decision-Ready Meeting Brief | Summarize messy meeting notes | C.A.R.E. | **Context:** The following notes come from a project meeting about an internal service portal.<br>**Action:** Create a concise brief for the project manager.<br>**Rules:** Preserve names, dates, numbers, decisions, and uncertainty. Do not convert suggestions into decisions. Mark missing information as `[Not Specified]`.<br>**Expected Output:** Start with a three-bullet bottom line, followed by decisions, risks, open questions, and an action-item table with owner, deadline, priority, and status. | **Example:** Pilot confirmed for 200 users on Monday; onboarding update remains open; FAQ ownership is not assigned. |
| Timeline Change Email | Communicate a project delay | R.C.T.O. | **Role:** Act as a Digital Solutions Analyst preparing a project communication.<br>**Context:** The project deadline changed from September 15, 2026 to September 25, 2026 because of a technical delay.<br>**Task:** Write a professional email to the project team explaining the update.<br>**Output:** Include a subject line and short paragraphs. Use a professional, friendly, and concise tone. Mention both dates and the reason. Do not add unconfirmed impacts. | **Example:** A short email that clearly states the old deadline, new deadline, and reason without blame. |
| Risk Log Builder | Turn project updates into a risk log | C.A.R.E. | **Context:** I am monitoring a fictional internal portal project and will provide anonymized project updates.<br>**Action:** Identify risks, issues, assumptions, and dependencies.<br>**Rules:** Distinguish current issues from possible risks. Do not assign probability, impact, owner, or due date unless supported by the input. Flag unknowns.<br>**Expected Output:** A table with type, description, evidence, probability, impact, owner, mitigation, and status. | A structured RAID-style log with unsupported fields marked `[Not Specified]`. |
| Process Improvement Ideas | Brainstorm improvements to a workflow | R.C.T.O. | **Role:** Act as a process-improvement assistant supporting a Digital Solutions Analyst.<br>**Context:** The current fictional service-request process uses email and spreadsheets, causing duplicate entries and slow status updates.<br>**Task:** Generate practical improvement options and compare them.<br>**Output:** Provide five options in a table with benefit, effort, risk, dependency, and recommended next step. Treat recommendations as suggestions for human review. | Five evaluated options, followed by a clearly labeled recommendation. |
| Project Planning Chain | Build an actionable project plan | C.A.R.E. | **Context:** A Digital Solutions Analyst must prepare a four-week plan for an internal service portal pilot.<br>**Action:** Break the goal into mechanisms, phases, and specific tasks.<br>**Rules:** Keep the plan realistic and concise. Identify dependencies. Do not invent named owners or confirmed dates.<br>**Expected Output:** Goal, success measures, mechanisms, phase table, tasks, dependencies, and open decisions. | A short Goal to Mechanisms to Phases to Tasks plan. |
| Acceptance Criteria Draft | Draft testable acceptance criteria | R.C.T.O. | **Role:** Act as a Digital Solutions Analyst drafting acceptance criteria.<br>**Context:** I will provide one anonymized user story for an internal service portal.<br>**Task:** Draft acceptance criteria and identify ambiguity.<br>**Output:** Use Given/When/Then statements, followed by assumptions and clarification questions. Do not add functions not mentioned in the story. | Testable acceptance criteria plus questions requiring stakeholder confirmation. |

## How I Would Use These Prompts

- **Requirements Extractor:** after a requirements workshop.
- **Decision-Ready Meeting Brief:** after meetings with scattered notes.
- **Timeline Change Email:** when a confirmed schedule change must be communicated.
- **Risk Log Builder:** during weekly project monitoring.
- **Process Improvement Ideas:** during early analysis and option evaluation.
- **Project Planning Chain:** when converting an approved goal into a work plan.
- **Acceptance Criteria Draft:** after a user story is agreed in principle.

## Short Example Outputs

### Example 1 - Decision-Ready Meeting Brief

- The pilot is confirmed for 200 users starting Monday.
- The updated onboarding flow is still pending; its deadline is not specified.
- The support FAQ has no assigned owner and must be resolved before launch.

### Example 2 - Timeline Change Email

**Subject: Updated Project Deadline**

Hello Team,

Please note that the project deadline has moved from September 15, 2026 to September 25, 2026 due to a technical delay. Please update your plans accordingly and raise any confirmed dependency concerns through the project channel.

Best regards,  
Hajar
