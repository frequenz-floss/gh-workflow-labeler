# Labeler GitHub workflow

This GitHub workflow is just a thin wrapper over the [labeler](https://github.com/marketplace/actions/labeler) action that takes care of:

* Making sure the action is called securely.
* And with the options that make more sense for our projects.

By having this thin wrapper we can also ensure that we can easily *propagate* updates to the action in a more controlled way.

## Usage

```yaml
name: Pull Request Labeler

on: [pull_request_target]

jobs:
  labeler:
    uses: frequenz-floss/gh-workflow-labeler/.github/workflows/labeler.yaml@v0.x.x
    secrets: inherit
```
