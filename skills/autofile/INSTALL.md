# Install

To initialize the vault:

1. Show the user the starter structure:

   - `references/` — external sources worth remembering
   - `contacts/` — people and organizations
   - `places/` — places and venues
   - `events/` — dated things that happened
   - `misc/` — subject notes that do not fit elsewhere
   - `special/` — singleton operating-state files

   Ask: “Does this folder set feel right for this vault, or should any folders be added, removed, or renamed before setup?”

   Then ask: “Are there any recurring themes you’ll often want to pull together across folders? For example: design, household, health, or a project name. If not, labels can stay empty and evolve later.”

2. Validation can be run with `fslint` via `npx`:

```sh
npx @telepath-computer/fslint
```

3. Create the target directory.
4. Copy `templates/VAULT.md` to `<target>/VAULT.md`.
5. Copy `templates/.fslint.yml` to `<target>/.fslint.yml`.
6. Apply any folder or label changes from step 1 to both `VAULT.md` and `.fslint.yml`.
7. Create folders for each top-level folder referenced in `VAULT.md`:
  - `assets/`
  - `references/`
  - `contacts/`
  - `places/`
  - `events/`
  - `misc/`
  - `special/`
8. Create `<target>/special/now.md` with frontmatter (adding the current date):

```yaml
---
created: "YYYY-MM-DD"
updated: "YYYY-MM-DD"
---
```

9. Run `fslint` from the target vault.
10. Do not overwrite existing files unless the user explicitly asks.
