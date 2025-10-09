# Templates

Generated applications share many common structures. To avoid re‑synthesizing the same code repeatedly, we extract reusable fragments into templates.

## How Templates Work

1. After a successful generation, the `templateService` analyzes the resulting file tree and identifies recurring patterns (e.g., authentication flow, CRUD operations, form components).
2. It extracts minimal, parameterized fragments and stores them in the `packages/templates` directory under a unique slug.
3. Each template includes:
   * A `manifest.json` containing metadata (name, tags, dependencies, fit criteria, examples).
   * A `files/` folder with the code fragments.
   * A `quality_score.json` recording test and build results from previous uses.
4. When generating a new app, the engine consults the registry to pick the best matching templates and composes them before falling back to fresh code generation.

## Contributing a Template

If you identify a useful pattern that isn’t yet templatized:

* Create a new subfolder under `packages/templates/your-template-name`.
* Add a `manifest.json` describing the template.
* Include parametric fragments in the `files/` directory.
* Document example usage.
