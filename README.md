# Repolex Knowledge Graph of jupyterhub/firstuseauthenticator

RDF knowledge graph data for [jupyterhub/firstuseauthenticator](https://github.com/jupyterhub/firstuseauthenticator), parsed by [repolex](https://repolex.ai).

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
rlex download jupyterhub/firstuseauthenticator
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 7216c7415a3e6d088750aa05538466841fb61f1d
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 7216c7415a3e6d088750aa05538466841fb61f1d
│           └── chunk-001.nq.gz
├── blob
│   ├── 0c130aef34b610a37f17ddf08aec6ff2744e4e28.nq.gz
│   ├── 19f878e17aef414a52b4abe82d7bf5f3a32a1e16.nq.gz
│   ├── 2e68da7a4692e167550fef2b92b61eede12f016e.nq.gz
│   ├── 32d3342ea10578df5eb697e7f8860316c1bf403f.nq.gz
│   ├── 4152359d87340e44829fb5bf0e61bac41fb0868b.nq.gz
│   ├── 4378b33295acb74e19e3ff21d01138c2a156ff40.nq.gz
│   ├── 4d76e0c35dedcf620b7642517673f8f1c7cc241c.nq.gz
│   ├── 59eab2c4bec88dae37317bf959d394e1a043d8e0.nq.gz
│   ├── 5c5f7432e797b710b89c20508f7ee9da9d6ee8e2.nq.gz
│   ├── 855241d3241c36808cf35a96d1c062ba6cad8a8b.nq.gz
│   ├── 88fc039f0dccbac8678fcdcd53c3af9397d86461.nq.gz
│   ├── 9323eaf5bf049659deadb62fc6fb1dee18126120.nq.gz
│   ├── a30716606759a0bc80a82dccc67369fe781db9e0.nq.gz
│   ├── caa7fafbb735bedfb1a6fd8f2196f431358b6ff3.nq.gz
│   ├── ccdf29b948bc9c6945ce3f975a2fe61a6c9a239e.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   └── fa4ab0d7f48c50c6b150a1ca7f88f9546154f03f.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 7216c7415a3e6d088750aa05538466841fb61f1d.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 25 files
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

[jupyterhub/firstuseauthenticator](https://github.com/jupyterhub/firstuseauthenticator)

---
*Parsed on 2026-10-15 by [repolex](https://repolex.ai)*
