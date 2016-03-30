# intro-git

This is a simple example where merging branches will cause a conflict.

If you try to merge branch `master` with branch `first-line`:

```
$ git merge first-line
```

*git* will notice that both branches have changed the same line
and doesn't know how to proceed (which change should stay, if any).
If you open that has conflicts you will see something of the form:

```
<<<<<<< HEAD
Test test
=======
This is my first change
>>>>>>> first-line
```

When fixing a conflict, `HEAD` refers to the
current branch in which you are (`master`) and the other commit
refers to the "other" branch, in this case, `first-line`.

To resolve the conflict:

1. decide what to keep and what to remove
2. `git add <file-that-you-fixed>` (`git add example.md`)
3. `git commit`
4. Done! :)
