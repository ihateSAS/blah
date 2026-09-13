# Co-authoring Changes

## Paired commits

Use the pairing helper after two or more people have genuinely worked on a change together. It creates a standard commit from your staged changes and automatically adds GitHub's official `Co-authored-by` trailers.

```sh
# Stage your changes
git add <files-you-worked-on>

# Run the pairing helper
./scripts/pair-commit

# Push to the remote repository
git push
```

### How it works
The helper walks you through a few quick steps before finalizing the commit:
* **Contributor Info:** It asks for each contributor's name and GitHub-associated email. 
* **Privacy Support:** You can use a **private GitHub email** formatted as `ID+USERNAME@://github.com`.
* **Verification:** It displays a summary of your staged changes and requires confirmation before committing.


