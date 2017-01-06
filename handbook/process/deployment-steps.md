---
title: Deployment Steps
---
1. In your particular project, create a new release following the standard: YYYY-MM-DD.X where X is the incremental release count for the day. Make sure to add the start date and a description.
2. Go to each of the issues that you intend to release and set the fixed in version to the currently unreleased version you created.
3. Review the JIRA release version to ensure that all Pull Requests are approved and all issues are marked as `Done`.
4. Ensure all post-deployment and pre-deployment steps are outlined if necessary.
5. Run all pre-deployment steps.
6. Deploy the new version. Deploy the build by hitting run on the Teamcity production job after ensuring all the related code was merged in.
7. Run all post-deployment steps.
8. Mark the JIRA version as `Released` and set the correct release date.
9. Tag the commit for the release in master with the release version number, making sure to push the tag to origin.
10. Send out release notes to Product and Engineering. If the deployment contained a big or well known feature, send it to All.