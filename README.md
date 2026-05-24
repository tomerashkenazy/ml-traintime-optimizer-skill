# ML Training Timing Optimizer Skill

This repository contains a Codex skill for exploring machine-learning model training runtime optimizations under strict experiment-preservation constraints.

The skill is designed for repeated timing work:

- explore one simple runtime idea at a time
- benchmark first on local hardware
- track tested ideas to avoid repetition
- inspect and generate cluster/Slurm timing jobs for promising ideas
- keep recommendations separate from exploration
- require stronger validation for risky candidates

The current scripts were developed using the `ares` adversarial training repo, but the structure is useful for other training projects that need careful timing experiments across local and cluster hardware. To adapt it, update the repo contract, protocol definitions, dataset paths, environment names, and Slurm targets.

## Included Files

```text
training-runtime-optimizer/
├── SKILL.md
├── agents/openai.yaml
├── references/
└── scripts/
```


## Install

Copy `training-runtime-optimizer/` into your Codex skills directory or into a repo-local `.agents/skills/` directory.

Example:

```bash
mkdir -p /path/to/project/.agents/skills
cp -R training-runtime-optimizer /path/to/project/.agents/skills/
```

Then update the reference files and script constants for the target training repo.

## Notes

This skill is a workflow for controlled runtime research where preserving the training protocol matters most.
