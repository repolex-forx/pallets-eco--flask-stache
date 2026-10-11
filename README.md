# Repolex Knowledge Graph of pallets-eco/flask-stache

RDF knowledge graph data for [pallets-eco/flask-stache](https://github.com/pallets-eco/flask-stache), parsed by [repolex](https://repolex.ai).

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
rlex download pallets-eco/flask-stache
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── b3bbd326bdbcab04f7eec04dae20e74c1713942b
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── b3bbd326bdbcab04f7eec04dae20e74c1713942b
│           └── chunk-001.nq.gz
├── blob
│   ├── 01c8e73ae975008155236b4ca113ee248f764efa.nq.gz
│   ├── 036f0b6d792794d14f42e3035baf619d32f201d3.nq.gz
│   ├── 142ff3aac8d99ed89e341386ec7daaef82308fec.nq.gz
│   ├── 161634d64d4d9ec8f716593283a7357f6060d1f3.nq.gz
│   ├── 265c0036ed751e669a9519e181274b2d78e6b2ab.nq.gz
│   ├── 2b1a4f0b9c203602ddb36d0d6ba3939d49e86e11.nq.gz
│   ├── 32c79a603ea21eb140777d4fba3165fb036a72a5.nq.gz
│   ├── 3440e34ff8e17e5c7780849509cddb75d958d2fb.nq.gz
│   ├── 38447485cdcdd83285d63061ffdc40954808fefd.nq.gz
│   ├── 6740d247b30fbd8fd7b6bee0ea13cc967cc3d7ea.nq.gz
│   ├── 6d3308a8975552de7f821f56dd45b3285e6b50b7.nq.gz
│   ├── 7b4e800d9406a8a2e09f331f6c76ae22db84a953.nq.gz
│   ├── 8a05a51e8698babbed33230457f17c9073042d81.nq.gz
│   ├── 988e3b1a7b826604cb9f436c6adf41fd20c34038.nq.gz
│   ├── 9f7e3a2cd332888dfbdf792d406d67dcad507e36.nq.gz
│   ├── b488a9b20bdc3119d9f4467209df1880085c8bfb.nq.gz
│   ├── bf7b494fc7044e1395c1c821f2babc309277bf78.nq.gz
│   ├── c5f458c8dc4ddbcb42459c4cfe2634dea3ef065c.nq.gz
│   ├── daf25454e6eea7a7dd0df0cce8299b0e66133dbd.nq.gz
│   ├── e35d8850c9688b1ce82711694692cc574a799396.nq.gz
│   ├── e7858462787427846f90bbe8c372355c324fa82a.nq.gz
│   └── f5c6f5921d26a7837d0e5a743cf08052c6330a64.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── b3bbd326bdbcab04f7eec04dae20e74c1713942b.nq.gz
├── issue
│   └── issue.nq.gz
└── tag
    └── tag.nq.gz

12 directories, 29 files
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

[pallets-eco/flask-stache](https://github.com/pallets-eco/flask-stache)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
