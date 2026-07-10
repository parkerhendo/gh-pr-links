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

Requires `jq`.

## Usage

```sh
gh pr-links           # list links, pick one to open (Enter to skip)
gh pr-links --print   # print URLs only, no prompt
```

Example:

```
Links in comments on PR #42:
1)  Visit Preview (vercel[bot])   https://myapp-git-my-branch.vercel.app
2)  Inspect (vercel[bot])        https://vercel.com/me/myapp/DKxYn8oVaB
3)  Web (railway-app[bot])       https://myapp-pr-42.up.railway.app
Open which? [1-3, Enter to skip]
```

Markdown link text and comment author are shown for context. Image embeds
are skipped, and duplicate URLs are deduped.
