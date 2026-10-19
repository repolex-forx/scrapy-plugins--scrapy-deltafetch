# Repolex Knowledge Graph of scrapy-plugins/scrapy-deltafetch

RDF knowledge graph data for [scrapy-plugins/scrapy-deltafetch](https://github.com/scrapy-plugins/scrapy-deltafetch), parsed by [repolex](https://repolex.ai).

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
rlex download scrapy-plugins/scrapy-deltafetch
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── a8caf39de50ce44abe1950e6d3f3f94a56df393f
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── a8caf39de50ce44abe1950e6d3f3f94a56df393f
│           └── chunk-001.nq.gz
├── blob
│   ├── 07880e1c3628142ed07e4c776206692e9ca73481.nq.gz
│   ├── 4f6813f976c21daac9e4d66020e4cf999f944c44.nq.gz
│   ├── 545885b4dfb7a78bcbf7df42dd6ca00becb71e7c.nq.gz
│   ├── 555500bc9d0375d9b393e38f9c94a6b1292defdb.nq.gz
│   ├── 6c4228c411ef1f829c32e28fa3fd9e371f812d4c.nq.gz
│   ├── 6e42d58d9d653cef3e0872fc2c01e64d1f075814.nq.gz
│   ├── 98f6514f36ae99e279beac2fe550406851bc0857.nq.gz
│   ├── 9d0e3fc66ce8b0cbf583504d8c74e67e9a297c6d.nq.gz
│   ├── b9b574ed934ceeabfc864f3ba0e77aed539ae346.nq.gz
│   ├── bd686f7436b4b11f6dd1a51dcb4110be746f5de5.nq.gz
│   ├── d3e17bed373109c1829a89820c1018dbd5df31e6.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   └── fd707ad173186ace01c470aa27522c31fbdb725e.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── a8caf39de50ce44abe1950e6d3f3f94a56df393f.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 21 files
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

[scrapy-plugins/scrapy-deltafetch](https://github.com/scrapy-plugins/scrapy-deltafetch)

---
*Parsed on 2026-10-19 by [repolex](https://repolex.ai)*
