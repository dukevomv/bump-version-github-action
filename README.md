# bump-version-github-action
Automates the creation of a new version upon PR merge with commit and tag directly on the repository.

This Action will only run when a PR is **merged** on `main` branch.

The purpose is to change the version in `composer.json` to the next available and tag the last commit on the repository in order for composer to be able to find the version.

## Bugfix Version - Default
This action will find the version in `composer.json` and bump the Bugfix digit.

e.g If branch `test` is merged with version in `composer.json` set to `1.2.3` after this Action execution the branch will have changed version in `composer.json` to `1.2.4` along with the same tag.


## Minor Version - Feature
When the merged branch starts with `feature` this action will find the version in `composer.json` and bump the Minor digit while reseting the Bugfix to `0`.

e.g If branch `feature/test` is merged with version in `composer.json` set to `1.2.3` after this Action execution the branch will have changed version in `composer.json` to `1.3.0` along with the same tag.
