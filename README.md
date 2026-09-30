# pure-libs

### 123 zero-dependency micro-libraries. One repo per thing. Stdlib only.

I build tiny packages that do exactly one thing: a CRC variant, a classic hash,
an RFC-correct HTTP header parser, a crypto primitive, an MCP agent tool.
No dependencies, no lockfiles — every package runs on the language standard
library alone. MIT licensed, tested, documented.

**Browse everything:** [the catalog](https://prasad-a-abhishek.github.io/pure-libs/)

### Start here

| Package | What it does | Install |
|---|---|---|
| [csvcomp](https://github.com/prasad-a-abhishek/csvcomp) | Semantic CSV diff: schema + rows + cells | `pip install csvcomp` |
| [argpeek](https://github.com/prasad-a-abhishek/argpeek) | argv inspector + safe shell replay for CLIs | `pip install argpeek` |
| [ulid-pure](https://github.com/prasad-a-abhishek/ulid-pure) | ULID encode/decode, pure stdlib | `pip install ulid-pure` |
| [crc16-modbus-pure](https://github.com/prasad-a-abhishek/crc16-modbus-pure) | CRC-16/MODBUS with canonical check value | `pip install crc16-modbus-pure` |

### Benchmarked, not just claimed

Every package was benchmarked against the most popular existing library for
the same job — correctness first, then size, then speed (timeit best-of-5,
identical inputs). Smaller won nearly everywhere (typically 5–50x fewer
lines). These also won on speed:

- [mcpschema](https://github.com/prasad-a-abhishek/mcpschema) — 7.1x faster than langchain-mcp-adapters, ~800x smaller install
- [iban-pure](https://github.com/prasad-a-abhishek/iban-pure) — 23x faster than schwifty
- [diffpriv-pure](https://github.com/prasad-a-abhishek/diffpriv-pure) — 12x faster than diffprivlib
- [csvcomp](https://github.com/prasad-a-abhishek/csvcomp) — beats pandas on a 5,000-row keyed diff, ~5,500x smaller installed
- [cronlint](https://github.com/prasad-a-abhishek/cronlint) — 5.2x faster than croniter
- [isbn-pure](https://github.com/prasad-a-abhishek/isbn-pure) — 2.6x faster than isbnlib
- [purl-parse-pure](https://github.com/prasad-a-abhishek/purl-parse-pure) — 2.2x faster than packageurl-python
- [iso7064-pure](https://github.com/prasad-a-abhishek/iso7064-pure) — up to 4.1x faster than python-stdnum
- [accept-header](https://github.com/prasad-a-abhishek/accept-header) — 2.75x faster than npm `accepts`

Where pure Python lost on speed (zlib, xxhash, `cryptography`, scipy), the
repos say so. The catalog marks every verified win: [browse all 123](https://prasad-a-abhishek.github.io/pure-libs/)

### The families

- **Dev tools & CLI** — csvcomp, argpeek, hush, scrublog, urlcanary, cronlint…
- **Checksums & CRC** — 30+ variants: crc16-modbus, crc32, crc64-xz, fletcher, adler-32…
- **Hashes & sequences** — djb2, fnv, murmur, siphash, xxh3, sobol, xorshift32…
- **HTTP & web standards** — 25 RFC-correct header parsers: forwarded, cache-control, etag, sfv…
- **Crypto, identity & encoding** — pbkdf2, hkdf, ulid, jwk-thumbprint, isbn, iban…
- **AI agents & MCP** — mcpsnoop, mcp-promptdiff, tool-call-warrant, agent-replay-journal…

### What I aim for in every package

1. Zero runtime dependencies — stdlib only
2. Tests with canonical vectors (checksums) or RFC section references (parsers)
3. Spec doc + QA report in the repo
4. MIT license

### Publishing status

39 of 123 on PyPI and counting — working through the rest.
Open an issue on any repo to request the next publish.
