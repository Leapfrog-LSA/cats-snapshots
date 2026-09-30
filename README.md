# cats-snapshots

Daily RSS snapshots of the labelled OSINT sources used to calibrate and validate
[CATS](https://github.com/Leapfrog-LSA/CATS-Contextual-Ambiguity-Trust-Scoring).
This is a data repository: the collector code and `data/labels.jsonl` live in the CATS repo.

- `snapshots/labelled_sources_<YYYY-MM-DD>.jsonl` — one snapshot per UTC day.
- `SHA256SUMS` — plain `sha256sum` manifest of every snapshot; verify with `sha256sum -c SHA256SUMS`.
- Same-day collisions are always unioned with `python -m cats.calibration.merge_snapshots`, never overwritten.

Consumers mirror this repo into `data/snapshots/` with `make snapshots-download` in the CATS repo.
