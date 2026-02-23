# Real World Nuxt

> Real World Nuxt applications and their open source codebases for developers to learn from

This repository aggregates production-quality, open source Nuxt applications into a single collection, allowing you to explore real codebases built by experienced teams and developers. Studying working applications is one of the best ways to level up your skills. Browse the curated apps in the [`apps/`](apps/) subdirectory.

📋 **See [apps.md](apps.md) for a complete list of all included applications with descriptions and versions.**

Real World Nuxt helps developers:

- Explore how production applications structure components, pages, and composables
- Study real implementations of Nuxt 3 features like server API routes and middleware
- See practical examples of state management, API integration, and data fetching patterns
- Discover how teams integrate and configure popular Nuxt modules
- Use LLMs to search across codebases and identify common patterns or best practices
- Reference working code when you're stuck on a specific feature or technique

## How to install on your computer

Ensure you have git installed: https://git-scm.com

```bash
# Clone this git repo:
git clone git@github.com:steveclarke/real-world-nuxt.git

cd real-world-nuxt/

# Run the setup script to initialize all apps:
bin/setup
```

**Or manually:**
```bash
GIT_LFS_SKIP_SMUDGE=1 git submodule update --init --single-branch --jobs 4
```

## Handy Scripts

We've included some helpful scripts in the `bin/` directory:

- **`bin/setup`** - Initialize and download all Nuxt app submodules (run after first clone)
- **`bin/update`** - Pull latest changes from real-world-nuxt and all Nuxt apps
- **`bin/status`** - Show status of all submodules and which apps are initialized

## How to update your local copy of real-world-nuxt

Simply run:
```bash
bin/update
```

**Or manually:**
```bash
git pull
GIT_LFS_SKIP_SMUDGE=1 git submodule update --remote
```

This will pull the latest changes from each Nuxt app (e.g., if the Movies app adds new features, you'll get them).

## Analyze with LLMs

With all the codebases aggregated in one place, you can leverage AI to understand patterns across real-world Nuxt applications:

- Point an LLM (like Claude or Cursor) at the entire `apps/` directory
- Ask questions like "Show me how these apps implement authentication" or "What patterns do they use for data fetching?"
- Compare different approaches to the same problem across multiple codebases
- Discover best practices by analyzing what experienced teams actually do in production
- Search for specific Nuxt features or module usage across all projects at once

### Storing Your Analyses

We've included an `analyses/` directory for you to store your own analysis documents:

- This directory is **git ignored** - your analysis files won't be committed or show up in pull requests
- Store markdown files, notes, code reviews, or any other documentation here
- Safe space for personal observations, learning notes, or work-in-progress research
- Keeps your workspace clean without cluttering the repository

Example: `analyses/movies-playwright-e2e-analysis.md` or `analyses/authentication-patterns.md`

## Contributing

Contributions are welcome! If you know of a great open source Nuxt application, please:

1. Check the criteria below
2. Add it as a submodule
3. Submit a pull request

### Criteria for adding apps

Apps must:
- Be open source and publicly available
- Use Nuxt 3 or Nuxt 4
- Be actively maintained or represent quality code
- Be real-world applications (not just demos or tutorials)
- Have meaningful code to learn from

### How to add a Real World Nuxt app

Given a GitHub repo for a Nuxt app `githubuser/foo`:

```bash
# Inside real-world-nuxt root:
# Replace <DEFAULT_BRANCH> with correct branch (probably 'main' or 'master').
git submodule add -b <DEFAULT_BRANCH> git@github.com:githubuser/foo.git apps/foo
```

### How to remove a git submodule

Only use this if a previously public repo has been removed:

```bash
# Remove the submodule from .git/config
git submodule deinit -f path/to/submodule

# Remove the submodule from .git/modules
rm -rf .git/modules/path/to/submodule

# Remove from .gitmodules and remove the submodule directory
git rm -f path/to/submodule
```

## License

This repository structure and documentation is provided as-is. Each application in the `apps/` directory is licensed under its own terms - please check individual repositories for their licenses.

## Other Real World Codebase Collections

- Real World Rails https://github.com/steveclarke/real-world-rails
- Real World Sinatra https://github.com/jeromedalbert/real-world-sinatra
- Real World Ruby Apps https://github.com/jeromedalbert/real-world-ruby-apps
- Real World Django https://github.com/ckrybus/real-world-django
- Real World Ember https://github.com/eliotsykes/real-world-ember
