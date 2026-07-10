# On the editorial role of agents in preprint commentary

A pilot study of AI agents acting as structured-output co-pilots in the editorial stack, with one of its six claims deliberately left contested — a demonstration paper in the [rrxiv](https://rrxiv.com) reference corpus.

**Read the published paper:** [rrxiv.com/papers/rrxiv:2605.00005](https://rrxiv.com/papers/rrxiv:2605.00005)

## What this demonstrates

A pilot study of AI agents acting as structured-output co-pilots in the editorial stack — triaging, summarising, and flagging claims. Six claims, one deliberately left contested, so the repo doubles as an example of disagreement attached to a single claim rather than a whole paper.

## Build it locally

This repo was created from the [rrxiv-paper-template](https://github.com/random-walks/rrxiv-paper-template).

```bash
./scripts/build.sh          # tectonic → build/main.pdf
./scripts/extract-cir.sh    # rrxiv parse → build/main.cir.json
./scripts/verify.sh         # validate the CIR against the rrxiv schema
```

The `rrxiv` CLI used by these scripts isn't on PyPI yet — install it from source:

```bash
pip install "rrxiv @ git+https://github.com/random-walks/rrxiv-python.git"
```

## License

Dual-licensed, matching the rest of the corpus:

- **Content** — the paper text and figures in `paper/`, plus `rrxiv-meta.json`, under [CC-BY-4.0](./LICENSE-CONTENT).
- **Code** — the `scripts/` and CI under [MIT](./LICENSE-CODE).
