---
title: Branching Strategy
---
We follow the [Gitflow](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow) branch strategy. 

This means:

1. **Branch from `master`** for new branches

2. **Branch name format** should be 
    
    `[ISSUE-TYPE]/[ISSUE-KEY]-short-descriptive-name`

    For example, for a Story with key WEB-123, which modifies the color of buttons, the branch name would be

    `story/WEB-123-change-button-color`

3. **Pull request title** should be 

    `[ISSUE-TYPE]/[ISSUE-KEY]: Short descriptive name`
    
    For example, for a Story with key WEB-123, which modifies the color of buttons, the pull request name would be
    
    `story/WEB-123: Change button color`

4. **Commit message format** should be

     `[ISSUE-KEY]: Short description of changes`

   For example, for a Story with key WEB-123, which modifies the color of buttons, the commit message should read

     `WEB-123: Change color of buttons to pink`

5. **Version numbering** should follow [Semantic Versioning 2.0.0](http://semver.org/)