# pre-commit-julia-format

[pre-commit](https://pre-commit.com/) hooks for running [JuliaFormatter.jl](https://github.com/domluna/JuliaFormatter.jl)

## Hook Prerequisites

* requires `JuliaFormatter.jl` installed in a julia environment, e.g., can be
  the global environment, or a dedicated julia
  environment only for `JuliaFormatter.jl`, or the environment for your own
  julia package.

  To check if `JuliaFormatter.jl` is installed, run

  ```bash
  cd DIR_OF_YOUR_JULIA_ENVIRONMENT/
  julia       # start julia REPL
  ]           # enter Pkg mode
  activate .  # activate the environment of the current dir
  status      # there should be a JuliaFormatter installed
  ```

## Hook Installation

To use the hook, add the following code block to your `.pre-commit-config.yaml`:

```yaml
- repo: https://github.com/qiaojunfeng/pre-commit-julia-format
  rev: v0.2.1                # use the most recent version
  hooks:
  - id: julia-format         # formatter for Julia code
```

## Hook Configuration

### Julia project path

By default the hook will use the default julia environment (under `~/.julia/environments/`)
to run `JuliaFormatter`, if you want to use a different one, add an `args` key in the yaml:

```yaml
  - id: julia-format
    args: [--project=/DIR_OF_YOUR_JULIA_ENVIRONMENT]
```

where `DIR_OF_YOUR_JULIA_ENVIRONMENT` is the path to your julia environment containing
`JuliaFormatter.jl`.

### Style

You can use the [.JuliaFormatter.toml](https://domluna.github.io/JuliaFormatter.jl/dev/config/) to specify the style.

### Example usage

You can check this repo for an example of how to use the hook: <https://github.com/qiaojunfeng/WannierIO.jl>

## References

* pre-commit: [https://pre-commit.com/](https://pre-commit.com/)
* pre-commit supported hooks: [https://pre-commit.com/hooks.html](https://pre-commit.com/hooks.html)
* JuliaFormatter.jl: [https://github.com/domluna/JuliaFormatter.jl](https://github.com/domluna/JuliaFormatter.jl)
* Julia Blue Style: [https://github.com/invenia/BlueStyle](https://github.com/invenia/BlueStyle)
* julia-format: [https://github.com/julia-actions/julia-format](https://github.com/julia-actions/julia-format)
