# leetcode
Practice and solutions.

**Remote:** https://github.com/azabelo/leetcode

## Clone and work locally

```bash
git clone https://github.com/azabelo/leetcode.git
cd leetcode
```

## Automation and Cursor Cloud

Create or update GitHub resources with the GitHub CLI using a personal access token that has the **`repo`** scope (and org permissions if the repo is under an org).

In Cursor Cloud for this project, a PAT is injected as the environment variable **`github_pat`**. Use it as `GH_TOKEN` so `gh` authenticates as your user instead of the default integration:

```bash
export GH_TOKEN="$github_pat"
gh repo create azabelo/leetcode --public --source=. --remote=origin --push --description "LeetCode practice and solutions"
```

If `git push` fails with **Permission denied to cursor[bot]**, your environment may be rewriting `https://github.com/` URLs to the integration token. Push using a URL that includes the PAT (GitHub documents the `x-access-token` form), or adjust credential helpers so pushes use the same PAT as `GH_TOKEN`.

## Create the repo from scratch (manual / other machines)

```bash
cd leetcode
gh repo create <owner>/leetcode --public --source=. --remote=origin --push --description "LeetCode practice and solutions"
```

Replace `<owner>` with your GitHub username or organization. If the repo already exists:

```bash
git remote add origin https://github.com/<owner>/leetcode.git
git push -u origin main
```
