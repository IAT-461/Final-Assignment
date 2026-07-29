**Format:** Individual. Every student plays two roles across the project: 

- **Client**: You will define a problem that will be assigned to another student.
- **Data Scientist**: You will solve a problem defined by another student that is assigned to you. 

You will never solve your own proposal.

## Learning Goals
- Practice defining a tractable data science problem from a stakeholder's point of view (Client role).
- Choose and justify the right technique — prediction vs. pattern discovery — based on the problem and data type, rather than being told which to use (Data Scientist role).
- Work across both structured/tabular data and text data.
- Practice evaluating a delivered solution against original business needs (Client role, second pass).

---

## Timeline

| Date | Milestone |
|---|---|
| **Tue Jul 21** | Client proposal due |
| **Wed Jul 22** | Projects are assigned to students (instruction team reviews proposals and resolves conflicts) |
| **Wed Aug 5** | Checkpoint 1 — EDA on dataset. Submitted to instructor **and** shared with your assigned Client |
| **Thu Aug 6** | Client Check-in — Client responds to Checkpoint 1 with brief feedback |
| **Sun Aug 9** | Checkpoint 2 — Problems substantially modeled; draft notebook submitted to instructor only |
| **Tue Aug 11** | Final delivery — Notebook + recorded presentation (+ optional Streamlit link) delivered to your Client and the instructor |
| **Wed Aug 12 – Wed Aug 14** | Client Evaluation window |
| **Fri Aug 14** | Client Evaluation report due |
| **Sun Aug 16, 11:59pm** | Final revisions (optional, based on Client feedback) + all materials due |

---

## Phase 1 — Client Proposal (due Jul 22)

Each student acts as a client. You are tasked with defining a problem for an entity you care about — real or fictional — that will be assigned to another student. **You will not know who receives your proposal or whose problem you are assigned until assignments are released on July 22.**

### Required Sections on Your Proposal

1. **Entity**: Name and a one-paragraph description. Real or fictional; if fictional, ground it in a plausible industry context.
2. **Problem Definition**: A specific business or policy question answerable using structured/tabular or text data. Word it precisely enough that a data scientist reading it can determine, without being told, whether it calls for *predicting an outcome* (supervised) or *finding structure with no predefined outcome* (unsupervised). Vague phrasing like "help us understand our customers" is unacceptable because it could imply either approach.
3. **Stakeholder / Audience**: Define who within the entity will use the answer and what specific decision it informs.
4. **Datasets** (Provide one of the following):
   - An attached file (CSV/JSON for tabular; plain text/CSV for text) with a **minimum of 200 rows** and an accompanying column dictionary, OR
   - A link to a verified public dataset that you have personally confirmed loads properly and fits the problem, OR
   - A synthetic dataset you generated yourself using a seeded RNG (include the generation script).

   *Note: No proposal may rely on data that does not exist yet or that you have not personally verified as usable.*
5. **Success Criteria**: 2–3 sentences (or a short paragraph) detailing what a good answer looks like from the stakeholder's perspective. If the problem is prediction-based, specify what decision the prediction should support. If it is discovery-based, describe what kind of pattern would be actionable or useful.
6. **Constraints (Optional)**: Known data quality issues, sensitive variables to handle carefully, or scope boundaries.

**Length:** 1–2 pages. Submit as a PDF.

**Contingency:** If your proposal is late, incomplete, or fails the data accessibility check, the instructor will substitute a proposal from a reserve pool so your assigned Data Scientist is not delayed. This penalty applies strictly to the late/incomplete Client, not the Data Scientist.

---

## Phase 2 — Assignment (Jul 27)

Assignments are randomized (one proposal per student; no self-assignments). The instruction team will review all proposals to ensure appropriate depth and workload, while resolving any conflicts (e.g., a dataset failing accessibility checks).

---

## Phase 3 — Data Scientist Deliverables (Jul 27 – Aug 11)

Working on your **assigned** client proposal:

1. **Analyze and Justify:** Read the problem statement, decide whether each component calls for a prediction task (supervised) or a pattern-discovery task (unsupervised), and justify your choice in writing based on the data and business question — not simply because the client suggested it.
   - **If supervised:** Build and evaluate the model using metrics appropriate to the task (e.g., precision, recall, F1, ROC-AUC for classification; RMSE, $R^2$ for regression). Interpret these metrics against the stakeholder's success criteria rather than just reporting the raw numbers.
   - **If unsupervised:** Build the model and interpret the findings by explaining what the resulting clusters or structures mean for the stakeholder in light of their success criteria. Report a validity metric (e.g., silhouette score), but treat it as an exploratory guide rather than a final verdict.
