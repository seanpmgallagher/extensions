# AnyGit

Source control and pull requests for Git across **GitHub, GitHub Enterprise,
Forgejo, and Gitea** — one panel, with the right backend auto-detected per
repository.

> Based on the official [Git extension](https://github.com/muxy-app/extensions/tree/main/extensions/git)
> by **Saeed Vaziry** ([@saeedvaziry](https://github.com/saeedvaziry)), extended
> with multi-forge pull-request support and several workflow fixes. See
> [Credits](#credits).

## Features

- **Source Control panel** (`cmd+y`) — staged/unstaged changes, stage, commit,
  and discard.
- **Branch switcher** — switch and create branches from the status bar.
- **Diff viewer** — inline file diffs.
- **Pull Requests** — browse PRs, view the current PR for the branch, create,
  mark draft PRs ready, merge, and close.
- **Worktrees** — create and switch worktrees.

## How forge detection works

Pull-request features pick a backend per repository from the `origin` remote:

- **GitHub / GitHub Enterprise** → the [`gh`](https://cli.github.com) CLI.
- **Forgejo / Gitea** → the [`tea`](https://gitea.com/gitea/tea) CLI, when the
  remote host matches one of your `tea login list` entries.

Install whichever CLI(s) you use and authenticate once (`gh auth login` /
`tea login add`). Detection is per repository, so GitHub and Forgejo repos work
side by side. Plain source control (status, commit, branch, diff, worktrees)
uses `git` alone and needs neither CLI.

## Building

```sh
npm install --ignore-scripts
npm run build
```

Then click **Reload** in the Muxy Extensions modal.

## Credits

Original Git extension by **Saeed Vaziry** ([@saeedvaziry](https://github.com/saeedvaziry)).
Multi-forge (Forgejo/Gitea) pull-request support and additional workflow fixes
by **Sean Gallagher** ([@seanpmgallagher](https://github.com/seanpmgallagher)).
MIT licensed.
