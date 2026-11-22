# AGENTS.md — cyb.money

> the doctrine of the home is `~/cyber/AGENTS.md`; it applies here first.

this repository is one product: CYB, the root money of cyber, with its network's definition, its genesis and its site. it holds no code of a node and no client. its layout is the standard of cybernode `specs/network.md`; the twins are `BOOT` and `PUSSY`. the repository is named after the site because GitHub reads `CYB` and `cyb` as one name and `cyb` is the browser.

## what lives here

- `network.toml` — the identity and rules of the network, a draft that states only what is decided
- `genesis/` — the sources (the proven states of pussy and bostrom), the claims, the empty graph, the lock (not built)
- `endpoints.toml` — the site
- `site/` — cyb.money: static files, no build, no Node
- `docs/` — the history, the economy of the token, what can be run

the node is cyberia-to/cybernode; the client `cyber` and the protocol's pages are cyberia-to/cyber. a change to how a network runs goes to the node; a change to what CYB is goes here.

## rules

- nothing of CYB runs. a file here never says otherwise: a value is decided, proposed or open, and says which.
- the native token's key is `token`.
- `docs/economics.md` follows `cyber/$CYB.md` of the repository cyber; a figure changes there first.
- `genesis/genesis.lock` is written by the first build, with a receipt in `audit/` of two independent builds.
- the genesis file is never committed; it is built.

## checks before a commit

- `python3 -c "import tomllib,sys; [tomllib.load(open(f,'rb')) for f in sys.argv[1:]]" network.toml endpoints.toml genesis/sources.toml genesis/distribution.toml genesis/graph.toml genesis/genesis.lock`
- the site opens when served from `site/`: `python3 -m http.server -d site 8767`, then `python3 ~/cyber/cyber/scripts/cdp.py http://localhost:8767/`
