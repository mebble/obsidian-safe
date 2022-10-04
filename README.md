# Obsidian Safe

Back up your [Obsidian](https://obsidian.md/) vault in [git](https://git-scm.com/).
## Requirements

- Git
- Python 3

## Usage

1. Clone this repository
2. Open this project in Obsidian
3. Edit your notes
4. Do one of the following:

Commit your staged notes:

```
./lock
```

Commit all your notes (including unstaged and untracked):

```
./lock all
```

Sync your notes to the remote:

```
./lock up
```

## About

This tool is for backing up your Obsidian vault in a git repository. By using git, we can ensure our Obsidian notes are not accidentally saved while they're in an undesirable state. We also get the benefit of using git's diff feature to double check our notes before locking them in. For a comfortable diffing experience, use a graphical tool like [Sublime Merge](https://www.sublimemerge.com/).

The `./lock` command will run `git commit` with the [`--amend`](https://git-scm.com/docs/git-commit#Documentation/git-commit.txt---amend) flag, meaning all your notes will be squashed into one commit. Therefore this tool is meant purely as a backup and doesn't preserve version history.

For a more standard solution, see [Obsidian Git](https://github.com/denolehov/obsidian-git).
