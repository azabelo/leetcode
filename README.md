# leetcode
Practice and solutions.

## Create the GitHub remote (run locally with your account)

```bash
cd leetcode
gh repo create <owner>/leetcode --public --source=. --remote=origin --push --description "LeetCode practice and solutions"
```

Replace `<owner>` with your GitHub username or organization. If the repo already exists on GitHub:

```bash
git remote add origin https://github.com/<owner>/leetcode.git
git push -u origin main
```
