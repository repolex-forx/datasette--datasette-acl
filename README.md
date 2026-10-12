# Repolex Knowledge Graph of datasette/datasette-acl

RDF knowledge graph data for [datasette/datasette-acl](https://github.com/datasette/datasette-acl), parsed by [repolex](https://repolex.ai).

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
rlex download datasette/datasette-acl
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── b586db5bef9fa18efebd47bfc13a90980dd2f395
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── b586db5bef9fa18efebd47bfc13a90980dd2f395
│           └── chunk-001.nq.gz
├── blob
│   ├── 02e5e7c5b1e904274b01ba4f5ffefb2251053f5f.nq.gz
│   ├── 04580d39afdd55a469061295b118dcc65dcc8ad4.nq.gz
│   ├── 07d8d2c28853169f316d6ae04cf0c3e60894481f.nq.gz
│   ├── 2519978bf16dfbe7595405876e28698eb6b30b73.nq.gz
│   ├── 261eeb9e9f8b2b4b0d119366dda99c6fd7d35c64.nq.gz
│   ├── 26b96292e9ba81bf8de1269802187a5928ed8659.nq.gz
│   ├── 28b83d7e90c4f8a8655a666282f0fbd091e7667a.nq.gz
│   ├── 29dafe9560c8491b19e61f9b0a1072ff8c7cdb4d.nq.gz
│   ├── 432f18873762b3f277abea8da35cd97982cedc6a.nq.gz
│   ├── 46fc0564fd03a969e8099e2a3b3036d6dc15d40b.nq.gz
│   ├── 578c2d7014cb9b2d0b026db1e7c994e8630f50d8.nq.gz
│   ├── 60b534e93ec368d4f84a1408a7e59db94303f3d5.nq.gz
│   ├── 76f32d45bac7fecb1da6971e481e087cc008f195.nq.gz
│   ├── 801f7b326e4176a12b920099c01383cbe9c67e3b.nq.gz
│   ├── 96c71f76357db0a4584109a8f510171f00c9ddc3.nq.gz
│   ├── a67a9e70559c3a09138a88e046530b76eb4a073b.nq.gz
│   ├── a6c58553e94b502f3589736a1633f8824e8916d9.nq.gz
│   ├── a7fa5b48eb41c268d4ec6a6e9c6ba4bfb86c6032.nq.gz
│   ├── aa3e8242d1564e6e835779481394ad186467835f.nq.gz
│   ├── aafc3bdd3fcc122407626f03628cd9a041c7ba24.nq.gz
│   ├── af0f7fb8c742560f0c7723a6b4bec89b7c7e879f.nq.gz
│   ├── b575c0439da06579e602e98133ef93f582634ca2.nq.gz
│   ├── b5fc977062ad5c13aabdb065f03f691136415f7f.nq.gz
│   ├── bd1ade013ffbbfb6bfe5a554601c72333b03f26a.nq.gz
│   ├── be3e1d8e2a9beb919339ae05f7b39eb513c47baa.nq.gz
│   ├── ce5da26956b7a39164980fdd8abcd146740ce0e8.nq.gz
│   ├── d403499b6d8218301e80433f615d7e6da1a59631.nq.gz
│   ├── d421c89176425dc0745c723e90239f1c5de5514b.nq.gz
│   ├── da4732d7edc87d8dd055ab329c15fa28b745682f.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── eb316ffea59ccd0a7d58689ba0f6f133a6847464.nq.gz
│   └── f500363b864817b3086bd7396ff925b1db39aa8d.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── b586db5bef9fa18efebd47bfc13a90980dd2f395.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 40 files
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

[datasette/datasette-acl](https://github.com/datasette/datasette-acl)

---
*Parsed on 2026-10-12 by [repolex](https://repolex.ai)*