2. **Execute Problem Components:** Address required sub-problems/data types (e.g., structured/tabular analysis and text analysis) as outlined in the client proposal.
3. **Client Check-in (Checkpoint 1 — Due Jul 31 / Feedback by Aug 3):** Send your assigned Client a short update detailing your Exploratory Data Analysis (EDA) findings, the direction (supervised vs. unsupervised) you are taking for each problem, and your rationale. Keep it concise; this is a quick sanity check, not a full design review.
4. **Assumptions Log:** Document any assumptions you made where the client proposal was ambiguous or incomplete, particularly prior to the Aug 3 check-in.

### What Goes in the Jupyter Notebook
*(Note: Every step must be annotated using Markdown text, not just raw code cells)*

- **Title & Overview:** Title plus your restatement of both problems in your own words.
- **Data Loading & Documentation:** Data source, column dictionary, and known data quality issues.
- **Exploratory Data Analysis (EDA):** Feature distributions, missing value handling, and key relationships.
- **Problems Sections:** Technique selection + justification, modeling, and evaluation/interpretation as outlined above.
- **Assumptions Log:** List of initial ambiguities and how you resolved them.
- **Limitations:** What you would do differently given more time, computational resources, or higher-quality data.
- **Executive Summary:** A plain-language summary tailored for the business stakeholder rather than the course instructor.
- **Links:** Direct links to your recorded video presentation and your Streamlit app (if applicable).

### Presentation
A **5-minute recorded video** walking a non-technical stakeholder through both problems, your methodology, and your key findings. A clean screen recording of your notebook with voiceover is completely acceptable; high production polish is not required.

### Streamlit App (Bonus)
*Optional.* If you build an interactive Streamlit web app allowing the stakeholder to explore your findings or test model predictions interactively, you can earn up to **+10% bonus points**.

---

## Phase 4 — Client Evaluation (Aug 12–14)

You return to being the Client for the proposal you originally wrote. Review the notebook and watch the presentation.

### Evaluation report (~300–400 words + ratings)

Rate each 1–5, with one or two sentences justifying each score:

| Criterion | What you're judging |
|---|---|
| Answered Problem Sections | Does it address your questions as you posed them? |
| Technique judgment | Did they choose a defensible approach (supervised/unsupervised) given how you worded the problem? |
| Evaluation/interpretation quality | Are the metrics (supervised) or the interpretation (unsupervised) actually connected back to your success criteria? |
| Communication | Is the presentation and notebook summary understandable to your stakeholder, not just to another data scientist? |

Plus one paragraph of open-ended feedback.

**This is not a peer grade.** It's evidence the instructor uses when grading the solution — it does not set the numeric grade directly, so be honest rather than generous or harsh.

---

## Grading

| Component | Weight |
|---|---|
| Client Proposal (Phase 1) | 15% |
| Notebook + Presentation (Phase 3) | 55% |
| Client Evaluation Report (Phase 4, judged on rigor of your evaluation, not positivity) | 15% |
| Checkpoints and Client Check-in met on time | 15% |
| Streamlit app | +10% bonus |
| Using creative techniques or advanced models in solving the problem | +5% bonus |
| Creating an interesting dataset requiring clever data science work | +5% bonus |

---

## Example Client Proposals

Before we see some examples of the types of proposals we have in mind, you might have this question:

"How should I balance the difficulty, volume, and complexity of the proposal I'm going to create?"

First of all, we review all proposals, and if we feel one is too simple or too difficult/time-consuming, we'll give feedback so you can revise it.
However, we strongly recommend and encourage you to keep the following goal in mind when writing your proposal and finding/generating a dataset for it:
Your proposal should motivate and encourage another student to explore and practice the concepts they've learned in the course so far.

Therefore, if it's too simple (with no real challenge), it won't be engaging enough. On the other hand, if it's too difficult and complex, it will be overwhelming and discouraging.

Put yourself in the position of a caring manager or team lead who wants to assign a task to a teammate. It's important to you that the task solves a real problem, is challenging enough to encourage learning, and is not so heavy that it overwhelms them or takes over their life.

Your proposals can be similar to the subquestions we gave you in Question 4 of the midterm (with the difference that here you are expected to not only explain your strategy for solving the problem, but also build a complete data pipeline). However, they should have a bit more complexity.

