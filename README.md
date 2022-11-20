# actions
Collection of reusable actions

### `sarisia/actions/conclusion@main`

```yaml
jobs:
  some-task:
    ...
  
  conclusion:
    needs: some-task
    if: always()
    runs-on: ubuntu-latest
    permissions:
      actions: read
    steps:
      - uses: sarisia/actions/conclusion@main
        id: conclusion
      - run: |
          echo result is ${{ steps.conclusion.outputs.conclusion }}
          echo jobs is ${{ steps.conclusion.outputs.jobs }}
```

### `sarisia/actions/update-devcontainer@master`

```yaml
jobs:
  update-devcontainer:
    runs-on: ubuntu-latest
    permissions:
      contents: read
      packages: write
    steps:
      - uses: sarisia/actions/update-devcontainer@main
```
