# Repolex Knowledge Graph of zopefoundation/zope.ptresource

RDF knowledge graph data for [zopefoundation/zope.ptresource](https://github.com/zopefoundation/zope.ptresource), parsed by [repolex](https://repolex.ai).

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
rlex download zopefoundation/zope.ptresource
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 1ca955c954279d4e6863ad0098ba2048c2c81938
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 1ca955c954279d4e6863ad0098ba2048c2c81938
│           └── chunk-001.nq.gz
├── blob
│   ├── 015389853bbf316c3a8e2847d4168c0362f0b84b.nq.gz
│   ├── 064a6fe195889fa90a73621206818352aaa69608.nq.gz
│   ├── 085520c0c4af563701b828cefe5a8f7ed798f34e.nq.gz
│   ├── 0ab12fe1e0c8eb6cb0d68fce1b14a2209cdb0def.nq.gz
│   ├── 12edc3e20c8bcec708ecbd279b0107cb4ef1ee3f.nq.gz
│   ├── 1f321f52abb7db6f79c285bab56e2852dc575699.nq.gz
│   ├── 3f9a228ac81bfc11cfef773b56451335cdb618fd.nq.gz
│   ├── 79859e06010bf4967c5b4b044afea6ef39742938.nq.gz
│   ├── 84f380081c7317b29e5ce125064d5a04998f33e7.nq.gz
│   ├── 90f82b07f129220d66d2737a7a9d006a412dc469.nq.gz
│   ├── a26875774f4a7d88efa3587300ad79423260f896.nq.gz
│   ├── add2483b340ce80c1d58ff2abf840658cd79c478.nq.gz
│   ├── b828f41877e58b12d9f21109fa7506dd32bdb387.nq.gz
│   ├── c5508b9f083362a81185d598327e7801d837cb18.nq.gz
│   ├── ccdedc28073a0ba8303c52c91284a4e7e70bb471.nq.gz
│   ├── cfec5c9ab5c4943cd501ee55b132f62dbb3ee428.nq.gz
│   ├── e1f9ad7b3b48377bfbfaa1b380c384ddea24060f.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── e7b4fd9feb91e261c85b5a1a9db2dcdc482096c2.nq.gz
│   ├── e999faee760ab19141cb907b98f0b377beda79ed.nq.gz
│   └── ff77ae62e5f620bc7cd67b23c157a050bd380320.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 1ca955c954279d4e6863ad0098ba2048c2c81938.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 29 files
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

[zopefoundation/zope.ptresource](https://github.com/zopefoundation/zope.ptresource)

---
*Parsed on 2026-11-06 by [repolex](https://repolex.ai)*