For example, if you choose to define a problem with a tabular dataset, your dataset (or the combined total of your datasets if the problem involves more than one) should have at least 7-8 columns, and finding the patterns should require one or two stages of feature engineering (meaning the patterns should not be directly discoverable from the raw dataset).

*Note*: You will receive a 5% bonus for including more advanced data types (e.g. GeoJSON, GraphML, XML, KML) or encouraing your peers to use topics you have learned more recently in the course (topics not covered in first 3 assignments).

Nevertheless, these model the format and specificity expected - not templates to copy:

# Example 1: Roast Collective — Subscriber Retention Strategy

**Entity:** A 6-location specialty coffee subscription roaster managing a direct-to-consumer monthly bean delivery program.

**Business Context & Strategic Options:** Monthly recurring revenue (MRR) has plateaued over the last two quarters, and management is considering three strategic interventions to restore growth:

- **Option A:** Launch a broad paid advertising campaign to acquire new subscribers.
- **Option B:** Cross-sell high-end espresso equipment add-ons to existing subscribers.
- **Option C:** Offer targeted retention discounts to subscribers who are at high risk of canceling.

**The Task:**

- **Phase 1 (EDA & Strategy Validation):** Using the provided dataset, conduct an exploratory analysis to evaluate the financial viability and behavioral support for Options A, B, and C. Identify which option the data justifies pursuing.
- **Phase 2 (Data Science Implementation):** Assuming management proceeds with Option C, predict which currently-active subscribers will cancel in the next billing cycle, using order frequency, roast preferences, tenure, and support-ticket history.

**Dataset Provided:** `subscribers_dataset.csv` (1,800 subscriber records including account tenure, order frequency, bean preference vectors, delivery delay flags, historical CAC, equipment purchase history, and cancellation records).

**Success Criteria:** A clear EDA section demonstrating why two of the options are unfeasible, followed by a risk score precise enough that a targeted campaign to the top-risk decile would be worth the spend.

---

# Example 2: Roast Collective — Customer Support Friction Analysis

**Entity:** A 6-location specialty coffee subscription roaster managing a direct-to-consumer monthly bean delivery program.

**Business Context & Strategic Options:** Customer support ticket volume has surged by 40%, placing severe strain on operations. Management is debating three solutions:

- **Option A:** Hire three additional full-time support agents to clear the queue.
- **Option B:** Implement a static FAQ chatbot to deflect incoming inquiries.
- **Option C:** Re-evaluate and resolve root customer complaints by discovering actual friction points rather than relying on existing ticket categories.

**The Task:**

- **Phase 1 (EDA & Strategy Validation):** Using the provided dataset, conduct an exploratory analysis of support volume, resolution times, and customer retention patterns to evaluate Options A, B, and C. Identify which option the data justifies pursuing.
- **Phase 2 (Data Science Implementation):** Assuming management proceeds with Option C, group our last 12 months of customer support chat transcripts by underlying issue, without using our existing ticket-category tags, so we can see whether our categories still match what customers actually complain about.

**Dataset Provided:** `support_chat_transcripts.json` (600 multi-turn conversation logs spanning 12 months, including timestamps, customer tenure, fulfillment metadata, and existing tag IDs).

**Success Criteria:** A clear EDA section demonstrating why two of the options are unfeasible, followed by issue groupings a support manager could use to check whether the existing ticket taxonomy is stale.

---

# Example 3: Vancouver Tool Library — First-Year Member Renewal Strategy

**Entity:** A non-profit community tool-lending library offering access to specialized hardware, woodworking tools, and garden equipment funded by annual memberships.

**Business Context & Strategic Options:** First-year member retention has dropped to 42%, threatening long-term solvency. The board is debating three proposals:

- **Option A:** Increase annual membership fees by 25% to make up for lost revenue.
- **Option B:** Host monthly social and networking events to build a stronger community atmosphere.
- **Option C:** Launch an early-intervention outreach program targeting new members showing signs of low engagement in their first 90 days.

**The Task:**

- **Phase 1 (EDA & Strategy Validation):** Using the provided dataset, conduct an exploratory analysis of member engagement, event attendance, and renewal behavior to evaluate Options A, B, and C. Identify which option the data justifies pursuing.
- **Phase 2 (Data Science Implementation):** Assuming management proceeds with Option C, predict which members will fail to renew after their first year, using checkout frequency, tool categories borrowed, and event attendance in the first 90 days.

