# WorkflowTest
### an example using Github Actions Workflows to build Crestron 4-series / VC-4 CPZ releases
### Chris Poole chris@avsp.co.uk

Build Github Workflow / Actions Test

Two example Github actions workflows are included in this project.

Firstly, `.github/workflows/build-on-push.yml` runs a build whenever any push occurs.

To trigger this workflow, simply push to the github repo.

Secondly, `.github/workflows/release.yml` runs a build and uploads it as a release, whenever a new tag is pushed that beging "v".

`release.yml` includes a Powershell script to modify the VersionInfo.cs in the project to include the version tag in the C# code.

To trigger the workflow, commit all changes to master, then add a new tag and push it.

For example:

```
# add all non-excluded files
git add .

# commit the changes
git commit -m "write the changelog here"

# add a release tag
git tag v1.0.0

# push the commit and the tag to the origin (github)
git push origin --tags
```

The output and logs for these actions are available in the "Action" tab of the Github repo.
