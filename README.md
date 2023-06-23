# Hotfix Workflow

## Process

1. Find the current `PROD` commit in `main`
   1. TODO: Determine the best steps via git cli / github ui?
2. Branch from that commit into `hotfix/description-of-the-fix`
3. Apply code fix
4. Test locally (why wouldn't you do this anyways!?!)
5. Commit locally
6. Push to GitHub remote branch
7. Go to `GitHub > REPO > Actions`
8. Select `Hotfix` workflow
9. Manually dispatch (`Run workflow`) and select your `hotfix/description-of-fix` branch
10. Wait for deployment to complete... don't go anywhere!
11. Test and verify the fix in `PREPROD`
12. Go to `GitHub > REPO > Actions > Hotfix > [YOUR RUN]`
13. Approve deployment to `PROD`
14. Test and verify the fix in `PROD`

> At this point, the hotfix will be deployed to PROD and a PR has been set up to merge the hotfix code back to `main`

15. Go to GitHub > Pull Requests
16. Review yourself, get others to review, ensure all checks are green, go have a coffee