**Dataset Provided:** `vtl_membership_log.csv` (900 first-year member records capturing early activity metrics, event attendance types, checkout categories, and Year 1 renewal outcomes).

**Success Criteria:** A clear EDA section demonstrating why two of the options are unfeasible, followed by a defensible story about first-90-day behaviors that predict renewal, usable in a board presentation.

---

# Example 4: Vancouver Tool Library — Exit Survey Theme Extraction

**Entity:** A non-profit community tool-lending library offering access to specialized hardware, woodworking tools, and garden equipment funded by annual memberships.

**Business Context & Strategic Options:** Member churn remains high, and leadership is deciding how to allocate their annual capital budget:

- **Option A:** Spend funds to extend weekend operating hours by four hours.
- **Option B:** Purchase duplicate inventory for high-demand tools (e.g., pressure washers).
- **Option C:** Overhaul member policies based on qualitative member feedback from departing members.

**The Task:**

- **Phase 1 (EDA & Strategy Validation):** Using the provided dataset, analyze tool utilization rates, reservation wait times, and operating logs to evaluate Options A, B, and C. Identify which option the data justifies pursuing.
- **Phase 2 (Data Science Implementation):** Assuming management proceeds with Option C, identify the main themes members raise in their end-of-membership exit surveys, without assuming our current three-option "reason for leaving" dropdown captures what's actually going on.

**Dataset Provided:** `vtl_exit_data.csv` (Tool usage logs, wait-time records, structured survey choices, and 400 free-text exit survey responses).

**Success Criteria:** A clear EDA section demonstrating why two of the options are unfeasible, followed by themes specific enough to suggest an actual policy change, not "members want more tools."

---

# Example 5: PixelForge Games — High-Value Contributor Identification

**Entity:** An independent game studio running an active Discord and Twitch community around an online multiplayer title.

**Business Context & Strategic Options:** Community activity drops sharply 30 days post-launch, impacting overall player retention. Studio leadership is considering three initiatives:

- **Option A:** Run paid influencer Twitch streams to continuously bring in new casual players.
- **Option B:** Lower in-game difficulty to make the game more accessible to casual players.
- **Option C:** Launch an invite-only "Community Ambassador Program" where core members moderate events, guide newcomers, and host community matches.

**The Task:**

- **Phase 1 (EDA & Strategy Validation):** Using the provided dataset, conduct an exploratory analysis on player telemetry and community engagement to evaluate Options A, B, and C. Identify which option the data justifies pursuing.
- **Phase 2 (Data Science Implementation):** Assuming management proceeds with Option C, predict which community members are likely to become long-term active contributors (vs. one-time posters), using account age, post frequency, and reaction counts in their first two weeks.

**Dataset Provided:** `discord_member_activity.csv` (1,000 user records tracking early engagement metrics, post/reaction frequencies, channel diversity, and long-term contributor markers).

**Success Criteria:** A clear EDA section demonstrating why two of the options are unfeasible, followed by a shortlist the community manager could realistically reach out to.

---

# Example 6: PixelForge Games — Twitch Patch Sentiment Analysis

**Entity:** An independent game studio running an active Discord and Twitch community around an online multiplayer title.

**Business Context & Strategic Options:** Following major balance patches, developer Twitch streams are flooded with intense chat feedback, leaving team leaders divided on how to react:

- **Option A:** Immediately roll back all recent patch balance changes.
- **Option B:** Put Twitch chat into "Subscriber-Only / Slow Mode" to suppress chat volume.
- **Option C:** Analyze patch-day stream chat logs to determine what specific game elements drive community reactions and sentiment.

**The Task:**

- **Phase 1 (EDA & Strategy Validation):** Using the provided dataset, analyze post-patch player retention and chat demographic distribution to evaluate Options A, B, and C. Identify which option the data justifies pursuing.
- **Phase 2 (Data Science Implementation):** Assuming management proceeds with Option C, surface the topics and sentiment patterns in our Twitch chat logs around patch-release days, without a predefined list of topics, so the community manager can see what actually drives reaction.

**Dataset Provided:** `twitch_patch_chat_logs.csv` (Player session telemetry, timestamps, user badges, moderation flags, and raw Twitch chat message logs).

**Success Criteria:** A clear EDA section demonstrating why two of the options are unfeasible, followed by a weekly-checkable view of what's driving chat sentiment, not a one-off report.
