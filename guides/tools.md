# The toolkit

The prompts in this repo are model-agnostic — they work in Claude, ChatGPT, Copilot, or anywhere you can paste text. But the real leverage comes from connecting the model directly to your Power BI work so it can read your model, write code, and build visuals instead of guessing from screenshots.

These are the tools I actually use.

---

## pbi-cli — talk to your semantic model

A command-line interface that connects an AI agent to a live Power BI / Analysis Services semantic model. Once connected, the model can read tables, columns, measures and relationships, run DAX queries, write measures, export/import TMDL, and document the whole thing.

- **Repo:** https://github.com/MinaSaad1/pbi-cli

What it unlocks:
- DAX written and tested against the real model, not invented in a vacuum
- Whole-model documentation and data dictionaries in seconds
- Version control for semantic models via TMDL export
- RLS, perspectives, partitions and refresh logic managed from the terminal

I drive this through a set of Claude skills that wrap the CLI, so I can ask in plain English ("add a YoY measure", "document this model", "trace the slow query") and the agent runs the right commands.

---

## Power BI MCP — model operations as tools

The Power BI Modeling MCP server exposes model operations (tables, columns, measures, relationships, DAX queries, partitions, security roles, traces) as structured tools the model can call directly. Where pbi-cli is a terminal workflow, the MCP server lets the agent operate the model natively as part of a conversation.

- **Docs:** Microsoft Learn — search "Power BI modeling MCP" / Analysis Services tabular model
- Use it when you want the agent to make structured, validated changes to the model rather than running raw CLI commands.

---

## Figma MCP — design ↔ Power BI

The Figma MCP server bridges code and design in both directions. For Power BI work I use it to:
- pull a design-system layout, spacing and colour tokens out of Figma to drive a report theme
- mock up report pages and dashboard layouts before building them
- keep report styling consistent with a wider brand system

- **Docs:** https://www.figma.com/ (Figma MCP / Dev Mode)

---

## Deneb Visual Skill — custom Vega-Lite visuals

My own Claude skill for generating, adapting, debugging and explaining Deneb (Vega-Lite) visuals for Power BI — tooltips, formatting, interactivity, cross-highlighting, and safe templates, including editing `visual.json` files directly in PBIR projects.

- **Repo:** https://github.com/DuncanBoyneJnr/Deneb-Visual-Skill

Reach for this when Power BI's built-in visual library can't render what you need and a custom visual is overkill.
