# actions
Collection of reusable actions

### `sarisia/actions/conclusion@main`

```yaml
permissions:
  actions: read
  
steps:
  - uses: sarisia/actions/conclusion@main
    id: conclusion
  - run: echo result is ${{ steps.conclusion.outputs.conclusion }} # `success` or `failure`
```
