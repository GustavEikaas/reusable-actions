## Reusable actions

A collection of reusable github actions

To use in another repo set it up like this

```yml
name: Publish changed
on:
  push:
    branches:
      - main
jobs:
  publish:
    environment: npm
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
        with:
          fetch-depth: 0
  
      ## This action
      - name: PNPM setup
        uses: GustavEikaas/reusable-actions/.github/actions/pnpm-setup@main

      - name: Build
        shell: bash
        run: pnpm build
```
