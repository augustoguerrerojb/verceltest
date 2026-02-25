# AGENTS.md

## Cursor Cloud specific instructions

This is a **Next.js 15 front-end dashboard** ("M.O.N.K.Y OS") with no backend, database, or external service dependencies. All data is mock/hardcoded.

### Running the app

- `pnpm dev` starts the dev server on `http://localhost:3000`
- `pnpm build` creates a production build
- `pnpm lint` runs ESLint (`next lint`)
- `pnpm start` serves the production build

### Gotchas

- **ESLint compatibility:** `eslint-config-next` must match the Next.js version (15.2.4). ESLint v9 is required; v10 causes circular structure errors with this config.
- **pnpm build scripts:** `@tailwindcss/oxide`, `sharp`, and `unrs-resolver` require build script approval. This is handled via `pnpm.onlyBuiltDependencies` in `package.json`.
- **No automated test suite:** The project has no test framework or test files. Validation is done via lint and build.
- The `vaul` package has unmet peer dependency warnings for React 19 — these are safe to ignore and do not affect functionality.
