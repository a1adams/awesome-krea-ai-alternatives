# Krea AI alternatives for generation, editing and reusable workflows

A maintained dataset of **krea ai alternatives** options: what each one connects to, where it stops, how to run it, and a link to the vendor's own pricing page rather than a price that will be wrong by the time you read it.

The tables below are generated from [`data/tools.json`](data/tools.json). Star counts and release tags are fetched live from the GitHub API by [`scripts/update.js`](scripts/update.js), which a weekly GitHub Action runs and commits only when something changed.

<!-- LAST-CHECKED:START -->
Live repository data last checked **2026-09-24** by [`scripts/update.js`](scripts/update.js), which runs weekly via GitHub Actions.
<!-- LAST-CHECKED:END -->

Maintained by [a1adams](https://github.com/a1adams). Corrections welcome — see [CONTRIBUTING.md](CONTRIBUTING.md).

## Contents

- [The data](#the-data)
- [Capability scores](#capability-scores)
- [The tools](#the-tools)
  - [Krea AI](#1-krea-ai)
  - [Wireflow](#2-wireflow)
  - [Flora AI](#3-flora-ai)
  - [Freepik Spaces](#4-freepik-spaces)
  - [Recraft](#5-recraft)
  - [ComfyUI](#6-comfyui)
- [Decision this list supports](#decision-this-list-supports)
- [Scope and evidence](#scope-and-evidence)
- [Selection notes](#selection-notes)
- [Acceptance recipe](#acceptance-recipe)
- [Evaluation record](#evaluation-record)
- [How this list is maintained](#how-this-list-is-maintained)
- [Contributing](#contributing)
- [License](#license)

## The data

One row per tool, one column per thing people actually check before committing. Columns with nothing verified behind them are dropped rather than filled with guesses.

<!-- DATA-TABLE:START -->
| Tool | Claude connection | REST API | Free tier | Model support | Pricing | Open-source SDK / MCP |
|---|---|---|---|---|---|---|
| **[Krea AI](#1-krea-ai)** | — | Yes | — | Image and video operations; model coverage varies | — | — |
| **[Wireflow](#2-wireflow)** | Hosted MCP; see official connector setup | Yes | [check](https://www.wireflow.ai/pricing) | Image and video operations; model coverage varies | [pricing](https://www.wireflow.ai/pricing) | — |
| **[Flora AI](#3-flora-ai)** | Hosted MCP with OAuth | Yes | — | Image and video operations; model coverage varies | — | — |
| **[Freepik Spaces](#4-freepik-spaces)** | Magnific hosted MCP; follow current official setup | Yes | — | Image and video operations; model coverage varies | — | — |
| **[Recraft](#5-recraft)** | — | Yes | — | Image operations; see documented model and format support | — | [recraft-ai/mcp-recraft-server](https://github.com/recraft-ai/mcp-recraft-server) — 60 ★, v1.6.5 |
| **[ComfyUI](#6-comfyui)** | — | Yes | — | Image and video operations; model coverage varies | — | [Comfy-Org/ComfyUI](https://github.com/Comfy-Org/ComfyUI) — 134,748 ★, v0.37.0 |
<!-- DATA-TABLE:END -->

## Capability scores

The score counts how many of the checks in [`data/tools.json`](data/tools.json) → `capabilityChecks` a tool passes. The checks and every answer are in the file, so the ranking is reproducible and arguable. Disagree with a cell? Open an issue naming the tool, the check and the evidence.

<!-- CAPABILITY-SCORES:START -->
| Tool | REST API | Visual graph | Image tools | Vector output | Score |
|------|---|---|---|---|-------|
| **[Krea AI](#1-krea-ai)** | ✅ | ✅ | ✅ | — | **3/4** |
| **[Wireflow](#2-wireflow)** | ✅ | ✅ | ✅ | — | **3/4** |
| **[Flora AI](#3-flora-ai)** | ✅ | ✅ | ✅ | — | **3/4** |
| **[Freepik Spaces](#4-freepik-spaces)** | ✅ | ✅ | ✅ | — | **3/4** |
| **[Recraft](#5-recraft)** | ✅ | — | ✅ | ✅ | **3/4** |
| **[ComfyUI](#6-comfyui)** | ✅ | ✅ | ✅ | — | **3/4** |
<!-- CAPABILITY-SCORES:END -->

## The tools

### 1. Krea AI

- **What it is:** Creative model APIs alongside a Nodes canvas for image, video and audio workflows.
- **Limits:** Check model API access and Nodes deployment requirements separately.
- **Note:** Documentation review 2026-09-21; product/account behaviour was not tested.
- **Links:**
  - [Homepage](https://www.krea.ai)
  - [Docs](https://www.krea.ai/docs/developers/introduction)
  - [Official source 2](https://www.krea.ai/docs/user-guide/features/nodes)
  - [Official source 3](https://www.krea.ai/docs/api-reference/node-apps/execute-a-node-app)
  - [Official source 4](https://www.krea.ai/docs/api-reference/image-enhance/krea-enhance)

Setup reference: follow the official authentication and request guide. This is a documentation URL, not an executed API example.
```text
https://www.krea.ai/docs/developers/introduction
```

### 2. Wireflow

- **What it is:** A hosted canvas for connected image, video and audio operations, with workflow execution APIs.
- **Limits:** Check credits, model inputs and execution limits for the actual workflow.
- **Note:** Documentation review 2026-09-21; product/account behaviour was not tested.
- **Links:**
  - [Homepage](https://www.wireflow.ai)
  - [Docs](https://www.wireflow.ai/docs)
  - [Pricing](https://www.wireflow.ai/pricing)
  - [Official source 1](https://www.wireflow.ai/docs/creating-workflows)
  - [Official source 2](https://www.wireflow.ai/docs/api/run)
  - [Official source 3](https://www.wireflow.ai/docs/mcp)
  - [Official source 4](https://www.wireflow.ai/docs/batch-image-generation)

Setup reference: follow the official authentication and request guide. This is a documentation URL, not an executed API example.
```text
https://www.wireflow.ai/docs
```

### 3. Flora AI

- **What it is:** A creative canvas with reusable Techniques, API access and a hosted MCP interface.
- **Limits:** A saved Technique must expose suitable inputs; check billing and account access before running it.
- **Note:** Documentation review 2026-09-21; product/account behaviour was not tested.
- **Links:**
  - [Homepage](https://flora.ai)
  - [Docs](https://developer.flora.ai/api/)
  - [Official source 2](https://developer.flora.ai/mcp/)
  - [Official source 3](https://developer.flora.ai/quickstarts/cli/)

Official CLI installation; this installs software but submits no generation:
```bash
go install github.com/florafauna-ai/flora-cli/cmd/flora@latest
```

### 4. Freepik Spaces

- **What it is:** Now part of Magnific: a shared image/video canvas alongside documented media APIs and MCP access.
- **Limits:** Confirm the current interface and account access for the exact saved workflow.
- **Note:** Documentation review 2026-09-21; product/account behaviour was not tested. The older indexed Apps API guide returned 404 after redirecting to Magnific on 2026-09-21. Current full-workflow REST execution was not established in this review; this is uncertainty, not a claim that the capability is absent.
- **Links:**
  - [Homepage](https://www.magnific.com/spaces)
  - [Docs](https://docs.magnific.com/introduction)
  - [Official source 3](https://www.magnific.com/blog/magnific-mcp-chatgpt/)

Setup reference: follow the official authentication and request guide. This is a documentation URL, not an executed API example.
```text
https://docs.magnific.com/introduction
```

### 5. Recraft

- **What it is:** APIs for raster and vector generation, image edits, background removal and upscaling.
- **Limits:** Select the output family and operation deliberately; editing and generation have different requirements.
- **Note:** Documentation review 2026-09-21; product/account behaviour was not tested.
- **Links:**
  - [Homepage](https://www.recraft.ai)
  - [Docs](https://www.recraft.ai/docs/api-reference/getting-started)
  - [recraft-ai/mcp-recraft-server](https://github.com/recraft-ai/mcp-recraft-server)
  - [Official source 1](https://www.recraft.ai/api)
  - [Official source 3](https://www.recraft.ai/docs/api-reference/endpoints)
  - [Official source 4](https://www.recraft.ai/docs/mcp-reference/getting-started)

Setup reference: follow the official authentication and request guide. This is a documentation URL, not an executed API example.
```text
https://www.recraft.ai/docs/api-reference/getting-started
```

### 6. ComfyUI

- **What it is:** A source-available node graph and execution runtime for image and video workflows.
- **Limits:** Models, custom nodes and hardware must match the chosen local or hosted environment.
- **Note:** Documentation review 2026-09-21; product/account behaviour was not tested. ComfyUI has both local and hosted routes. Downloadable software does not make GPU use, hosted services or every model licence free.
- **Links:**
  - [Homepage](https://www.comfy.org)
  - [Docs](https://docs.comfy.org)
  - [Comfy-Org/ComfyUI](https://github.com/Comfy-Org/ComfyUI)
  - [Official source 2](https://github.com/Comfy-Org/docs/blob/main/openapi-v2.yaml)

Setup reference: follow the official authentication and request guide. This is a documentation URL, not an executed API example.
```text
https://docs.comfy.org
```

## Decision this list supports

Split a Krea replacement into interactive exploration, repeatable production and output format. A tool that makes an attractive image may still lack the workflow or vector deliverable you need.

## Scope and evidence

Documentation reviewed on 2026-09-21. This is a Wireflow-maintained resource dataset. Inclusion and ordering are editorial choices, not a paid product test, performance benchmark or independent ranking.

The capability score counts positively documented checks. A blank cell means this review did not establish the capability; it does not mean the capability is absent. Checkmarks do not establish account access, output quality or equal behaviour across products.

The weekly repository job refreshes GitHub metadata. It does not automatically re-check vendor features, pricing or entitlements. Follow the official links for current terms.

## Selection notes

Evaluate hosted canvases for shared processes, Recraft when vector output is required, and ComfyUI when local control or custom nodes drive the decision. Keep Krea in the trial as the baseline.

## Acceptance recipe

- Use one brief, one reference image and one agreed output size across candidates.
- Save an initial result before making a local edit or style change.
- Repeat the accepted process with a second product or subject.
- Check whether another teammate can find inputs and rerun the process.
- For vector work, inspect the actual exported format and editability.
- Compare accepted files and manual correction time, not gallery examples.

## Evaluation record

Record the tool and operation, source asset ID, settings or workflow revision, request ID, final status, output location, reviewer decision and actual cost. Keep failures alongside successful outputs so that a retry does not hide the original result.

## How this list is maintained

- [`data/tools.json`](data/tools.json) is the source of truth. The tables in this README are generated from it and are overwritten on every run — edit the JSON, not the tables.
- [`scripts/update.js`](scripts/update.js) fetches star counts and latest release tags from the GitHub API for the tools that publish an official repo, stamps the check date, and regenerates the tables. `--offline` regenerates without the network; `--check` exits non-zero if the README has drifted from the data.
- [`.github/workflows/refresh.yml`](.github/workflows/refresh.yml) runs it weekly and on manual dispatch, and commits only when the data actually changed.
- Prices are deliberately not stored as numbers. A stale price in a comparison table is worse than no price, so the table links to each vendor's own pricing page.

## Contributing

Corrections and additions are welcome, including corrections to the entry for the tool that maintains this list. Open an issue with the tool name, a working link, one line on what it does that the tools already listed do not, and one line on where it stops. Entries are judged on whether they are usable today, not on popularity. Full rules in [CONTRIBUTING.md](CONTRIBUTING.md).

## License

[CC0 1.0 Universal](LICENSE) — public domain. Take the data, fork the list, no attribution required.

---

Maintained by [a1adams](https://github.com/a1adams).
