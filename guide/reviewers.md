# Guide to reviewing MCW package updates

This guide walks you through the steps you must follow when reviewing updates to MCW packages. You will see references to both **stakeholders** and **reviewers**. A stakeholder is the primary person(s) responsible for coordinating MCW package updates, who creates a GitHub issue that starts the review process, and who ultimately merges the pull requests. Reviewers are typically subject matter experts (SMEs) who are asked to review MCW packages to provide feedback on what should be updated, and who review pull requests submitted by [contributors](contributors.md) who make the updates. The basic flow of an MCW package update is as follows:

- [Stakeholder creates GitHub issue](#create-a-new-issue-for-update)
- [Maintainer forks repository and completes changes](contributors.md#fork-the-mcw-repository)
- [Maintainer creates pull request (PR) and associates with issue](contributors.md#create-pull-request)
- [Reviewer(s) comment and provide feedback on PR](#review-pull-request)
  - Maintainer commits any additional changes based on feedback
- [Stakeholder merges PR and closes issue](#merge-pr-and-close-issue)

## Create a new issue for update

The first step of the process is for the **stakeholder** to create a new GitHub issue on the MCW repo that needs to be updated. This issue will be referenced by the pull request (PR) that the contributor submits when they are ready for a review of their submitted changes. This step is completed by the stakeholder, or the person responsible for scheduling and overseeing the update cycle for the MCW.

1. Browse to the top-level MCW repository and locate the link to the MCW repository for which you wish to initiate a test/fix or update: <https://github.com/Microsoft/MCW>.

2. With the selected MCW repository open, select the **Issues** tab and click **New issue** to create a new issue.

   - Enter a title indicating this is an update request. Example: `Update serverless architecture MCW`.
   - Write a description of the update request and instructions to the SMEs. Example: `This package is scheduled for a November update. Please review the contents of this repo and comment on this issue with suggested updates. All suggestions must be added to this issue by [DUE DATE].`.
   - Optionally assign one or more SMEs to review and offer suggestions.

## Review pull request

Per the [contributor instructions](contributors.md), the contributor will [create a pull request](contributors.md#create-pull-request) and associate it with the issue [you created](#create-a-new-issue-for-update). When this happens, you will see a comment added that references their pull request with the issue. You can click the pull request title in this comment to view it.

![Screenshot of issue with linked PR](media/issue-with-linked-pr.png 'Issue with linked PR')

Alternately, you may select the **Pull requests** tab in the repository to find and select the PR.

The pull request screen contains the following components:

1. A list of commits associated with the PR. These can be selected to view just the changes associated with a commit.
1. The outcome of checks GitHub made to ensure the pull request can be merged, along with a button to merge the pull request. **Only stakeholders will merge pull requests**.
1. A place to add comments to the PR. This is the ideal location to discuss issues and questions about the update.
1. Tabs that allow you to view the commits, checks, and changed files.

![Screenshot of the various components of a pull request](media/pull-request-components.png 'Pull request components')

The **stakeholder** may select one or more reviewers (SMEs) on this screen.

Consider using the following features to review changes associated with the PR:

1. Select the **Files changed** tab to view a list of files and the changes that were made to them.

   ![Screenshot of the files changed tab](media/files-changed-tab.png 'Files changed tab')

2. If you find an item in a file that you need to have the contributor change, select the **+** button that appears when you hover over the changed line. From here, type in your comments and click **Start a review**. This will notify the contributor that they have a review on their PR. They will have options to reply with a comment or request a review of their changes.

   ![Animated gif showing adding a new review item to a file](media/start-review.gif 'Start review')

3. After you are done writing the review, click **Finish your review**.

4. The **Review changes** button on top of the Files tab will show a badge with the number of reviews you added. Click on this button to submit your reviews when you are ready. Your options are to submit a comment without approval, submit feedback and approve, or request changes that must be addressed before merging. When you are done writing comments and selecting the appropriate review option, click **Submit review** to finalize.

   ![Submit review dialog with comments](media/submit-review-dialog.png 'Submit review dialog')

5. After submitting the review, it will appear on the **Conversation** tab of the pull review. This is where you can see all reviews and associated comments in one place.

   ![PR conversation tab with new review displayed](media/new-review-with-comments.png 'New review with comments')

6. Once the contributor has resolved the review, you will have the option to dismiss or complete the review.

7. Once feedback and any issues have been addressed, the **stakeholder** will merge the update to the repository by clicking on the **Merge pull request** button.

   ![Click Merge pull request to accept PR](media/merge-pull-request.png 'Merge pull request')

## Merge PR and close issue

The final steps are performed by the stakeholder who created the issue to initiate the maintenance cycle.

1. In GitHub, select the open pull request, and select **Merge pull request**.
2. Type a commit message.
3. Select **Confirm merge** to complete the pull request.
4. Navigate to the **Issues** tab in GitHub and select the Issue which initiated the current maintenance cycle.
5. Enter any comments, then select **Close issue**.

   - If the contributor associated the issue with the pull request, the issue should have automatically closed when you merged the PR.
