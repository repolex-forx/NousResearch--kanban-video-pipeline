# Repolex Knowledge Graph of NousResearch/kanban-video-pipeline

RDF knowledge graph data for [NousResearch/kanban-video-pipeline](https://github.com/NousResearch/kanban-video-pipeline), parsed by [repolex](https://repolex.ai).

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
rlex download NousResearch/kanban-video-pipeline
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── a464bdda58d9d7784225d972668129323de519a3
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── a464bdda58d9d7784225d972668129323de519a3.nq.gz
│   └── repolex
│       └── a464bdda58d9d7784225d972668129323de519a3
│           └── chunk-001.nq.gz
├── blob
│   ├── 20b87f0d7e6311f5073968f185069d53e3a5a670.nq.gz
│   ├── 28e39343149461294597001d5230edba5f191e27.nq.gz
│   ├── 3393ccf0b6fcbae67fa2e6aac91d5637f3b56a40.nq.gz
│   ├── 4cdc7f99b1a944d052d188a7158f98aa502f7d2c.nq.gz
│   ├── 7302ed7a3ec5045bdb9e0dda7583ee1a970ca957.nq.gz
│   ├── 76ee2f79900d39505accaa0eb7942c9ba56f6405.nq.gz
│   ├── 7ee5903dc1f4ef84c9fc07241a0b53523282f40a.nq.gz
│   ├── 9ff4996819a6f5afbfe29ce1e810b4e739bd6a60.nq.gz
│   ├── abccddfc588f619eec4c53388a4e5e98eca9e127.nq.gz
│   ├── b42b49b1c1313696229dc8407e04b2e56f2a91bc.nq.gz
│   ├── c386a7f6ed6bbee9303625afc8ebdc019ec8e8b5.nq.gz
│   ├── d1e576968c3aa716a90e7280e69cf540fe07c700.nq.gz
│   ├── e1780a532938be9e7eb511a94a19ab037e905635.nq.gz
│   ├── ea98a0372adad4d497c0865c6127e1ad0eeff36a.nq.gz
│   ├── eb0b5a3038230f0953df0eeeb44b5a25cdd07ed6.nq.gz
│   ├── ed1f6fe374ed56439b6896ccba1e49c66a0474dd.nq.gz
│   └── f2addaad949bf3805b393976229804bc1a700f98.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── a464bdda58d9d7784225d972668129323de519a3.nq.gz
├── filetree
│   └── a464bdda58d9d7784225d972668129323de519a3.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

14 directories, 26 files
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

[NousResearch/kanban-video-pipeline](https://github.com/NousResearch/kanban-video-pipeline)

---
*Parsed on 2026-10-02 by [repolex](https://repolex.ai)*
