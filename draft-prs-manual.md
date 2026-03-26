# Draft Pull Requests Manual

## Introduction

Draft Pull Requests (PRs) in GitHub are a feature that allows you to create a pull request that is not yet ready for review. This is useful for sharing work-in-progress code, getting early feedback, or preparing a PR before it's fully polished. Draft PRs are clearly marked as drafts and cannot be merged until they are marked as ready for review.

## Key Features of Draft PRs

- **Visibility**: Draft PRs are visible to collaborators but are clearly labeled as drafts.
- **No Merging**: You cannot merge a draft PR until it is converted to a regular PR.
- **Feedback**: You can still receive comments and suggestions on draft PRs.
- **Conversion**: You can easily convert a draft PR to a ready-for-review PR when it's complete.

## How to Create a Draft PR

1. **Navigate to Your Repository**: Go to the GitHub repository where you want to create the PR.

2. **Start a New Pull Request**:
   - Click on the "Pull requests" tab.
   - Click the "New pull request" button.

3. **Select Branches**:
   - Choose the base branch (e.g., `main`) and the compare branch (your feature branch).

4. **Create as Draft**:
   - Scroll down to the PR creation form.
   - Check the box that says "Create a draft pull request" (this option appears when creating a new PR).

5. **Fill in Details**:
   - Add a title and description for your PR.
   - Optionally, add labels, assignees, or reviewers.

6. **Submit**: Click "Create draft pull request".

## Converting a Draft PR to Ready for Review

Once your PR is ready:

1. Go to your draft PR.
2. Click the "Ready for review" button (usually located near the merge button).
3. Confirm the conversion.

Your PR will now be a standard pull request and can be reviewed and merged.

## Best Practices

- **Use Drafts for WIP**: Create drafts early to get feedback on direction.
- **Clear Descriptions**: Even in drafts, provide context about what the PR aims to achieve.
- **Iterate Based on Feedback**: Use comments on drafts to refine your code before marking as ready.
- **Avoid Force Pushes**: Be mindful of force pushes on branches with open draft PRs, as they can affect reviewers.
- **Branch Protection**: Ensure your repository's branch protection rules allow drafts if needed.

## Limitations

- Draft PRs cannot trigger certain CI/CD workflows that are set to run only on "opened" PRs (some may need to be configured for "opened" or "ready_for_review").
- Merging is blocked until the PR is marked as ready.

## Team Workflow for Iterative Comments on a Draft PR

When you create a Draft PR and your teammates comment with requested changes, follow this process:

1. Keep the Draft PR open while you process feedback.
2. Do additional work on the same branch (e.g., `feature/x`).
   - `git checkout feature/x`
   - apply changes
   - `git add .` and `git commit -m "address review feedback"`
   - `git push`
3. GitHub automatically updates the Draft PR with new commits.
4. Optionally update your PR description with progress and remaining scope.
5. Use comments to indicate status ("working on this", "ready for next review").

### What to do with the Draft PR while changing

- Leave it in Draft status
- Do not close the PR for each change
- Re-request review with comments or by mentioning reviewers

### After applying the changes

- Push the final update to the same branch
- Ensure CI passes and new feedback is addressed
- Click "Ready for review" when the work is complete

### Do you create another Draft PR?

- Usually no: use the same Draft PR until it's ready
- Only create a new PR if branch or scope changes completely

### Final merge phase

1. Convert Draft to a regular PR using "Ready for review".
2. Complete the review loop and resolve any last comments.
3. Merge when approved and passing checks.
4. Delete the branch if the team policy requires.

## Additional Resources

- [GitHub Documentation on Draft PRs](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/about-pull-requests#draft-pull-requests)
- [Creating a Pull Request](https://docs.github.com/en/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/creating-a-pull-request)

This manual provides a basic overview. For more advanced features, refer to GitHub's official documentation.