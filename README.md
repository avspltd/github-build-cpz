# github-build-cpz

> sample code for Github Actions Workflows to build Crestron 4-series / VC-4 CPZ releases

Two example Github Actions workflows are included in this project.

#### release.yml

Firstly, `.github/workflows/release.yml` runs a build and uploads it as a release, whenever a new tag is pushed that beging "v".

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

On the Github website in the Actions tab, any running or completed actions can be seen with their log files.

Further information is in the actions doc

#### build-on-push.yml
Secondly, `.github/workflows/build-on-push.yml` runs a build whenever any push occurs.
Generally this is less useful than the second and will cause a build to occur whenever code is pushed.

To trigger this workflow, simply push to the github repo.

The output and logs for both of these actions are available in the "Action" tab of the Github repo.

---
## Usage

To use these scripts in your own projects, create a .github/workflows folder in your project, copy one of the yml files to your project and customize the sln / cpz paths in the yml file.

---
## Contributing

Contributions are what make the open source community such an amazing place to be learn, inspire, and create. Any contributions you make are **greatly appreciated**.

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---
## License

Distributed under the MIT License. See `LICENSE` for more information.

---
## Contact

| <a href="https://www.avsp.co.uk/" target="_blank">**Chris Poole**</a> | <a href="https://www.avsp.co.uk/" target="_blank">**AVSP Ltd**</a> |
| :---: | :---: |
| [![](https://avatars1.githubusercontent.com/u/651218?s=180)](https://www.avsp.co.uk/) | [![](https://avatars0.githubusercontent.com/u/64958898?s=180)](https://www.avsp.co.uk/) |
| <a href="http://github.com/ninjaoxygen" target="_blank">`github.com/ninjaoxygen`</a> | <a href="http://github.com/avspltd" target="_blank">`github.com/avspltd`</a>
| [@ninjaoxygen](https://twitter.com/ninjaoxygen) |
| chris@avsp.co.uk | info@avsp.co.uk |


Project Link: [https://github.com/avspltd/github-build-cpz](https://github.com/avspltd/github-build-cpz)

