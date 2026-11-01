# FACTR Agile

Version 0.1.0. Decompose product or system scope and refine epics, features, stories, and acceptance criteria using FACTR Core's behavioral methodology.

FACTR Agile is a separate product with one [entry skill](skills/factr-agile/SKILL.md). SPLIT supplies decomposition and allocation reasoning; SHAPE supplies backlog refinement. Neither is a prerequisite stage for the other. Direct story refinement, decomposition alone, and combined decomposition/refinement are supported.

## Example requests

- “Decompose these product notes into cohesive feature slices; label assumptions.”
- “Refine this feature into stories and observable acceptance criteria.”
- “Propose subsystem responsibility allocations from these requirements; ownership is not yet decided.”
- “Compare these two interpretations and draft the supported alternatives.”

Outputs preserve concrete rules, source references, inference labels, and material open decisions. Agile does not require a separate FACT Set, approved decomposition, or formal source authority for provisional work. An expected acceptance result is not observed evidence.

## Package

The skill bundles an exact versioned Core contract and conditional formal-conclusion guidance. [core-provenance.json](core-provenance.json) records the source revision and file hashes. Core need not be installed separately. Decomposition, shaping, and illustrative examples are conditional references.

The plugin and local marketplace have their own `factr-agile` identities. Agile and Test have separate workflows; this package contains no Test integration.

## Local registration

From this repository root, register the marketplace:

```powershell
codex plugin marketplace add .
```

Then open the plugin browser in your host, find FACTR Agile, and install and enable it. Start a new chat or CLI session after installation. Invoke the skill as `$factr-agile`, or select the plugin/skill with `@` where supported.

Registration and installation are user actions; creating this package does not register or enable it. See the [official OpenAI plugin documentation](https://developers.openai.com/codex/plugins) for host behavior. Package validation does not confirm installation in a particular host.

## Development checks

The evaluation, scripts, and tests folders are local development material excluded from Git. The commands below apply when those folders are present. Python 3 is sufficient for the package checks; the plugin itself requires no Python runtime or build.

```powershell
python scripts/check_package.py
python -m unittest discover -s tests -v
```

When the Core source checkout is available, verify synchronization as well:

```powershell
python scripts/check_package.py --core-source ../factr-core
```

Run the available skill-creator `scripts/quick_validate.py` against `skills/factr-agile` after editing skill instructions. That tool needs PyYAML. It checks skill structure, not reasoning quality.

Local evaluation cases in `evaluation/cases.json` specify realistic requests and behavioral review criteria. They are development material and are never a prerequisite for ordinary Agile use. Live model and host evaluation remain separate from the structural checks; no latency or reasoning-quality improvement is claimed from this package alone.
