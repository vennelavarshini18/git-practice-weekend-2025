# Rebasing Commits in Git

 

In software development, managing commits is essential for maintaining a clean and coherent project history. Git offers various tools to manage commits, including rebasing, which allows you to reapply commits on top of another branch's history. Let's explore how to rebase commits effectively.

## Setup

- Create a branch called `feature-branch`.
- Make several commits in the `feature-branch` to simulate a feature development process.
- Switch to the master branch
- Make some commits into the `master` branch

## Rebasing

Now, let's assume that while you were working on your feature, changes were made to the `master` branch. To incorporate these changes into your feature branch, you can rebase your commits onto the latest `master` branch.

1. Switch to the `feature-branch` by running `git checkout feature-branch`.
2. Run `git rebase master` to rebase your commits onto the latest `master` branch.

<img src="https://lh3.googleusercontent.com/u/0/drive-viewer/AKGpihapdOC_T7VatzaamItAARUawhQt60tD4D5wXZOjA8PHJuxcNALSs6hTjbSZRo0CH0YBiyyfNZYVty5JZFourh2SHtvriw=w3200-h1730" alt="rebase" width="500px" height="auto">
During the rebase process, Git will pause if there are any conflicts that need manual resolution. Resolve conflicts as prompted by Git.

After resolving conflicts, continue the rebase process by running `git rebase --continue`.

Once the rebase is complete, your commits will be applied on top of the latest `main` branch.

## Next Steps

After rebasing and squashing commits, you can push your changes to the remote repository and create a pull request for review.
