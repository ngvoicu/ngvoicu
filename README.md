# Gabriel Voicu

Software engineer and AI-native consultant. Open-source tools for AI coding agents and the models behind them.

I build open-source tools for AI coding agents and for the models behind them, and use them on real work every day. I also help companies [become AI-native](https://ngvoicu.dev/#consulting): AI built into the workflow by design, with humans owning truth, risk, and direction. The playbook is written down in [Becoming an AI Native Company](https://ngvoicu.dev/becoming-an-ai-native-company/).

## The AI-native toolkit

Free and open source, MIT licensed.

| Tool | What it does | Repo |
|---|---|---|
| **[ConsensFlow](https://consensflow.ngvoicu.dev)** | A desktop app (macOS, Windows) that runs a team of AI coding agents on your project. You talk to a chief agent; it plans the work on a board, and a staff in nine roles (workers, reviewers, testers, designers and more) takes the tasks, each in its own terminal running Claude Code, Codex, Pi, Devin, or Muse Code. Rust engine; [releases](https://github.com/ngvoicu/consensflow/releases). | [`consensflow`](https://github.com/ngvoicu/consensflow) |
| **[Kluris](https://kluris.ngvoicu.dev)** | The SME your team never had: one shared brain for all your AI agents, kept as markdown in git. Agents propose, people approve. | [`kluris`](https://github.com/ngvoicu/kluris) |
| **[Specmint](https://specmint.ngvoicu.dev)** | AI coding specs that survive the session: research and interviews first, then a spec in your repo that any tool can resume. | [`specmint-core`](https://github.com/ngvoicu/specmint-core) · [`specmint-tdd`](https://github.com/ngvoicu/specmint-tdd), each also in an HTML edition ([`core`](https://github.com/ngvoicu/specmint-core-html), [`tdd`](https://github.com/ngvoicu/specmint-tdd-html)) |

## providers.dev

The models behind the agents, as each provider and access method really exposes them, and the tools to use them well. Free and open source, MIT licensed.

| Tool | What it does | Repo |
|---|---|---|
| **[providers.dev](https://providers.dev)** | The real context window, output limit, price and cache lifetime of a model for the way you actually reach it, subscription logins included, so your tools compact and cache against the right numbers. One safe value per quantity, measured where it can be, with every source beside it, on a page per model and in a free JSON API. | [`providers.dev`](https://github.com/ngvoicu/providers.dev) |
| **[Provimux](https://provimux.providers.dev)** | Every AI account you pay for, behind one key: a self-hosted gateway (OpenAI-, Claude- and Gemini-compatible) for you or your whole team, with the accounts tried in your order under names of your own, the prompt cache kept in use so you pay for a prompt once, and a page that shows what caching was worth. My distribution of [CLIProxyAPI](https://github.com/router-for-me/CLIProxyAPI). | [`provimux`](https://github.com/ngvoicu/provimux) · console [`provimux-ui`](https://github.com/ngvoicu/provimux-ui) · Homebrew [`homebrew-tap`](https://github.com/ngvoicu/homebrew-tap) |
| **[pi-provimux](https://provimux.providers.dev/#pi)** | The Pi extension for Provimux: every model your Provimux serves appears in Pi's `/model`, its name saying which accounts serve it, and other extensions learn which one answered. | [`pi-provimux`](https://github.com/ngvoicu/pi-provimux) |
| **[pi-cache-keeper](https://pi-cache-keeper.providers.dev)** | Makes a long Pi session cost less: it compacts at the right moment, from the warm cache at about a tenth of the input price when the context is full and before the cache expires, and with a cheaper model you pick when the cache is already cold; and it keeps the cache warm through a break instead of paying to write the session again. Grew from Nico Bailon's [pi-cached-compaction](https://github.com/nicobailon/pi-cached-compaction). | [`pi-cache-keeper`](https://github.com/ngvoicu/pi-cache-keeper) |
| **groundtruth** | The measuring tool behind providers.dev: how long prompt caches really live and how large the limits really are, per endpoint, model and route, subscription logins measured first through the vendors' own clients. | [`groundtruth`](https://github.com/ngvoicu/groundtruth) |

## Watch it work

Short demos on [YouTube](https://www.youtube.com/@CodeWithZee): actual agents, actual outputs, no mockups.

- Latest: [ConsensFlow: a second AI opinion inside Claude Code & Pi](https://www.youtube.com/watch?v=iKuBFEDE8Go). It shows the earlier plugin version, before ConsensFlow became a desktop app.
- [Kluris: give your AI agents one shared memory](https://www.youtube.com/watch?v=ei1F0ZbNX3o)
- [Specmint: AI coding specs that survive the session](https://www.youtube.com/watch?v=QSI-C57bt78)

## Elsewhere

[ngvoicu.dev](https://ngvoicu.dev) · [Articles](https://ngvoicu.dev/articles/) · [YouTube](https://www.youtube.com/@CodeWithZee) · [LinkedIn](https://www.linkedin.com/in/ngvoicu/) · [Medium](https://medium.com/@ngvoicu) · [office@ngvoicu.dev](mailto:office@ngvoicu.dev)
