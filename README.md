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

## Notes

- work a few commits in a private repo
- add a branch and do a few commits
- create a private repo and commit branch there
- turn private to public repo
- a few more commits in both main and branch

