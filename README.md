# Financial Aid Office Workflow

**A free Claude workflow plugin by [Revuity Systems](https://revuitysystems.com).**

![Financial Aid Office Workflow plugin icon](assets/icon-128.png)

A free Claude plugin for organizing recurring financial aid office work without replacing institutional judgment. It helps authorized staff structure case review, queue management, missing-information follow-up, student communication drafts, verification preparation, appeals, professional-judgment preparation, loan-processing checklists, reconciliation preparation, and recurring office reviews.

- Plugin name: `financial-aid-office`
- Skill: `/financial-aid-office:financial-aid-operations`
- Version: 1.0.0
- License: MIT

## Plugin icon

The plugin icon ships in the assets folder in 512, 256, and 128 pixel versions. The manifest references it with the icon field, which Anthropic's directory reads for the plugin listing and Claude Code ignores at load time.

## Good for

- Case and queue review
- Missing-information follow-up
- Student communication drafts
- Verification and conflicting-information preparation
- Appeal and professional-judgment preparation
- Loan-processing checklists
- Award-year transition checklists
- Reconciliation and closeout preparation
- Daily and weekly operations reviews

## How it works

The plugin separates known facts, missing information, next actions, deadlines, owners, escalation conditions, and human decisions. It helps a financial aid team move work from intake to documented resolution while preserving the institution's policies, approval structure, and regulatory responsibilities. Every case or queue summary names its sources, what is still missing, who owns the next step, and which decisions belong to a person.

## Example requests

Once the plugin is loaded, ask in plain language or invoke the skill directly with `/financial-aid-office:financial-aid-operations`.

- "Review this queue of open files and tell me what is blocked, what is aging, and what needs a staff decision."
- "Draft a missing-document follow-up for this student based on our checklist, and give me the internal tracking note and follow-up date."
- "Prepare an approval-ready brief for this professional-judgment request using the criteria I have pasted below."
- "Give me a weekly financial aid operations review from this export."

You supply the information, either by pasting it in or through tools you have already connected to Claude. The plugin does not collect data of its own, does not call any Revuity service, and has no executable code.

## Authority and safety boundaries

The plugin assists workflow execution and preparation. It does not independently make regulated eligibility determinations, override institutional policy, invent compliance requirements, certify awards, move money, or send consequential communications without appropriate authorization. When current policy or regulatory requirements matter, it directs you to the institution's governing source or another authorized current source and stops at preparation when sources are missing or conflict. Final eligibility determinations, aid adjustments, professional-judgment decisions, loan certification or cancellation, money movement, and formal compliance certification stay with authorized people.

When something is missing, stale, or in conflict, the plugin is written to stop and say so rather than guess.

## Data handling

Use only the student data a task needs. The skill is written to avoid reproducing SSNs, full financial account numbers, passwords, authentication secrets, or unrelated sensitive identifiers, and to prefer institutional IDs or redacted references. Your institution's privacy and records policies still apply to anything you share with Claude.

## Install

This repository is a single Claude plugin with its manifest at `.claude-plugin/plugin.json` and its skill at `skills/financial-aid-operations/SKILL.md`.

To try it locally, clone the repository and start Claude Code with the plugin directory:

```bash
git clone https://github.com/revuitysystems/revuity-financial-aid-workflow.git
claude --plugin-dir ./revuity-financial-aid-workflow
```

Then run `/reload-plugins` and confirm `/financial-aid-office:financial-aid-operations` appears. To check the package without running it, use `claude plugin validate ./revuity-financial-aid-workflow`.

## Validation

A GitHub Actions workflow in this repository checks the manifest, semantic version, skill frontmatter, and required documentation on every push and pull request. See `.github/workflows/validate.yml`. Passing validation shows the package is well formed. It does not replace testing the plugin in your own Claude environment against your own policies.

## Built by Revuity Systems

Revuity Systems is an Operations Systems company. These public workflow plugins are free operating tools designed to make real work easier while demonstrating how Revuity thinks about roles, workflows, responsibility, authority, exceptions, outcomes, and operating cadence.

When an organization later needs the workflow adapted to its own systems, policies, data, approvals, integrations, or operating model, Revuity may help design or build that larger system. You do not need to talk to anyone to use this plugin.

More at [revuitysystems.com](https://revuitysystems.com). Questions or security concerns: info@revuitysystems.com.

## Privacy

This plugin does not collect or store data itself. Revuity's privacy policy is at [revuitysystems.com/privacy](https://revuitysystems.com/privacy).

## License

MIT. See [LICENSE](LICENSE).
