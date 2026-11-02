# WhoopingLlama

**A human-guided AI research pipeline for evidence curation, classification, provenance preservation, and traceable analysis.**

> [!NOTE]
> **Status: early development.** This repository is currently a public project landing page. Source code, downloadable builds, and installation instructions have not yet been published here. The architecture described below is only an evolving design.

## Overview

**WhoopingLlama** is the codename for a ground-up architectural rethink of **PaxResearchPipeline (PRP)**. The project explores a modular, human-directed environment for turning heterogeneous source material into research outputs whose origins, transformations, and supporting evidence can be inspected.

AI-assisted analysis is part of the design, but it is not intended to replace human judgment. The operator retains responsibility for framing questions, evaluating findings, verifying claims, and approving publication.

## Working architecture

The current concept separates evidence handling and classification, research orchestration, inference, and publication:

```text
Source material
      |
      v
  PaxCorpus ----> PaxClassifier ----> PaxConductor <----> PaxInference
                                           |
                                           v
                                PaxUniversalTranslator
                                           |
                                           v
                                       PaxPublish
```

The proposed components are:

- **PaxCorpus** — evidence ingestion, organization, and preservation of source context and provenance.
- **PaxClassifier** — classification, categorization, and annotation of corpus evidence, with traceable classification decisions.
- **PaxConductor** — a workbench for specifying, running, and inspecting human-directed research workflows.
- **PaxInference** — model execution services, with local inference an important design priority.
- **PaxUniversalTranslator** *(working name)* — adapting research artifacts into forms suited to different audiences and output formats.
- **PaxPublish** — preparation and publication of reviewed research outputs.

These names, boundaries, and relationships remain subject to change as implementation and verification proceed.

## Design priorities

- **Evidence before interpretation:** retain identifiable source material and meaningful provenance, keeping derived classifications distinct from original evidence.
- **Traceable transformations:** connect classifications, annotations, and other derived outputs to the inputs and processes that produced them.
- **Operator control:** make decisions, verification gates, and publication approvals explicit.
- **Modularity:** separate evidence storage, classification, workflow control, model runtimes, and output generation.
- **Local operation:** favor practical local-first workflows without making network services a universal requirement.
- **Verifiable engineering:** distinguish design proposals, experimental builds, tested behavior, and operator-accepted releases.

## Project status

This is an active research and software-engineering effort, **not yet a publicly released application**. There are currently no supported builds, installation procedures, or stability guarantees associated with this repository.

As material becomes ready for publication, this repository can grow to include source code, component specifications, build instructions, test evidence, and release notes. No release schedule is being announced here.

## License

Original material published in this repository is licensed under the **GNU General Public License, version 3 only** (`GPL-3.0-only`). See the full terms in [LICENSE](LICENSE).

Third-party dependencies or assets, if introduced, remain subject to their own applicable license terms. A license file here does not make source code that has not been published available.

## Maintainer

An independent project by [PedanticLlama](https://github.com/PedanticLlama).
