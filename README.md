# Testing GitHub Merge Strategies

This was a little playground for myself to see what GitHub does with the three different options
for merging Pull Requests:

1. Create a merge commit
2. Squash and merge
3. Rebase and merge

Specifically I wanted to know if option 2) would create a merge commit. The results were as follows:

## Create a merge commit

This seems to be the equivalent of `git merge --no-ff` - it will create a special merge commit
that references the commits being merged.

## Squash and merge

This seems to be the equivalent of squashing all the commits and then doing a `git merge` so this
will fast-forward the commit directly onto the destination branch if possible.

## Rebase and merge

This seems to be the equivalent of `git rebase`ing all the commits onto the destination branch.
