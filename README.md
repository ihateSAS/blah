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


### 💡 How to find your Private GitHub Email
If you want to keep your personal email private, you can find your unique GitHub ID and noreply email by following these steps:
1. Go to your GitHub **Settings** -> **Emails**.
2. Scroll down to the **Keep my email addresses private** section.
3. Copy the email address shown there (it will look exactly like `12345678+username@://github.com`).

*Note: This script never creates filler changes or stores contributor email addresses within the repository history.*
