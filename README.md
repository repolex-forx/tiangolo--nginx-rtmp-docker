# Repolex Knowledge Graph of tiangolo/nginx-rtmp-docker

RDF knowledge graph data for [tiangolo/nginx-rtmp-docker](https://github.com/tiangolo/nginx-rtmp-docker), parsed by [repolex](https://repolex.ai).

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
rlex download tiangolo/nginx-rtmp-docker
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── ff589ceb6234ddd4976e488cd9ac08a06ac9fb16
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── ff589ceb6234ddd4976e488cd9ac08a06ac9fb16
│           └── chunk-001.nq.gz
├── blob
│   ├── 1ab6a93ad5001f074bfe7866335e7c4c35365bca.nq.gz
│   ├── 1b2851346eb59a250fe5f88874266f28acadcc24.nq.gz
│   ├── 5422101c72c9367b86e88c93f429d74f4448520d.nq.gz
│   ├── 6c628b80228fb629d44ce73d34021ae9d46ef05b.nq.gz
│   ├── 723e721673ec99598c7a299159bb74896ca5fb2e.nq.gz
│   ├── 797ef0bcef05ed72b71a2e7291c6d469d1106f2b.nq.gz
│   ├── 841ac4900b75dc2f971db7c3acfccb03c0c6a205.nq.gz
│   ├── 93a8da2063766c1e97e2ef15caab90ceeff6b46a.nq.gz
│   ├── a09ee31711a17dd2fc97f33ca4b9f4246496a093.nq.gz
│   ├── a2a59ce0ac1a5f26072ffa927c5242d50e73be87.nq.gz
│   ├── a7f12511f60ac7e3c1b2828a4370d128fbe79c08.nq.gz
│   └── b1f6ed41fb95b2e566ba206fee9f22347803812d.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── ff589ceb6234ddd4976e488cd9ac08a06ac9fb16.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 20 files
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

[tiangolo/nginx-rtmp-docker](https://github.com/tiangolo/nginx-rtmp-docker)

---
*Parsed on 2026-10-10 by [repolex](https://repolex.ai)*
