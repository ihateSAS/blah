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
* **Privacy Support:** You can use a **private GitHub email** formatted as `ID+USERNAME@users.noreply.github.com`.
* **Verification:** It displays a summary of your staged changes and requires confirmation before committing.

### 💡 How to find your Private GitHub Email

If you want to keep your personal email private, you can find your unique GitHub ID and noreply email by following these steps:

1. Go to your GitHub **Settings** -> **Emails**.
2. Scroll down to the **Keep my email addresses private** section.
3. Copy the email address shown there (it will look like `12345678+username@users.noreply.github.com`).

*Note: This script never creates filler changes or stores contributor email addresses within the repository history.*

### Verify the attribution

After pushing, open the commit on GitHub and confirm that every contributor is
shown as a co-author. If someone is missing, check that their trailer has the
exact `Co-authored-by: Name <email>` format and that the email belongs to their
GitHub account. When contributing through a pull request, verify that the merge
method preserves the trailer in the final commit history.
