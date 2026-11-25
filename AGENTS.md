# Agent instructions: ngvoicu profile README

This file exists twice, as `CLAUDE.md` and `AGENTS.md`, and the two are byte-identical. Edit one, copy it over the other, and check with `cmp CLAUDE.md AGENTS.md`.

## What this repo is

`ngvoicu/ngvoicu` holds Gabriel Voicu's GitHub profile README, shown at https://github.com/ngvoicu. `README.md` is the only file the profile shows; the rest is for agents.

## What to keep true

- **The toolkit table.** ConsensFlow, Kluris and Specmint, each with its `*.ngvoicu.dev` site and its repo, described as they are today. Before changing a row, read the product's repo README, its latest release and its site. If they disagree, the repo and the release win; tell the owner which page is behind.
- **The providers.dev table.** providers.dev, Provimux, pi-provimux, pi-cache-keeper and groundtruth, the work under `providers.dev`, kept apart from the toolkit on `*.ngvoicu.dev`. Their truth lives in the same three places, and the same rule decides:
  - providers.dev: the `providers.dev` repo's README and https://providers.dev (no releases; the site deploys from `main`).
  - Provimux: the `provimux` README and latest release, https://provimux.providers.dev; its console `provimux-ui` (README and release) and the Homebrew tap `homebrew-tap`. Provimux is built on CLIProxyAPI by router-for-me; the row says so.
  - pi-provimux: the `pi-provimux` README and release, its npm package, and the "For pi" section of Provimux's site (`https://provimux.providers.dev/#pi`); it has no site of its own.
  - pi-cache-keeper: the `pi-cache-keeper` README and release, its npm package, https://pi-cache-keeper.providers.dev. It is based on pi-cached-compaction by Nico Bailon; keep that credit wherever its origin is described.
  - groundtruth: the `groundtruth` README; it has no site and no releases.
- **Links.** Never link a retired domain (`kluris.io`, `specmint.io`) or the archived `ngvoicu/consensflow-cc`. Provimux's support page is `https://provimux.providers.dev/support/`, not the old `https://providers.dev/support/` (it only redirects), and Provimux's and pi-cache-keeper's sites are their subdomains, not paths under `providers.dev`. Don't link npmjs.com: it answers `403` to scripts; each repo links its package. ConsensFlow downloads go to `https://github.com/ngvoicu/consensflow/releases`, which lists both channels: GitHub's `/releases/latest` is the latest stable release, while the alphas, which run ahead of it, are prereleases. Don't pin version numbers, and don't call them alphas or prereleases in the text: they are releases, and they ship often.
- **The latest video.** The first item under "Watch it work" is the newest full video on https://www.youtube.com/@CodeWithZee (Shorts are clips of those and don't count). Update it the day a video publishes. A video that shows an older version of a product says so.
- **The tone.** Real tools, real workflows, no hype. Short. No emojis, no badge walls.
- **Contact.** `office@ngvoicu.dev` is the one email address the profile shows, as a `mailto:` link at the end of the "Elsewhere" line (ngvoicu.dev links the same address). No other address, personal or otherwise.

## Remotes

- `origin` is the owner's NAS mirror (`ssh://git@zeenas:2222/ngvoicu/ngvoicu.git`).
- `upstream` is GitHub (`https://github.com/ngvoicu/ngvoicu.git`); its `main` is the public profile.

Publishing the profile is `git push upstream main`, and the owner does it after review. Don't push to `upstream`.

## Check links before committing

Each line should start with `200`:

```sh
grep -oE 'https://[^) ]+' README.md | sort -u | while read -r url; do
  echo "$(curl -sSL -o /dev/null -w '%{http_code}' -A 'Mozilla/5.0 (Macintosh)' "$url") $url"
done
```

- Medium answers `403` to scripts. Check `https://medium.com/feed/@ngvoicu` instead: it should list his posts.
- YouTube answers `200` even for a deleted video. Check each video with `curl -s "https://www.youtube.com/oembed?url=<video-url>&format=json"`: it should print the video's title, not `Not Found` or `Unauthorized`.
- `grep -nE 'kluris\.io|specmint\.io|consensflow-cc' README.md` prints nothing.
