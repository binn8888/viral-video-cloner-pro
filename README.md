> 🌐 Language / 语言：**[English](./README.md)** | [简体中文](./README.zh-CN.md)

# Viral Video Cloner Pro

> Open-source Codex Skill workflows for planning e-commerce short-form video projects.

Viral Video Cloner Pro is a self-hosted collection of Codex Skill definitions for structured e-commerce video planning. The repository currently provides workflow instructions and Codex metadata only. It does **not** contain a runnable video-generation application or a provider inference integration.

## Project Status

### Implemented today

The current repository contains two Codex Skills:

| Skill | Codex invocation | Current scope |
|---|---|---|
| Viral-video analysis and adaptation workflow | `$ecommerce-viral-video-clone-hybrid` | Guides reference analysis, narrative adaptation, shot planning, prompt preparation, compliance review, quality checks, and delivery organization. |
| Original e-commerce video planning workflow | `$ecommerce-video-original-pure` | Guides original concept development, script planning, shot design, prompt preparation, audio and subtitle planning, compliance review, and delivery organization. |

The implemented artifacts are declarative `SKILL.md` instructions and `agents/openai.yaml` metadata. They help Codex organize a human-reviewed planning process; they do not invoke video models or render media.

### Not implemented

The following capabilities are **not present in the current codebase**:

- Python application code
- FastAPI services or HTTP endpoints
- OpenCV processing
- Image2-Storyboard processing
- Seedance 2.0 API or model adapters
- Automated image or video inference
- Batch rendering or final-video export
- A deployable local video-generation service

These items appear only in the Roadmap below.

## Repository Structure

```text
viral-video-cloner-pro/
├── ecommerce-viral-video-clone-hybrid/
│   ├── SKILL.md
│   └── agents/
│       └── openai.yaml
├── ecommerce-video-original-pure/
│   ├── SKILL.md
│   └── agents/
│       └── openai.yaml
├── LICENSE
├── README.md
└── requirements.txt
```

`requirements.txt` is a roadmap-only planning document. It is not an installation manifest for a working Python application.

## Installation

Clone the repository and copy either or both Skill directories into the local Codex Skills directory:

```bash
git clone https://github.com/binn8888/viral-video-cloner-pro.git
mkdir -p ~/.codex/skills
cp -R viral-video-cloner-pro/ecommerce-viral-video-clone-hybrid ~/.codex/skills/
cp -R viral-video-cloner-pro/ecommerce-video-original-pure ~/.codex/skills/
```

Restart Codex or begin a new task so the Skill list can refresh.

## Usage

Invoke a Skill in Codex:

```text
$ecommerce-viral-video-clone-hybrid
```

or:

```text
$ecommerce-video-original-pure
```

Then provide the project brief, product information, audience, platform, target duration, and any authorized reference material requested by the selected workflow.

The Skills produce planning guidance and structured production instructions. Any external media-generation step requires separate tools, accounts, authorization, and human approval.

## Responsible Use

“Cloning” in this repository means analyzing and adapting high-level narrative structure, pacing, and shot function. It does not authorize copying protected footage, complete scripts, personal likenesses, trademarks, or other third-party assets.

Users are responsible for:

- obtaining rights to all input and reference material;
- reviewing advertising, platform, and regional compliance requirements;
- validating generated prompts and production plans before using external tools; and
- completing human review before publishing any media.

## Roadmap

The following items are proposals, not implemented features:

1. **Image2-Storyboard specification** — define an input contract for interpreting a single narrative storyboard canvas.
2. **Seedance 2.0 adapter design** — research a provider-neutral adapter boundary and configuration model.
3. **Python project foundation** — evaluate typed models, validation, tests, and command-line tooling.
4. **FastAPI service prototype** — explore local API boundaries after the data contracts are reviewed.
5. **OpenCV utilities** — evaluate optional storyboard inspection and media validation helpers.
6. **Parameter tuning module** — define reproducible configuration profiles and reviewable parameter changes.
7. **Local deployment documentation** — document installation and operation only after a runnable implementation exists.
8. **Batch rendering and export** — investigate only after provider integration, safety controls, and tests are available.

Roadmap work will be tracked through public issues. A roadmap item is not considered implemented until code, tests, and documentation are merged into the repository.

## Codex API Usage Statement

Any Codex or OpenAI API credits granted through the Codex for Open Source program will be used exclusively to maintain this public open-source repository. Eligible maintenance work includes:

- iterating on Codex Skill YAML metadata and workflow definitions;
- triaging and responding to repository issues;
- writing and reviewing documentation;
- reviewing configuration changes; and
- supporting pull-request, release, and other core repository-maintenance workflows.

Credits will **not** be used for commercial video generation, video-model inference, final-media production, paid client work, or operating a commercial content-generation service.

This statement reflects the repository's current public scope and is intended to remain aligned with the Codex for Open Source application.

## Maintenance

`binn8888` is the repository owner and primary maintainer. Maintenance includes issue triage, focused Skill and YAML updates, documentation review, configuration review, and versioned releases when changes are ready.

Contributions should describe the current behavior accurately, keep implemented capabilities separate from Roadmap proposals, and avoid claims that cannot be verified from the public repository.

## Contributing

1. Open an issue describing the proposed change.
2. Keep changes focused on Codex Skill workflows, metadata, documentation, or clearly labeled Roadmap design work.
3. Validate edited YAML before submission.
4. Explain how the change preserves the boundary between current functionality and future plans.
5. Submit a pull request for maintainer review.

## License

This project is licensed under the [MIT License](LICENSE).
