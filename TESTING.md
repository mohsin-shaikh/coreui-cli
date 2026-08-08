# Testing

This project has **no automated test suite** — no Jest/Vitest/etc., no `test` script, and no `*.test.ts` / `*.spec.ts` files.

Verification today is typecheck + format + build, plus running the CLI against a real project.

## Checks that exist

```bash
pnpm install
pnpm typecheck      # tsc --noEmit
pnpm format:check  # Prettier
pnpm build         # tsup → dist/
```

## Manual CLI smoke test

1. Build the CLI:

   ```bash
   pnpm build
   ```

2. In a sample app that already has a CSS file and a `tailwind.config` file, run:

   ```bash
   # from this repo
   node ./dist/index.js tailwind

   # or link globally, then run from the target project
   pnpm link --global
   coreui-cli tailwind
   ```

3. Confirm it:

   - Detects TypeScript when present
   - Installs Tailwind packages
   - Prompts for colors, format, and prefix
   - Writes CSS-first `@theme` config
   - Leaves the sample app in a working state
