## Reusable actions

A collection of reusable github actions

To use in another repo set it up like this

```yml
...action
      - name: PNPM setup
        uses: GustavEikaas/pnpm-setup/.github/actions/pnpm-setup@main
...action
```
