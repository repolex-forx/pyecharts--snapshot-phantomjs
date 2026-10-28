# Repolex Knowledge Graph of pyecharts/snapshot-phantomjs

RDF knowledge graph data for [pyecharts/snapshot-phantomjs](https://github.com/pyecharts/snapshot-phantomjs), parsed by [repolex](https://repolex.ai).

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
rlex download pyecharts/snapshot-phantomjs
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 5fc4d7696923b35cb9f8a62a356e832e1bc171a1
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 5fc4d7696923b35cb9f8a62a356e832e1bc171a1
│           └── chunk-001.nq.gz
├── blob
│   ├── 1cc8e402cef4ecab61aa8353171980a709fd9d58.nq.gz
│   ├── 2a9acf13daa95e85642ea255d3e3bd1ef8252804.nq.gz
│   ├── 334b4ba87e262dd8b5b44f600a20e3284144061f.nq.gz
│   ├── 37e4f24ba0b804bc31236bc896b8bb339c9ef1cd.nq.gz
│   ├── 3e0ee51423673045d76cf8604c03cc0c6432c58a.nq.gz
│   ├── 402e083dce2a4ee8597209cd6e2126cdac730c2f.nq.gz
│   ├── 492784e0d56404eee289bf72e303c98d416427e3.nq.gz
│   ├── 5357dac758dbfbf804cb170616d01a1526e90ea1.nq.gz
│   ├── 71ba03786857fd8df5308402b9f8b1d469f0e8c5.nq.gz
│   ├── 92b6f2ffe27e0cea6c4b849727192484213feff8.nq.gz
│   ├── b70c2782aa78ff135cc4dadbe992727e9a67596b.nq.gz
│   ├── b80ce952fe6ae18bab95ce286316fb9ee5619599.nq.gz
│   ├── b8cdc8a43fd9654086eb52ce8138ada9864ecfbf.nq.gz
│   ├── c0bd2f4a9abd1f9e0e0e436dd76167c08eb64d0e.nq.gz
│   ├── c5652ebf9d5cdcf4c603097cf04daf86e0767a2a.nq.gz
│   ├── c7cb404fafa97b03f5e65ef2e10096b29915451e.nq.gz
│   ├── ccab7bba6238e85917fa7f31488de0c7483402a8.nq.gz
│   ├── d31eeaa644fa18b29af15f226cc02daa5ad59227.nq.gz
│   ├── e2a89138117ddb81932ebb0323df03699cdc2536.nq.gz
│   └── f926159474b3f333d62247066377271f55590fc0.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 5fc4d7696923b35cb9f8a62a356e832e1bc171a1.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 28 files
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

[pyecharts/snapshot-phantomjs](https://github.com/pyecharts/snapshot-phantomjs)

---
*Parsed on 2026-10-28 by [repolex](https://repolex.ai)*
