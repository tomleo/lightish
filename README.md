# lightish

## Releasing a new version

### 1. Update the package version

First run `npm run versioning`, you'll see output similar to

```
> lightish@0.0.1 versioning
> commit-and-tag-version

✔ bumping version in package.json from 0.0.1 to 0.0.2
✔ bumping version in package-lock.json from 0.0.1 to 0.0.2
✔ outputting changes to CHANGELOG.md
✔ committing package-lock.json and package.json and CHANGELOG.md
✔ tagging release v0.0.2
ℹ Run `git push --follow-tags origin main && npm publish` to publish
```

### 2. Push the tag & changelog to github

Run `git push --follow-tags origin main`

*Note* safe to skip the `npm publish` recommendation, as this will be packaged
and published to the vscode marketplace not npm.

### 3. Publish new package to vscode marketplace

First make sure you're logged in via `npm run login`

Next you'll run something `npm run publish -- 0.0.2` swapping out `0.0.2` with
the new version outputted from step 1

## Useful Resources

- https://code.visualstudio.com/api/references/theme-color
