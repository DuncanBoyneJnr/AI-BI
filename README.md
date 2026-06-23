# AI-BI

AI prompts, how-tos and tooling for working on Power BI with an AI agent in the loop.

This is the companion repo to my talks — a place to grab the prompts and links I reference on stage. Everything here is what I actually use on real delivery work.

— [Duncan Boyne](https://www.linkedin.com/in/duncanboyne/)

---

All prompts are model-agnostic — paste them into Claude, ChatGPT, Copilot, or anything that takes text. They get sharper when the agent is connected to your model (see [the toolkit](#the-toolkit)).

## Review prompts

"Expert reviewer" prompts. Each puts the model in a specific role and runs a formal review of one layer of a Power BI solution.

| # | Prompt | Reviews | Give it |
|---|--------|---------|---------|
| 1 | [Power Query Review](prompts/01-power-query-review.md) | M code, transformations, refresh strategy | Your Power Query (M) |
| 2 | [DAX Review](prompts/02-dax-review.md) | Measures, calc columns, calc groups | Your DAX |
| 3 | [Documentation Review](prompts/03-documentation-review.md) | Specs, governance, data dictionaries | Your docs |
| 4 | [UI, UX & Accessibility Review](prompts/04-ui-ux-accessibility-review.md) | Layout, UX, WCAG accessibility | Screenshots / wireframes |
| 5 | [Does This Fit The Brief?](prompts/05-does-this-fit-the-brief.md) | Requirements vs delivered solution | Requirements + finished report |
| 6 | [Data Model Review](prompts/06-data-model-review.md) | Star schema, relationships, cardinality | Model diagram / live model |
| 7 | [Performance Optimisation](prompts/07-performance-optimisation.md) | Slow queries, model size, refresh | Performance Analyzer / live model |
| 8 | [Security & RLS Review](prompts/08-security-rls-review.md) | RLS, OLS, sharing, access | Roles, filter DAX, access config |

## Build & design prompts

Prompts that help you create rather than critique.

| # | Prompt | Does | Give it |
|---|--------|------|---------|
| 9 | [Measure From A Business Question](prompts/09-measure-from-business-question.md) | Turns plain English into correct, tested DAX | The question + your model |
| 11 | [Requirements To Spec](prompts/11-requirements-to-spec.md) | Turns messy discovery into a buildable spec | Notes / emails / transcripts |
| 12 | [Report Storyboard](prompts/12-report-storyboard.md) | Plans the report as a story before you build | Audience + metrics + constraints |
| 13 | [Model Documentation Generator](prompts/13-model-documentation-generator.md) | Generates a living data dictionary | Model objects / live model |

## Figma MCP workflow prompts

Prompts for moving from a rough dashboard idea into Figma and then into a buildable Power BI report.

| # | Prompt | Does | Give it |
|---|--------|------|---------|
| 16 | [Dashboard Idea To Figma Wireframe](prompts/16-dashboard-idea-to-figma-wireframe.md) | Uses Figma MCP to turn a rough dashboard idea into wireframed report pages | Idea, audience, metrics, constraints + Figma file |
| 17 | [Figma Wireframe To Power BI Build Spec](prompts/17-figma-wireframe-to-power-bi-build-spec.md) | Converts an approved Figma wireframe into a Power BI build sheet | Figma frame + model context |
| 18 | [Figma Wireframe To Report Build Agent](prompts/18-figma-wireframe-to-report-build-agent.md) | Drives the actual report build from the approved Figma design | Figma frame + build spec + report/model access |

## Explain & communicate prompts

Prompts for understanding and for talking to stakeholders.

| # | Prompt | Does | Give it |
|---|--------|------|---------|
| 10 | [DAX Explainer](prompts/10-dax-explainer.md) | Explains a measure in layers, filter context and all | DAX you don't fully get |
| 14 | [Error Troubleshooter](prompts/14-error-troubleshooter.md) | Diagnoses an error and explains the fix | Error message + context |
| 15 | [Stakeholder Narrative](prompts/15-stakeholder-narrative.md) | Turns the numbers into a decision-ready story | Metrics + trends + audience |

👉 **[How to use the prompts](guides/how-to-use-the-prompts.md)** — the workflow, getting better results, and running them as a pre-sign-off sequence.

---

## The toolkit

The prompts work anywhere, but they get a lot sharper when the agent is connected directly to your model and your design system. The tools I use:

- **[pbi-cli](https://github.com/MinaSaad1/pbi-cli)** — connect an AI agent to a live semantic model: read/write measures, run DAX, export TMDL, document the model.
- **Power BI MCP** — model operations (tables, measures, relationships, traces) exposed as structured tools the agent can call.
- **Figma MCP** — bridge design and Power BI: pull layout/colour tokens, mock up report pages, keep styling on-brand.
- **[Deneb Visual Skill](https://github.com/DuncanBoyneJnr/Deneb-Visual-Skill)** — my Claude skill for building, adapting and debugging Deneb (Vega-Lite) custom visuals for Power BI.

👉 **[Full toolkit guide](guides/tools.md)** — what each tool does and when to reach for it.

---

## Repo structure

```
AI-BI/
├── README.md
├── prompts/
│   ├── 01-power-query-review.md
│   ├── 02-dax-review.md
│   ├── 03-documentation-review.md
│   ├── 04-ui-ux-accessibility-review.md
│   ├── 05-does-this-fit-the-brief.md
│   ├── 06-data-model-review.md
│   ├── 07-performance-optimisation.md
│   ├── 08-security-rls-review.md
│   ├── 09-measure-from-business-question.md
│   ├── 10-dax-explainer.md
│   ├── 11-requirements-to-spec.md
│   ├── 12-report-storyboard.md
│   ├── 13-model-documentation-generator.md
│   ├── 14-error-troubleshooter.md
│   ├── 15-stakeholder-narrative.md
│   ├── 16-dashboard-idea-to-figma-wireframe.md
│   ├── 17-figma-wireframe-to-power-bi-build-spec.md
│   └── 18-figma-wireframe-to-report-build-agent.md
└── guides/
    ├── how-to-use-the-prompts.md
    └── tools.md
```

---

## License

The prompts and guides here are free to use and adapt. A link back is always appreciated.
