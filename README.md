# pair-

A simple helper for creating paired commits that satisfy GitHub's co-authoring requirements for the Pair Extraordinaire badge.

## What this does

This repository gives you a script you can use to make a commit with proper `Co-authored-by` trailers for two contributors. That is the GitHub-supported way to show that two people worked together on the same change.

## Why this matters

To get the GitHub Pair Extraordinaire badge, you typically need to have commits where multiple people are credited as co-authors on the same commit, and the commit must be in the public contribution graph for both accounts.

This repo is designed to make that easy for a pair such as:

- ihateSAS
- pyrrhonic

## How to use it

1. Clone this repo.
2. Make sure your changes are staged:

```sh
git add <files-you-worked-on>
```

3. Run the helper:

```sh
./scripts/pair-commit
```

4. Enter:

- the commit message
- contributor 1 name and GitHub-associated email
- contributor 2 name and GitHub-associated email

5. Confirm the commit.

6. Push the commit:

```sh
git push
```

## GitHub email format

Use the email associated with each GitHub account. If you want to keep your email private, you can use your GitHub noreply email address, which usually looks like:

```text
12345678+username@users.noreply.github.com
```

You can find that in GitHub Settings → Emails.

## Example

If you and your friend are working together, the helper will create a commit like this:

```text
Co-authored-by: ihateSAS <ihateSAS@users.noreply.github.com>
Co-authored-by: pyrrhonic <pyrrhonic@users.noreply.github.com>
```

## Important notes

- Both accounts must be genuinely involved in the work.
- The co-author trailers must be present in the final commit history.
- Doing this in a public repository is the usual path for the badge.
- The script only helps you generate the correct commit metadata; GitHub decides whether the badge is awarded based on their system.

## Related resource

This was inspired by the idea behind the GitHub badge setup used in projects like the one linked in your example:

- https://github.com/SIMARSINGHRAYAT/Gitzo

## Next step

After you commit and push a few paired commits, open your GitHub profile and check whether the badge appears under your achievements area.
