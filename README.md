# TIPS AND TRICKS FOR CREATING YOUR OWN SITE ON GITHUB

> [!NOTE]
> Sections marked with :copilot: are AI-generated.

## Create a site

[Read this doc](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-github-pages-site)! Your site works immediately after the **first section** (or, depending on your case, the second). It's quicker and more informative than any tutorials you're thinking of, I promise.

## Commits

> [!TIP]
> **Commit early and often!**. Commits are **easy and free**—it’s perfectly acceptable to have many very small commits, as long as each one is a single logical unit.
> 
> —[Standard Ebooks](https://standardebooks.org/contribute/producing-an-ebook-step-by-step) (kind of)

## Reverting changes :copilot:

Q. If I created and pushed commit 1, 2 and 3, and want to return my repo to its state at commit 1, what should i do?

A. Get the hash of commit 1 with `git log --oneline`, then run:

```bash
git revert --no-commit <hash-of-commit-3> <hash-of-commit-2>
git commit -m "Revert to state at commit 1"
git push
```

The `--no-commit` flag stages both reverts together so you end up with one clean revert commit. Your files will match commit 1, and the history will show what happened.
