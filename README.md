# Clojure hooks for pre-commit

[Clojure](https://clojure.org/) package for [pre-commit](https://pre-commit.com) hooks.

## Usage with pre-commit

```yaml
-   repo: https://github.com/vincentjames501/pre-commit-clojure
    rev: main
    hooks:
    -   id: clj-kondo
```

## Passing arguments to clj-kondo

```yaml
-   repo: https://github.com/vincentjames501/pre-commit-clojure
    rev: main
    hooks:
    -   id: clj-kondo
        args: ['--fail-level']
```