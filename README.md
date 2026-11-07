# Repolex Knowledge Graph of allenai/nora_lib

RDF knowledge graph data for [allenai/nora_lib](https://github.com/allenai/nora_lib), parsed by [repolex](https://repolex.ai).

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
rlex download allenai/nora_lib
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 45b630a1caba54d4f87e8fde82a4022c96034524
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 45b630a1caba54d4f87e8fde82a4022c96034524
│           └── chunk-001.nq.gz
├── blob
│   ├── 00b7b368d52e213f26bc7de76a431b79d163e207.nq.gz
│   ├── 15a93a00e3fdcd08725a6167dd86bafe457636b0.nq.gz
│   ├── 1996f243c704f1f0880320420a568988b6114b92.nq.gz
│   ├── 1c6a14d6f496f98623eba7f2b7ab3e3cfe4ab451.nq.gz
│   ├── 20a6f2e0f7033aabac2148f802a3e44a9b34c393.nq.gz
│   ├── 261eeb9e9f8b2b4b0d119366dda99c6fd7d35c64.nq.gz
│   ├── 2afbb2cc0fbac1dc33f44131ec36fb3aeec4850b.nq.gz
│   ├── 3ebbf99161e78c4a180686db165440746c20dbaf.nq.gz
│   ├── 40cd2cb75afd6a262dba23064e25899d049fcca3.nq.gz
│   ├── 4811fbb896ce41b9a0a2612896dd93a772eaba1b.nq.gz
│   ├── 4b0075311e1d1c1ca67aeb03019bec947596b216.nq.gz
│   ├── 54b1906aa6aebcb12bd3a9e732529bc60208c917.nq.gz
│   ├── 56109b76354c425b15fe43ada57177317e9a9454.nq.gz
│   ├── 5b296aa17e920112c1711ddb9a7b87a5108dab56.nq.gz
│   ├── 631f47997f183122cc7a0d08d0290b0d03cb17b9.nq.gz
│   ├── 7474d9f9b4d20979d703936b87e6c7d3f7af6da4.nq.gz
│   ├── 7b3f171ead827ec76c60a7e617acc1e71d43e6ee.nq.gz
│   ├── 7d174f6048ee7fc3e0285ea9e930a391ed7beff1.nq.gz
│   ├── 7edde81350024d36279de69ec696d25d7c168473.nq.gz
│   ├── 80e88a097ebf792dff27cfbe8ebe82150e6e9dfd.nq.gz
│   ├── 877327e8a4f108a4be7075023992a9e326240bcb.nq.gz
│   ├── 8a8c39a821c86fd0458b186ac44331527b7c9b07.nq.gz
│   ├── 931d93c3a4efdccd2f3b0f1303239e2fdbe88627.nq.gz
│   ├── 9787c3bdf008a57ae3cb2e27a8261eb3f134ff73.nq.gz
│   ├── 9d8f506c03cc273b796741e4472311563af5bd7b.nq.gz
│   ├── 9fc2d0a2faf3ec06d01bf7c287df236b7891a0d9.nq.gz
│   ├── a039b74f04a9db191827da92ec3943e68f73e7fc.nq.gz
│   ├── b6ae9e80b86ff359319c03239d24b4f0207fa282.nq.gz
│   ├── b92365c27764f9c49cf3a6a053080490d6febfba.nq.gz
│   ├── c8a562e2621550b474f7f7b70e6fcfec77b6578d.nq.gz
│   ├── da1868d65e1aa7c5541fad5253e663b0e056e8ef.nq.gz
│   ├── debf962e70e7ea6f865deba7c9cfd71c1b2f79b6.nq.gz
│   ├── e606aafc3436208f0fb91f12514064c5fb086279.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── ec8b694d4567aa30b45800b132659dcb811c08c3.nq.gz
│   ├── f235637a70b53382b0746d3dc617e15cc2434157.nq.gz
│   ├── f535b0a16295250c22d858667f90f454c7d84c5b.nq.gz
│   ├── f777c3672f106d22f97557113f76134d62d65ffa.nq.gz
│   ├── f8e233b27332b4712304d3226a791d32bdd967c5.nq.gz
│   ├── f8f2303474b97276b56a88c6fcbc10082d165482.nq.gz
│   └── ff9b8bd8b25a79a27680f69e4d21258c25cf78fe.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 45b630a1caba54d4f87e8fde82a4022c96034524.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 49 files
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

[allenai/nora_lib](https://github.com/allenai/nora_lib)

---
*Parsed on 2026-11-07 by [repolex](https://repolex.ai)*
