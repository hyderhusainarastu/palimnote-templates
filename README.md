# Palimnote Templates

Palimnote Templates is a catalog of process templates encoding hard-won operational discipline: an incident runbook template with mandatory non-evidence caveats, and a launch-campaign scaffold with default-deny claims/rights ledgers. Each template is usable standalone and lives in its own repository.

## Templates

| Template | Description |
| --- | --- |
| [incident-runbook-template](https://github.com/hyderhusainarastu/incident-runbook-template) | A fill-in-the-blanks incident runbook template that forces failure classification before log-reading and requires every ranked failure signature to carry an explicit non-evidence caveat |
| [launch-campaign-scaffold-kit](https://github.com/hyderhusainarastu/launch-campaign-scaffold-kit) | A directory scaffold and default-deny governance system for running a product, crowdfunding, or marketing launch: one JSON manifest describing the launch and its publication kill switch, claims and rights ledgers where nothing publishes until its row reads cleared, a plan-item-to-asset-to-ledger-row crosswalk, and two dependency-free Node tools for validating the manifest and checksumming an assets archive |

## Companions

`launch-campaign-scaffold-kit` pairs with the published [pre-publication-review-gate-checklist](https://github.com/hyderhusainarastu/pre-publication-review-gate-checklist) skill repo — run the review gate before flipping the launch manifest's kill switch.

## How to use

Copy the template file (or scaffold directory) from the individual repo into your own project, then fill in the `[[PLACEHOLDER]]` slots with your project's real values. Each template is self-contained and carries its own README with setup notes.

## Related catalogs

| Catalog | Description |
| --- | --- |
| [palimnote-skills](https://github.com/hyderhusainarastu/palimnote-skills) | Portable agent skills following the SKILL.md convention |
| [palimnote-tools](https://github.com/hyderhusainarastu/palimnote-tools) | Standalone tools and scripts |
| [palimnote-agent-patterns](https://github.com/hyderhusainarastu/palimnote-agent-patterns) | Reusable agent persona and orchestration patterns |

## License

CC-BY-4.0. Each repo in this catalog carries its own LICENSE file.
