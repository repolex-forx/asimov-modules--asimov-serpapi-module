# Repolex Knowledge Graph of asimov-modules/asimov-serpapi-module

RDF knowledge graph data for [asimov-modules/asimov-serpapi-module](https://github.com/asimov-modules/asimov-serpapi-module), parsed by [repolex](https://repolex.ai).

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
rlex download asimov-modules/asimov-serpapi-module
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── c6a936e7a00a63e711ab711819ed7eaf8240d17b
│   │       └── chunk-001.nq.gz
│   ├── lsp
│   │   └── c6a936e7a00a63e711ab711819ed7eaf8240d17b.nq.gz
│   └── repolex
│       └── c6a936e7a00a63e711ab711819ed7eaf8240d17b
│           └── chunk-001.nq.gz
├── blob
│   ├── 1a5b0da6a5d347b93ba236c3cdb017ec9337f56a.nq.gz
│   ├── 2391f73aa051d3804285ce744f2e9a1c7e08993d.nq.gz
│   ├── 2d73eb741c9c483ab838f605d80882d6f5c49d1f.nq.gz
│   ├── 337498f462c6797e905507324a577b68887ccc4d.nq.gz
│   ├── 3b0c8d61a8097f7e36cd9b2844d773308874460b.nq.gz
│   ├── 4916d79ff1ff69ec5f8459ddf229071a79233e70.nq.gz
│   ├── 570028147ce84c25146aa6d9e532c5f62c4d7394.nq.gz
│   ├── 5f5cf896c81688e4360b37f1bcda92f7bc6f7423.nq.gz
│   ├── 6b23d61018f43b840f8d2ff3b45a1c02d76df38d.nq.gz
│   ├── 6ef3b13114fa1800f140e0b8066791d69137c40e.nq.gz
│   ├── 75e3b65f99b29f48ab230e3eab3de8d0b7a9229f.nq.gz
│   ├── 7a25183c6dcd4a6bc293302c254407334fc65317.nq.gz
│   ├── 845639eef26c0e95586203ae78369f67552ccb17.nq.gz
│   ├── 8a320a6836f445052c0eabac1a7ef9aa9b270a2f.nq.gz
│   ├── 9bb31a4a140042cc39d48964dcbefe12cd5b9af9.nq.gz
│   ├── 9ddc1e65142cb3ee18435f7a814d7b90e66b65da.nq.gz
│   ├── a36fedab8db68b26a76fbbf1de1f549e4a12261b.nq.gz
│   ├── a4087d4dd0a8b2b12a91d512aba5887f43cac61f.nq.gz
│   ├── a732960f8c75659d6484c3563793f92fdef319bd.nq.gz
│   ├── abdeb353275c15639f9b0a51edb3e3e53fb10acd.nq.gz
│   ├── af9908b08f4b33c32a0080af73f53bc0fa0cdce4.nq.gz
│   ├── b5aefec5816b3f3225179aceaca835c6344cd378.nq.gz
│   ├── ba096cab9cd00927e8848710ddfcdd4cbd4e503f.nq.gz
│   ├── c3896c4a610edef5c30ad8a9358aaf3121eab20f.nq.gz
│   ├── cf42f6893594e2f8be2b722de51123d65e4d61c4.nq.gz
│   ├── d2429e0193d52c7c5d8cd29c39a8863f961e31d3.nq.gz
│   ├── d3a742a174aede457bb20ba5023ff25e46d88ba6.nq.gz
│   ├── d55b25abb746b8add3e2912d0cf0bf4d6e4dcc64.nq.gz
│   ├── e3e57a8ce4ccbf74759a6df8fa4a3980ff1c9209.nq.gz
│   ├── ec694c229cd97c685b3e86985fd6f19a929a6b4d.nq.gz
│   ├── ee93a54c693d34c90354aed98159a9c9d80cc28e.nq.gz
│   ├── efb98088164f5786b17e83ed384971fc3c74f93c.nq.gz
│   └── ff1b626f30ce14b6e08318fc27c1e40679e4836d.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── dep
│   └── c6a936e7a00a63e711ab711819ed7eaf8240d17b.nq.gz
├── filetree
│   └── c6a936e7a00a63e711ab711819ed7eaf8240d17b.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

14 directories, 42 files
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

[asimov-modules/asimov-serpapi-module](https://github.com/asimov-modules/asimov-serpapi-module)

---
*Parsed on 2026-09-28 by [repolex](https://repolex.ai)*
