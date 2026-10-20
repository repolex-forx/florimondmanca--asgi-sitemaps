# Repolex Knowledge Graph of florimondmanca/asgi-sitemaps

RDF knowledge graph data for [florimondmanca/asgi-sitemaps](https://github.com/florimondmanca/asgi-sitemaps), parsed by [repolex](https://repolex.ai).

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
rlex download florimondmanca/asgi-sitemaps
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 009b0f04ef4bca29bcfb8304411b27b9b2bda64e
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 009b0f04ef4bca29bcfb8304411b27b9b2bda64e
│           └── chunk-001.nq.gz
├── blob
│   ├── 01f0fb0a242092bb0018135313051636a5a19933.nq.gz
│   ├── 0b9bdad13f7f1cb621ef2f450255e9aba348ac2e.nq.gz
│   ├── 153e1e4b77841a5c73cc87887db3e8d16c5fd357.nq.gz
│   ├── 15608b6742ca4cbc1eb9ada0b24d2d16d865bfdf.nq.gz
│   ├── 1e9b6570cf899d58cb22c88da36cef9150d75d88.nq.gz
│   ├── 405f33e98e0e5cfd13d7acd8a88dd467687779a5.nq.gz
│   ├── 48eb80155f58e4181748cdf47aa352c0af06b2ee.nq.gz
│   ├── 49139e012b8905b8b421e488415d4e509f1838bc.nq.gz
│   ├── 5820dc66701a66bd610c73adf1880207455d053f.nq.gz
│   ├── 5becc17c04a9e3ad1c2a15f53252b7bb5a7517e7.nq.gz
│   ├── 66ef445412b3b89ffe6f4c7684ad1919b78b25de.nq.gz
│   ├── 802d1da3247e03ed7b42db0a0beb7f0535ec5c55.nq.gz
│   ├── 961b0e94d15958e5754a32cff86e219d40ea1ab6.nq.gz
│   ├── 9921cd9ba51b8c298ada611b008f99f36357c92e.nq.gz
│   ├── c39bdf1d7b687c6ff9228653056f5c8ef0d96394.nq.gz
│   ├── c943a3d7e4838b79a3510bf8f439345a2e1ca019.nq.gz
│   ├── d5a91f86c28e62c6aa25f5d136ecfbadd18a3917.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   └── fd0987826e084ce32c6a8b1f496aca70e5e4d86d.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 009b0f04ef4bca29bcfb8304411b27b9b2bda64e.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 27 files
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

[florimondmanca/asgi-sitemaps](https://github.com/florimondmanca/asgi-sitemaps)

---
*Parsed on 2026-10-20 by [repolex](https://repolex.ai)*
