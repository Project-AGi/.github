# Project AGi

> A modular project for developing AIVA, her capabilities, and the tools used to understand and improve her.

[![Organization](https://img.shields.io/badge/Organization-Project--AGi-967BB6?logo=github&logoColor=white)](https://github.com/Project-AGi)
[![Status](https://img.shields.io/badge/Status-experimental-orange.svg)](https://github.com/Project-AGi)
[![Development workspace](https://img.shields.io/badge/Workspace-OppaAI%2FAGi-76B900?logo=github&logoColor=white)](https://github.com/OppaAI/AGi)

---

## Repository map

Repositories are grouped by their role in AIVA’s architecture. The groups describe responsibility, not dependency or maturity.

### Entity · `#entity`

AIVA’s runtime and internal systems: identity, orchestration, memory, sensory input, and system integration.

| Repository | Role |
|---|---|
| [Shell](https://github.com/Project-AGi/shell) | Runtime workspace, component wiring and configuration support. |
| [Telepathy](https://github.com/Project-AGi/telepathy) | AIVA’s receptor and conversation adapter, following the Console/Receptor migration. |

### Capabilities · `#capability`

Tools AIVA can use to create, perceive, or act.

| Repository | Role |
|---|---|
| [Canvas](https://github.com/Project-AGi/canvas) | Vector drawing actions, validation, and SVG rendering. |
| [Imaging](https://github.com/Project-AGi/imaging) | Image-related capabilities used by AIVA. |

### Shared components

| Repository | Role |
|---|---|
| [Memory](https://github.com/Project-AGi/memory) | Shared memory interface and storage backends. |
| [Cypher](https://github.com/Project-AGi/cypher) | Shared ROS 2 messages and signal encoding. |
| [Interactive](https://github.com/Project-AGi/interactive) | Reusable conversation engine. |
| [Health](https://github.com/Project-AGi/health) | Logging and system health reporting. |

### Interfaces

| Repository | Role |
|---|---|
| [Console](https://github.com/Project-AGi/console) | External interfaces, including Telepathy Console and Canvas Studio. |
| [Augmented Reality](https://github.com/Project-AGi/augmented-reality) | Android Unity app that places AIVA in the room using ARCore. |

### Diagnostics · `#diagnostic`

Benchmarks and checks used to inspect behavior, compare models, and validate components.

| Repository | Role |
|---|---|
| [Scorecard](https://github.com/Project-AGi/scorecard) | Benchmark protocols, evaluation results, and model comparisons. |

Unit-test repositories and test suites belong in this group when they are maintained separately from the component they test. Tests stored inside Shell, Canvas, or Imaging stay with their component.

## How the groups fit together

```text
AIVA
├── Entity       Shell, Telepathy receptor, AIVA policies
├── Capabilities Canvas and Imaging
├── Shared       Memory and Cypher
├── Interfaces   Console and Augmented Reality
└── Diagnostics  Scorecard and cross-component evaluation
```

The entity hosts and coordinates AIVA’s behavior. Capabilities provide functions she can call. Diagnostics help evaluate her behavior and the models and components she uses.

### Project status
AGi is under active development. Repository descriptions and benchmark results document what has been implemented; planned model configurations and future capabilities should be treated as plans until they are integrated and evaluated.

Built in beautiful British Columbia, Canada.
