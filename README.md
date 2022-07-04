# pre-commit-julia-format

[pre-commit](https://pre-commit.com/) hooks for running [JuliaFormatter.jl](https://github.com/domluna/JuliaFormatter.jl)

## Hook Prerequisites

* requires `JuliaFormatter.jl` installed in your current julia package environment.
  i.e.,

  ```bash
  cd DIR_OF_YOUR_REPO/
  julia       # start julia REPL
  ]           # enter Pkg mode
  activate .  # activate the environment of the current dir
  status      # there should be a JuliaFormatter installed
  ```

## Hook Installation

To use hooks, add the following code block to your `.pre-commit-config.yaml`:

```yaml
- repo: https://github.com/qiaojunfeng/pre-commit-julia-format
  rev: 0.1.0                 # use the most recent version
  hooks:
  - id: julia-format         # formatter for Julia code
```

## Hook Configuration

### Style

You can use the [.JuliaFormatter.toml](https://domluna.github.io/JuliaFormatter.jl/dev/config/) to specify the style.

## References

* pre-commit: [https://pre-commit.com/](https://pre-commit.com/)
* pre-commit supported hooks: [https://pre-commit.com/hooks.html](https://pre-commit.com/hooks.html)
* JuliaFormatter.jl: [https://github.com/domluna/JuliaFormatter.jl](https://github.com/domluna/JuliaFormatter.jl)
* Julia Blue Style: [https://github.com/invenia/BlueStyle](https://github.com/invenia/BlueStyle)
* julia-format: [https://github.com/julia-actions/julia-format](https://github.com/julia-actions/julia-format)
