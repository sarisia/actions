# actions
Collection of reusable actions

# Deprecated

Use reusable workflows instead.

https://github.com/sarisia/workflows

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

### `sarisia/actions/tailscale-ssh@main`

```yaml
jobs:
  this-is-fucking-buggy-i-need-to-debug:
    runs-on: ubuntu-latest
    steps:
      - uses: sarisia/actions/tailscale-ssh@main
        with:
          client-id: ${{ secrets.TAILSCALE_CLIENT_ID }}
          client-secret: ${{ secrets.TAILSCALE_CLIENT_SECRET }}
          # optional
          version: '1.72.1'
          tags: 'tag:github-actions,tag:test'
          hostname: 'actions'
```
