# Real World Nuxt

> Real World Nuxt applications and their open source codebases for developers to learn from

This project brings production, open source Nuxt apps together in one repository. Having real codebases aggregated in a single place has always been valuable for learning — but it's become dramatically more useful in the age of AI coding agents.

See [apps.md](apps.md) for the full list of included apps with descriptions.

## Why this matters now

With all these codebases in one directory, you can point an agent at production Nuxt apps and ask questions like:

- "How do these apps implement authentication?"
- "Show me every approach to data fetching across these codebases"
- "What patterns do apps use for middleware?"
- "Compare state management implementations across apps"

An agent can search, read, and cross-reference code across every app instantly — something that would have taken hours of manual work before.

### Storing your analyses

The `analyses/` directory is git-ignored — a safe place to store your own research:

- Markdown files, notes, pattern comparisons, or any documentation
- Won't be committed or show up in pull requests
- Keeps your workspace clean while working alongside the codebases

## Getting started

Ensure you have git-lfs installed: https://git-lfs.com

```bash
git clone git@github.com:steveclarke/real-world-nuxt.git
cd real-world-nuxt/
bin/setup
```

## Staying up to date

Submodules are pinned to specific commits. When the repo is updated, pull and sync:

```bash
git pull
git submodule update
```

If you want to update all submodules to the absolute latest right now, run `bin/update`.

## Scripts

- **`bin/setup`** — Initialize and download all submodules (run after first clone)
- **`bin/update`** — Pull latest changes and update all submodules to their latest remote commits
- **`bin/status`** — Show how many apps are initialized
- **`bin/add`** — Add a new app by GitHub URL (e.g. `bin/add https://github.com/user/repo`)

## Contributing

Know of a great open source Nuxt app that should be in here? The easiest way is to [open an issue](https://github.com/steveclarke/real-world-nuxt/issues/new) with the GitHub URL and we'll add it.

If you already have the repo cloned, you can also submit a PR:

```bash
bin/add https://github.com/githubuser/foo
# then commit and open a pull request
```

#### Criteria for adding apps

Apps should:
- Be open source and publicly available on GitHub
- Be built with Nuxt 3 or Nuxt 4
- Be actively maintained or represent quality code worth studying
- Be real-world applications (not just demos or tutorials)

## Other Real World Codebase Collections

- [Real World Rails](https://github.com/steveclarke/real-world-rails)
- [Real World Ruby Apps](https://github.com/jeromedalbert/real-world-ruby-apps)
- [Real World Sinatra](https://github.com/jeromedalbert/real-world-sinatra)
- [Real World Django](https://github.com/ckrybus/real-world-django)
