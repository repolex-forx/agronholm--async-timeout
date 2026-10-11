# Repolex Knowledge Graph of agronholm/async-timeout

RDF knowledge graph data for [agronholm/async-timeout](https://github.com/agronholm/async-timeout), parsed by [repolex](https://repolex.ai).

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
rlex download agronholm/async-timeout
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── c7d61a81901dc90f8e32e4b79e81429e10a4a7df
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── c7d61a81901dc90f8e32e4b79e81429e10a4a7df
│           └── chunk-001.nq.gz
├── blob
│   ├── 04e86f0c4fdb6d021d9f2a4434c16ac709d52ca7.nq.gz
│   ├── 0ec19b38e912a6bf0477c0ed5a8505b668bd891e.nq.gz
│   ├── 3c5534834f7b2f157c5a45b710e578055a26267e.nq.gz
│   ├── 5a560f806c7172fead2635c2c1c4202f3fdc2f13.nq.gz
│   ├── 6ea20650afd318e6f414b05025314b348b228afc.nq.gz
│   ├── 72364f99fe4bf8d5262df3b19b33102aeaa791e5.nq.gz
│   ├── 7e20b69e106d05589e28529a0e1f98f96e9d100e.nq.gz
│   ├── 85b4b522a47b7d8328c37c895ae9098af7b452ac.nq.gz
│   ├── 8dada3edaf50dbc082c9a125058f25def75e625a.nq.gz
│   ├── 9740a44eebd664448713632b2791b0c4ceeaddc0.nq.gz
│   ├── a57c7aeb18f7d17473164f58945f259a07c421fe.nq.gz
│   ├── b51e2b8fa4cb539283d9fbf848671f31085fcb84.nq.gz
│   ├── be6a243ade7b3c8007c66362c37aba6ef4d9dab7.nq.gz
│   └── d3410db02454dc737197469bfd1cff9191b051df.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── c7d61a81901dc90f8e32e4b79e81429e10a4a7df.nq.gz
└── tag
    └── tag.nq.gz

11 directories, 20 files
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

[agronholm/async-timeout](https://github.com/agronholm/async-timeout)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
