# Repolex Knowledge Graph of beeware/setuptools_dynamic_dependencies

RDF knowledge graph data for [beeware/setuptools_dynamic_dependencies](https://github.com/beeware/setuptools_dynamic_dependencies), parsed by [repolex](https://repolex.ai).

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
rlex download beeware/setuptools_dynamic_dependencies
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 20c622b695562f55a828bda13d81549a9b7ca53d
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 20c622b695562f55a828bda13d81549a9b7ca53d
│           └── chunk-001.nq.gz
├── blob
│   ├── 0761cebf2bd27acafe2872bd6849690e6592bf5b.nq.gz
│   ├── 3419b44bd627c14c0e4eab35acfe6ea1ae38bc8f.nq.gz
│   ├── 48358cb778bc7a758b86205a97bcfbb0aac54324.nq.gz
│   ├── 699d1abcea467b56e05bad34da5fa4fdea2739b8.nq.gz
│   ├── 6a88bc6da3167ff0088758b04c30bdc6b6d56343.nq.gz
│   ├── 85b9269631ae91558dedfb932f9cdf7702efa180.nq.gz
│   ├── 8f4d891067235bc1b547ec2d9a5278d1d953f71d.nq.gz
│   ├── 9577c97cea71255b4b53925cafc04844dff84c81.nq.gz
│   ├── 9952b0f3bcca15f906c6dcc3a3e433e71e67cd65.nq.gz
│   ├── a5e1214e36b4f375b513362cb1203b73fac30885.nq.gz
│   ├── b834affdddcf5014398ca9c16aafe3ea7f2d0422.nq.gz
│   ├── bd26d83508060c0a53a0ce1221058c001aecb3f4.nq.gz
│   ├── c4d88e8173e484996f9c1fe716bd0fb7e4c8a73b.nq.gz
│   ├── df1fe96e58308f687e12e339fe8857458cffe233.nq.gz
│   └── f7af4dbcb11d67760984edfff9c81a3fa529c991.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 20c622b695562f55a828bda13d81549a9b7ca53d.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 23 files
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

[beeware/setuptools_dynamic_dependencies](https://github.com/beeware/setuptools_dynamic_dependencies)

---
*Parsed on 2026-11-07 by [repolex](https://repolex.ai)*
