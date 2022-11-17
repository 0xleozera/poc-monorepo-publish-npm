<p align="center">
  <h1 align="center">
    POC MonoRepo Publish NPM
  </h1>
</p>

POC publish multiple applications with monorepo into NPM

## Installation

Use the package manager to install project deps.

```bash
yarn && yarn bootstrap
# or
npm install && npm run bootrstrap
```

## Commands

Create a release file indicating Semantic Versioning for this release

```bash
yarn changeset
```

Update versions of all packages and create/update the CHANGELOG file

```bash
yarn version
```

Publish all packages

```bash
yarn publish
```

## Release

1. Create the branch and develop the new feature
2. After the feature is developed, run the `changeset` command to create the release file
3. Create the PR of the branch feature and create a `release` branch. Indicate the PR for the release branch
4. After merging the PR, the CI will run, in this first moment the CI will create a new PR containing the versions changes
5. After merging the PR created per CI into the `release` branch, the CI will run again and will publish the new versions of the packages
