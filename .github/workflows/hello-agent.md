---
name: Hello Agent
on:
  workflow_dispatch:
---
---
name: Hello Agent # Human-readable workflow name shown in GitHub Actions
on: # Events that can start this workflow
  workflow_dispatch: # Lets you run the workflow manually while testing
permissions: # GitHub token access the agent needs
  contents: read # Read repository contents
  issues: write # Create or comment on issues
---
permissions:
  contents: read
  issues: write
## Task

Search the open issues in this repository.
Find the issue with the most 👍 reactions.
Post a comment on that issue saying:
"This issue has the most community support! We'll prioritise it in our next planning session."

If there are no open issues, create one titled "Community Voting Test" and post the same comment.