## Merging

In the main, we write notes on the actual rebasing procedure.
Since this is a new file, it should be easy to merge this file
but the README.md will be tricky.

If we have been working on the same file in main and branch, the rebase command
will give errors:

- Top part (between <<<<<<< and =======): The code currently in main.

- Bottom part (between ======= and >>>>>>>): Your changes from the branch commit Git is applying.

Edit by hand the problematic file and decide what goes where taking into account the above info.

Save the file and do this:

```
git status #you will see hello.py in unmerged paths
git add hello.py
git status # file is now to be commited
```

DO NOT commit yet

```
git rebase --continue
```

We continue with the rebasing working with each problematic file at a time as above.
When we are done we do:

```
git push --force-with-lease private my_branch
```



