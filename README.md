# AI-BI

AI prompts, how-tos and tooling for working on Power BI with an AI agent in the loop.

This is the companion repo to my talks — a place to grab the prompts and links I reference on stage. Everything here is what I actually use on real delivery work.

— [Duncan Boyne](https://www.linkedin.com/in/duncan-boyne/)

---

## Review prompts

A set of five "expert reviewer" prompts. Each one puts the model in a specific role and runs a formal review of one layer of a Power BI solution. They're model-agnostic — paste them into Claude, ChatGPT, Copilot, or anything that takes text.

| # | Prompt | Reviews | Give it |
|---|--------|---------|---------|
| 1 | [Power Query Review](prompts/01-power-query-review.md) | M code, transformations, refresh strategy | Your Power Query (M) |
| 2 | [DAX Review](prompts/02-dax-review.md) | Measures, calc columns, calc groups | Your DAX |
| 3 | [Documentation Review](prompts/03-documentation-review.md) | Specs, governance, data dictionaries | Your docs |
| 4 | [UI, UX & Accessibility Review](prompts/04-ui-ux-accessibility-review.md) | Layout, UX, WCAG accessibility | Screenshots / wireframes |
| 5 | [Does This Fit The Brief?](prompts/05-does-this-fit-the-brief.md) | Requirements vs delivered solution | Requirements + finished report |

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
│   └── 05-does-this-fit-the-brief.md
└── guides/
    ├── how-to-use-the-prompts.md
    └── tools.md
```

---

## License

The prompts and guides here are free to use and adapt. A link back is always appreciated.
