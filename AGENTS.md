# Repository Guidelines

## Project Structure & Module Organization
This repository is currently minimal, so keep the layout predictable as the project grows. Place application code in `src/`, tests in `tests/`, and static assets in `assets/` or `public/` depending on runtime needs. Store project-level configuration at the root, for example `package.json`, `tsconfig.json`, or `.env.example`.[cite: 1]

Keep modules focused and colocate related files when useful. Example:[cite: 1]

```text
src/
  features/
  lib/
tests/
assets/
```[cite: 1]

## Build, Test, and Development Commands
No build system is committed yet. When adding one, expose the common workflows through consistent root commands so contributors have one entrypoint.[cite: 1]

* `npm install`: Install project dependencies once `package.json` exists.[cite: 1]
* `npm run dev`: Start the local development server.[cite: 1]
* `npm test`: Run the full automated test suite.[cite: 1]
* `npm run lint`: Check formatting and static analysis issues.[cite: 1]

If the project uses a different toolchain later, keep equivalent commands available and document any deviations in `README.md`.[cite: 1]

## Coding Style & Naming Conventions
Use 2-space indentation for JavaScript, TypeScript, JSON, and Markdown unless the adopted formatter enforces otherwise[cite: 2]. Prefer clear, descriptive names: `user-profile.ts`, `LinkCard.tsx`, `buildURL()`.[cite: 2]

* Use `camelCase` for variables and functions.[cite: 2]
* Use `PascalCase` for classes and component files.[cite: 2]
* Use `kebab-case` for non-component file names.[cite: 2]

Adopt automated formatting early, ideally with Prettier and ESLint, and run them before opening a pull request.[cite: 2]

## Testing Guidelines
Add tests alongside the first production code added to the repository[cite: 2]. Name test files after the unit under test, such as `link-parser.test.ts` or `LinkCard.test.tsx`[cite: 2]. Prefer fast, deterministic tests and avoid hidden network dependencies.[cite: 2]

Run all tests locally before submitting changes[cite: 2]. If coverage tooling is added, keep new code covered by meaningful unit tests.[cite: 2]

## Commit & Pull Request Guidelines
There is no existing git history in this checkout, so use a single, consistent commit style: imperative, concise subjects such as `Add URL validation utility` or `Create API client tests`.[cite: 2]

Pull requests should include:[cite: 2]
* A short description of the change[cite: 2]
* Test notes describing what was run[cite: 2]
* Screenshots or recordings for UI changes[cite: 2]
* Linked issues or task references when applicable[cite: 2]

## Configuration & Security
Do not commit secrets[cite: 2]. Keep local values in untracked environment files and commit only sanitized examples such as `.env.example`.[cite: 2]