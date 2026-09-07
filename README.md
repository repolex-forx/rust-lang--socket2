# Repolex Knowledge Graph of rust-lang/socket2

RDF knowledge graph data for [rust-lang/socket2](https://github.com/rust-lang/socket2), parsed by [repolex](https://repolex.ai).

> **Note**: This data is experimental and subject to change without notice.

## How to use this data

The easiest way to get started is to install the [lexq](https://github.com/repolex-ai/lexq) query tool using [uv](https://docs.astral.sh/uv/getting-started/installation/).

If you have uv installed, just copy/paste this into your terminal:

```bash
uv tool install git+https://github.com/repolex-ai/lexq
```

This installs lexq onto your system, in your user context. Verify the install:

```bash
lexq --help
```

**lexq is designed to be used primarily by LLMs in a terminal.** Start up your favorite LLM and ask it to use the lexq tool. It's that easy!

To load this repo's data:

```bash
lexq download rust-lang/socket2
```

This will automatically download essential data files from the last parsed commit. Consult `lexq --moreinfo` for other options, including downloading multiple commits, blobs, etc.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 239dd83a4ced08e514d2c38942aab99791119f0d
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── 239dd83a4ced08e514d2c38942aab99791119f0d.nq.gz
│   └── repolex
│       └── 239dd83a4ced08e514d2c38942aab99791119f0d
│           └── chunk-001.nq.gz
├── blob
│   ├── 120a5466492567859c103b2260916222bb8a85d0.nq.gz
│   ├── 16fe87b06e802f094b3fbb0894b137bca2b16ef1.nq.gz
│   ├── 2970f22f78170282d764014f07713c1921b7efa5.nq.gz
│   ├── 30eedd62751981e4d3cadb69b9f65379e2639495.nq.gz
│   ├── 39e0ed6602151f235148e6c08413aa7eda5b9038.nq.gz
│   ├── 5ad4ea927e5b9f295d685ea741d46eadc7d76152.nq.gz
│   ├── 67de36707444efb840f9cd0052cdfac06fbcb4bb.nq.gz
│   ├── 6b7a1c815b22067d35c1839eaf9970daec1690c2.nq.gz
│   ├── 75c73087c0f125c9304a116c11708bb05a920b03.nq.gz
│   ├── 7d8e949a49787fb747be2491acce5f48e5132b20.nq.gz
│   ├── 8475c67de7929e40a4ee999c69030f900fe4b504.nq.gz
│   ├── 886a8eab813788cdf4e5bdf2135a01effcb79689.nq.gz
│   ├── 97c87acc4670bd801603dfb41fa2b61fe200c8a4.nq.gz
│   ├── a226fe13ac981720016b0174d4cc08c363f95127.nq.gz
│   ├── b07a031f702ff3df39f701d40061173f711718e5.nq.gz
│   ├── cd0875583aabe89ee197ea133980a9085d08e497.nq.gz
│   ├── da01a77a2fc7412cc96d599c6d5d5f1bb1a29f7b.nq.gz
│   └── e41a22bba8d7e352a1814d74b5a6eaa7e4b36820.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── 239dd83a4ced08e514d2c38942aab99791119f0d.nq.gz
├── filetree
│   └── 239dd83a4ced08e514d2c38942aab99791119f0d.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

15 directories, 28 files
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

## Source repository

[rust-lang/socket2](https://github.com/rust-lang/socket2)

---
*Parsed on 2026-09-07 by [repolex](https://repolex.ai)*
