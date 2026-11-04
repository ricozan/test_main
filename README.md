# test_main
Test having a main and a private branch

## Main commands
```
# add a remote repo
git remote add private https://github.com/your-username/my-private-backup.git

# checkout to branch and push it
git push -u private your-feature-branch

# checkout to main and push it with -u
git checkout main
git push -u origin main

# after this we interact only with its remote repo for main and branch
```

## rebase
Commands needed when the main and the branch develop in parallel.
If you want to fast forward the branch to main, it is good to rebase
often the branch:

```
# 1. Switch to main and pull the latest changes from the public repo
git checkout main
git pull origin main

# 2. Switch to your feature branch
git checkout your-feature-branch

# 3. Rebase your feature branch on top of main
git rebase main
```

And we will need to force the push to private repo:

```
git push --force-with-lease private your-feature-branch
```

And when the branch is ready you can fast forward to main:
```
# 1. Switch to main
git checkout main

# 2. Fast-forward main to your branch
git merge --ff-only your-feature-branch

# 3. Push the updated main to your public repository
git push origin main
```

## Notes

- work a few commits in a private repo
- add a branch and do a few commits
- create a private repo and commit branch there
- turn private to public repo
- a few more commits in both main and branch

