# awesome-antseed

A curated list of [antseed](https://antseed.com) resources, tools, and hard-won notes.

## Contents

- [Tools](#tools)
- [Guides](#guides)
- [Notes from production](#notes-from-production)

## Tools

- [antseed-seller-watchdog](https://github.com/Dijinlong/antseed-seller-watchdog) — catch the silent failures that make a node invisible
- [antseed-network-stats](https://github.com/Dijinlong/antseed-network-stats) — snapshot the whole seller network
- [base-gas-guard](https://github.com/Dijinlong/base-gas-guard) — get warned before a Base wallet runs dry
- [llm-endpoint-bench](https://github.com/Dijinlong/llm-endpoint-bench) — benchmark OpenAI-compatible endpoints
- [antseed-price-sync](https://github.com/Dijinlong/antseed-price-sync) — keep pricing aligned with upstream cost

## Guides

*(contributions welcome)*

## Notes from production

Things that cost real time to learn, written down so they cost you nothing:

- **A running process is not a visible node.** Advertising can pause while the
  process stays healthy and the port stays open.
- **Look at `providers`, not at the HTTP status.** `/metadata` can return 200 with an
  empty provider list.
- **Trust is a gate, not a rank.** Buyers configured with a trust floor drop you
  entirely — price never enters the picture.
- **Delegated sellers do not have their own policy.** Check the delegating seller's
  rules before blaming your own config.

## Contributing

Open a PR. Keep entries short and honest — this list is more useful when it admits
what does not work yet.
