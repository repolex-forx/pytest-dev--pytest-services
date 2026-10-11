# Repolex Knowledge Graph of pytest-dev/pytest-services

RDF knowledge graph data for [pytest-dev/pytest-services](https://github.com/pytest-dev/pytest-services), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [rlex](https://github.com/repolex-ai/rlex) query tool:

```bash
cargo install --git https://github.com/repolex-ai/rlex
```

Verify the install:

```bash
rlex --help
```

**rlex is designed to be used primarily by LLMs in a terminal.** Start up your favorite AI assistant and ask it to use rlex. It handles the SPARQL — you just ask questions in plain English.

To load this repo's data:

```bash
rlex download pytest-dev/pytest-services
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── bf6132c8589a9884c3dc5ab18634002acd3ce498
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── bf6132c8589a9884c3dc5ab18634002acd3ce498
│           └── chunk-001.nq.gz
├── blob
│   ├── 04c7afe99f086f2267d95b04eda9fe84efc18863.nq.gz
│   ├── 0e9573692d01dc70e352cdd905be1ca06cc079a7.nq.gz
│   ├── 1002103858b8e11f9ae63f2d49710dbde5c034b0.nq.gz
│   ├── 181e34b5dfe8b10dab3f97e97a37df38b7ad99ca.nq.gz
│   ├── 1c9407ee93b824b0fbfe96d636a47994a58eadbd.nq.gz
│   ├── 201a90c08dd5433fd28e124b5d229428f911957f.nq.gz
│   ├── 27e1cf4d516314c9d6c153227a08d66177fb332b.nq.gz
│   ├── 2b72f3c75f4e8b2f4c413691d4b3dcdb9ccfa7e6.nq.gz
│   ├── 3959abd1bc34feede1f8f6e1d7abfdd4bf94c7d3.nq.gz
│   ├── 404289a3cf24000c3a3da2d17c4e51f203e5cbb3.nq.gz
│   ├── 4436a4c902501294db4612f27f012cf4d1fa0cc4.nq.gz
│   ├── 499d753ba272be1807ab785a60c3b2c9686b6109.nq.gz
│   ├── 4f278fdeb10dfd0ca987b2b664ee66c4dc700369.nq.gz
│   ├── 4f6ec52fd9fb70688f79566849229fc99c7cc891.nq.gz
│   ├── 50277c70a08d8a843203bcb716a5bec99cd1b41c.nq.gz
│   ├── 659f8be0f588b1914b72513a48d8ebef30b92968.nq.gz
│   ├── 684788eacc1859addcf0fd965c703458a17158d0.nq.gz
│   ├── 784fb01edd5129483942e28645afa38538af6a12.nq.gz
│   ├── 878349a8ff6889c87afc8aaf62fba9f5ed81a160.nq.gz
│   ├── 8873608ed2562d17417e05df5da5ce413312e445.nq.gz
│   ├── 8a3553aa6bd744218c96e55e43cbe040fd25be5d.nq.gz
│   ├── 911b442ae9e91eedc0eda3c3de45f56af859a838.nq.gz
│   ├── 97ae4fd8fb6a75216fcfdbe4a2c36a1ab7898b63.nq.gz
│   ├── 9e2dacadf1133357ce97bdc062971ac4704cebd6.nq.gz
│   ├── a54fc55a94ba88c5f6884b0677dcbeb1ebadb552.nq.gz
│   ├── a6498f8a81782503c0c101be7b865acda1d9da55.nq.gz
│   ├── ac09ac3972265baea84e8b05f5ed06d660f0cd71.nq.gz
│   ├── b9f896837cd797f11fcca4a49301f2d446f71001.nq.gz
│   ├── c3f263973181e259a9ad8b19acea81f868b55d6a.nq.gz
│   ├── c712d2595247bf32129c8609dcf822e238412a20.nq.gz
│   ├── d18a64b613456f277b0b75d7ec26db6f385e9382.nq.gz
│   ├── decbb5f16667139e48b00ed0b32c3b2f025d7418.nq.gz
│   └── f2e2d9c5bb486eae97f7a57eb7139dcaab5b057e.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── bf6132c8589a9884c3dc5ab18634002acd3ce498.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 41 files
```

| Directory | What it contains |
|-----------|-----------------|
| `blob/` | Per-file AST graphs, content-addressed by git blob SHA. Each file in the source repo gets its own graph. |
| `aggregate/ast/` | Combined AST graph per parsed commit. Merges all blob graphs for a snapshot of the entire codebase at that point. |
| `aggregate/lsp/` | Language Server Protocol enrichment: resolved symbols, definitions, references, and type information. |
| `aggregate/dataflow/` | Interprocedural data flow edges between functions and modules. |
| `aggregate/repolex/` | Combined graph (AST + LSP + dataflow) per commit. |
| `commit/` | Git commit metadata (author, date, message, parent links). |
| `branch/` | Branch metadata. |
| `tag/` | Tag metadata. |
| `filetree/` | File tree snapshots per commit (which files existed and their blob SHAs). |
| `audit/` | Code architecture and graph audit reports per commit. |

## Source repository

[pytest-dev/pytest-services](https://github.com/pytest-dev/pytest-services)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
