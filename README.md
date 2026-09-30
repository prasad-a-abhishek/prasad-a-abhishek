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
