# hypeup

## Design constraints

- Avoiding needing to `import` any of the DSL primitives. This includes HTML elements, CSS properties, basics like `on`, `each`, and `reactive` - things that will be used in markup.

## Code generation

The `packages/lexicon` package contains generated files (`css.gen.ts`, `html.gen.ts`, `primitives.gen.ts`). To regenerate them, run `bun run generate` **in `packages/lexicon`** — not in `packages/generate` directly. The generate script writes output relative to the lexicon package's working directory.

## Backwards Compatibility

This is a fresh framework with limited consumption. It is acceptable when necessary to break APIs without re-exporting or aliasing symbols.
