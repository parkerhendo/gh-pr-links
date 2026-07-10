# gh-pr-links

A [GitHub CLI](https://cli.github.com) extension that lists every link found
in the comments on the current branch's pull request — deploy previews
(Vercel, Netlify, Cloudflare, Railway, ...), CI logs, docs, whatever — and
lets you pick one to open in your browser.

## Installation

```sh
gh extension install parkerhendo/gh-pr-links
```

Or from a local checkout:

```sh
cd gh-pr-links
gh extension install .
```

## Usage

```sh
gh pr-links           # list links, pick one to open (Enter to skip)
gh pr-links --print   # print URLs only, no prompt
```

Example:

```
 1) https://myapp-git-my-branch.vercel.app
 2) https://vercel.com/me/myapp/DKxYn8oVaB
 3) https://myapp-pr-42.up.railway.app
Open which? [1-3, Enter to skip]
```

Image embeds are skipped, and duplicate URLs are deduped.
