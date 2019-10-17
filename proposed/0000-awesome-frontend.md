# 0000 - Awesome frontend

## Status
[status]: #status

Proposed

## Summary
[summary]: #summary

The Karte von morgen [frontend](https://github.com/kartevonmorgen/kartevonmorgen)
shall be accessible from multiple clients (browser, mobile) and the code shall be maintainable.

## Context
[context]: #context

The current frontend is in a bad state.
The following issues need to be solved to change the situation:

- **Maintainability**
  Due to the untyped programming language JavaScript most types of code refactoring are risky to realize.
  This gets emphasized by external dependencies that easily can break the web application.
  Often a simple dependency update leads to multiple hours of fighting the dependency hell.
  Unfortunately a handful of bugs don't occur during the refactoring process but during the
  runtime (because JS can't check correctness at compile time).

- **Complexity**
  The current complexity of the codebase is grown due to a lot of dirty quick fixes.
  This not only makes it hard for the community to contribute to the project
  but it also makes it costly to introduce new features.

- **Tests**
  There are few tests but most of the code is untested.
  This makes it even harder to refactor and maintain the project.

- **File size**
  The packed JavaScript bundle size was 5.3 MB some time ago.
  In the meanwhile its shrunken to 1.5 MB but that's still a bunch of bytes that
  needs to be downloaded at once.

## Decision
[decision]: #decision

We will rewrite the whole frontent in [Rust](https://rust-lang.org).
The result will be a [WASM](https://en.wikipedia.org/wiki/WebAssembly) module.

## Consequences
[consequences]: #consequences

> This section describes the resulting context, after applying the decision. All consequences should be listed here, not just the "positive" ones. A particular decision may have positive, negative, and neutral consequences, but all of them affect the team and project in the future.

## References
[references]: #references

- http://thinkrelevance.com/blog/2011/11/15/documenting-architecture-decisions
