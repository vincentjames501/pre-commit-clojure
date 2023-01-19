# Clojure hooks for pre-commit

[Clojure](https://clojure.org/) package for [pre-commit](https://pre-commit.com) hooks. Integrates with popular packages such as [clj-kondo (static linter)](https://github.com/clj-kondo/clj-kondo), [kaocha (unit testint)](https://github.com/lambdaisland/kaocha), and [zprint (file formatting)](https://github.com/kkinnear/zprint).

## Usage with pre-commit

```yaml
-   repo: https://github.com/vincentjames501/pre-commit-clojure
    rev: v1.x
    hooks:
    -   id: clj-kondo
    -   id: zprint
    -   it: kaocha
    
```

## Passing arguments to clj-kondo

```yaml
-   repo: https://github.com/vincentjames501/pre-commit-clojure
    rev: v1.x
    hooks:

    -   id: clj-kondo
        args: ['error']
    -   id: zprint
    -   id: kaocha
        # Must install pre-push: $ pre-commit install --hook-type pre-push
        # https://pre-commit.com/#pre-commit-during-push
        stages: [merge-commit, push, manual]  
        always_run: true
```
