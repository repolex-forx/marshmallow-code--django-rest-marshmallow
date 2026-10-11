# Repolex Knowledge Graph of marshmallow-code/django-rest-marshmallow

RDF knowledge graph data for [marshmallow-code/django-rest-marshmallow](https://github.com/marshmallow-code/django-rest-marshmallow), parsed by [repolex](https://repolex.ai).

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
rlex download marshmallow-code/django-rest-marshmallow
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── 117f89bd5f06de6049dd51d4705d0ccafcc351d7
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── 117f89bd5f06de6049dd51d4705d0ccafcc351d7
│           └── chunk-001.nq.gz
├── blob
│   ├── 08f59164cd36cdd8f6e52b0a01da89ae568a554e.nq.gz
│   ├── 350f00e7ecd87d83f08c5e1ce1bbc17f634732fb.nq.gz
│   ├── 3e4d1db119cf79daca03c032ae62d9d6ec12b367.nq.gz
│   ├── 52afaad522617a959e4eaa9ac8b6b07369be0dec.nq.gz
│   ├── 64da9ebcc2c90c118dce3585d677c63fab21e924.nq.gz
│   ├── 68a87caec21e9d06ac391ed490b12e547658bcc9.nq.gz
│   ├── 6e5fccc4231b09e17b7755e21d348a2d364e2bfd.nq.gz
│   ├── 9a1f6e97a22bc5f62d8e4d75c640cfdfa3560370.nq.gz
│   ├── ae5f7dc100774215b13adc94b046a53425ba795c.nq.gz
│   ├── ae73f8379da88b6686722ff3c0c5a5484e868a70.nq.gz
│   ├── c3d0ee9c6c03671112ece7b82ac19b9acf949053.nq.gz
│   ├── c4657ebc3aecbdcb43082cf8402a6776369962a3.nq.gz
│   ├── d4388d3a0bb9b103a320b18a03c793b6cd2f86cb.nq.gz
│   ├── e14d1a7e2c6094e4668ef615eb5ecf9825fa46d2.nq.gz
│   ├── e1d50b87207b8813af433a58d5a2676a32a644e0.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   ├── f85a2dbf4a9dcb3517f42278e10c7c5f7c40b7a0.nq.gz
│   └── fcd39a36b22c635d2c569863671d3f3a73da89ad.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── 117f89bd5f06de6049dd51d4705d0ccafcc351d7.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 26 files
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

[marshmallow-code/django-rest-marshmallow](https://github.com/marshmallow-code/django-rest-marshmallow)

---
*Parsed on 2026-10-11 by [repolex](https://repolex.ai)*
