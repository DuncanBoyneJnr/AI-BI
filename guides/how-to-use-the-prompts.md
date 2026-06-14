# How to use the review prompts

The five review prompts each play a different role on a delivery: data engineer, DAX architect, governance consultant, UX specialist, and the customer themselves. Run them as a sequence before sign-off, or pick the one that matches the question you're being asked.

---

## The basic loop

1. **Pick the prompt** for the layer you want reviewed.
2. **Give it the right material** — see the note at the top of each prompt file:
   - Power Query Review → paste the M code / query structure
   - DAX Review → paste measures, calculated columns, calc groups
   - Documentation Review → attach the docs / data dictionary
   - UI, UX & Accessibility → attach screenshots or wireframes
   - Does This Fit The Brief? → provide requirements + finished-report screenshots
3. **Paste the prompt, then the material**, and let it run.
4. **Read the output as a starting point, not gospel.** The score and the "challenge assumptions" framing are there to surface things you'd otherwise miss — you're still the consultant.

---

## Getting better results

**Give context up front.** Tell it the audience (board, ops team, finance), the maturity of the solution, and any constraints (Pro vs Premium, refresh windows, on-prem gateway). The prompts ask the model to be opinionated — context is what makes the opinions land.

**Feed it the real thing.** With [pbi-cli](tools.md#pbi-cli--talk-to-your-semantic-model) or the [Power BI MCP](tools.md#power-bi-mcp--model-operations-as-tools) connected, the DAX and Power Query reviews stop being "review this text I pasted" and become "review the model you're connected to" — which is a different class of answer. The agent can run the measure, check cardinality, and trace the query rather than reasoning from the code alone.

**Run them in order before a handover.** Power Query → DAX → Documentation → UI/UX → Does This Fit The Brief gives you a full pre-sign-off pass: build quality, then calculation quality, then governance, then experience, then "did we actually deliver what was asked".

**Use the scores to track progress, not to judge.** Re-run after you've actioned the quick wins and watch the score move. It's a useful before/after for stakeholders.

---

## Where these came from

I use these in real delivery work and in my talks. They're deliberately ruthless — the "Does This Fit The Brief?" prompt is written to protect the customer, not the developer, on purpose. If a review feels uncomfortable, that's usually the point.
