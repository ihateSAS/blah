# blah

## Paired commits

Use the pairing helper after two or more people have genuinely worked on a
change together. It creates a normal commit from changes that are already
staged and adds GitHub's official `Co-authored-by` trailers.

```sh
git add <files-you-worked-on>
./scripts/pair-commit
git push
```

The helper asks for each contributor's name and GitHub-associated email. A
private GitHub email can be entered in the form
`ID+USERNAME@users.noreply.github.com`. It displays the staged-change summary
and requires confirmation before committing. It does not create filler changes
or store contributor email addresses in the repository.


yo
