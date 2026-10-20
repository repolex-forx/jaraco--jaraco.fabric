# Repolex Knowledge Graph of jaraco/jaraco.fabric

RDF knowledge graph data for [jaraco/jaraco.fabric](https://github.com/jaraco/jaraco.fabric), parsed by [repolex](https://repolex.ai).

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
rlex download jaraco/jaraco.fabric
```

Consult `rlex --help` for other options, including SPARQL queries, HTTP server, and interactive visualization.

## Data structure

All data is stored as gzip-compressed [N-Quads](https://www.w3.org/TR/n-quads/) (`.nq.gz`), a standard RDF format that can be loaded into any triplestore or graph database.

```
.
├── aggregate
│   ├── ast
│   │   └── e10c79238c84ee8ac3bfaceafffad44dbf46a413
│   │       └── chunk-001.nq.gz
│   └── repolex
│       └── e10c79238c84ee8ac3bfaceafffad44dbf46a413
│           └── chunk-001.nq.gz
├── blob
│   ├── 10d412f406891b9683f832fcbc134c9bdf4f916e.nq.gz
│   ├── 240329c3604d8ead4c10aa8c88352caa8e4ce7b2.nq.gz
│   ├── 2e3f4dd791a6372b427d618eb0baa8c4dc58e5f0.nq.gz
│   ├── 304196f81e11a168c9894f966e4a617ebf4ed53c.nq.gz
│   ├── 415476e77cc2c51869da0ebaaf3f10b301df8450.nq.gz
│   ├── 54c9000ec94341dd65c2053251b85b124017b9b5.nq.gz
│   ├── 54cc8303b22089e12053e552d4e6cb852a865b8a.nq.gz
│   ├── 5503eeb57885bac86e31cbf1ecbdcc8930c50830.nq.gz
│   ├── 55c63da30ef19c5646c4eaa61b5fbb206bd5ffc9.nq.gz
│   ├── 577e87a793a20e413f7321f4f17ec1eba2ea1962.nq.gz
│   ├── 57eaf69866e91ae72bdf8c975a2642ad9b0ab71b.nq.gz
│   ├── 5a726a1faefc5447d330c717234e6bac0de7c337.nq.gz
│   ├── 5bdc232005af9be104a00437ae9bc64417a4c1cc.nq.gz
│   ├── 6cb940fc540d2432a172bf5a13b8098346167023.nq.gz
│   ├── 700235be57c1b2872455c0be5333f59cf568e252.nq.gz
│   ├── 724370638fc188317bbc7dc868f1a571995fd796.nq.gz
│   ├── 733ea64a54aca2e80982dad8ba6c6c91a8f38a6b.nq.gz
│   ├── 9a0f3bce1395ae3819030b822e5d9076c85068ea.nq.gz
│   ├── 9a32d0369ea4b680ff4fbef460d2ca2addee2e70.nq.gz
│   ├── 9d2b4784713b00f8c46e6d0dca945384d4406ce1.nq.gz
│   ├── a1a016a591b9985c164c243447c9c6bcc6dcfcf6.nq.gz
│   ├── a1ce4bc0c3ceae2dbee9cd0f0f95a8e41fe31ae6.nq.gz
│   ├── a92efcb38c6f8dd858878f7e6a69ba5869802552.nq.gz
│   ├── aa7c13a282f8f50a814abad12e7c806329f3fd5a.nq.gz
│   ├── b1bfb75fb2a579957b2d644f69327288f9b06292.nq.gz
│   ├── d445e7771532961b39839ca9a27ba4aee8c0d13e.nq.gz
│   ├── d8dd5df47f963a25a30fdd91979f8d5aea3eaed3.nq.gz
│   ├── d94c7eb2fc92f8ad14b11ce081a9d188aa67a4f0.nq.gz
│   ├── e05a3d4a2ab888e32952006d8cd380864368db5f.nq.gz
│   ├── e69de29bb2d1d6434b8b29ae775ad8c2e48c5391.nq.gz
│   └── e74893636d3a7a75135e19de444552eb5423d7d0.nq.gz
├── branch
│   └── branch.nq.gz
├── commit
│   └── commit.nq.gz
├── filetree
│   └── e10c79238c84ee8ac3bfaceafffad44dbf46a413.nq.gz
├── issue
│   └── issue.nq.gz
├── pr
│   └── pr.nq.gz
└── tag
    └── tag.nq.gz

13 directories, 39 files
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

[jaraco/jaraco.fabric](https://github.com/jaraco/jaraco.fabric)

---
*Parsed on 2026-10-20 by [repolex](https://repolex.ai)*
