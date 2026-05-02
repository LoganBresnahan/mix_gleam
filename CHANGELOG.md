# Changelog

## v0.7.0 - 2026-05-02 (LoganBresnahan fork)

- Replaced deprecated `Tuple.append/2` with explicit tuple construction in
  `mix gleam.deps.get`. Removes the deprecation warning emitted under
  Elixir 1.15+ and prepares the task for Elixir 1.19+ where the call would
  otherwise become an error.
- Bumped the default `mix gleam.new --retro` template to `gleam_stdlib ~> 1.0`
  and `gleeunit ~> 1.10`. New scaffolds now target Gleam 1.x out of the box
  rather than the pre-1.0 line.
- Bumped the project's own `:elixir` requirement from `~> 1.9` to `~> 1.15`,
  matching the stated minimum in the README.
- Released the long-running `0.7.0-dev` version as `0.7.0`.

This release ships from a community fork while upstream
`gleam-lang/mix_gleam` is in maintenance mode. Behavior is otherwise
identical to upstream `0.7.0-dev` (which was 6 cosmetic commits ahead of
upstream `0.6.2`).

## v0.6.2 - 2023-11-16

- Updated for Elixir v1.15 and Gleam v0.32 compatibility. Make sure to set
  `prune_code_paths: false` in your `mix.exs` project config.

## v0.6.1 - 2022-12-04

- Updated for Gleam v0.25 compatibility.
- Fixed a bug where compiling on Windows would fail for projects with a `priv`
  directory.

## v0.6.0 - 2022-06-16

- `mix gleam.compile` task is renamed to `mix compile.gleam` for compatibility
  with the `:compilers` Mix.Project option.
- `MixGleam.add_aliases` is deprecated in favor of adding `:gleam` to
  `:compilers` and specifying an alias for `:"deps.get"`.

## v0.5.0 - 2022-06-08

- Gleam code is now compiled from Mix's `_build` directory. The presence of
  `gleam.toml` in a project's base directory is no longer required.

## v0.4.0 - 2022-01-10

- Updated to work with the `gleam compile-package` v0.19 API.

## v0.3.0 - 2021-12-26

- Updated to work with the `gleam compile-package` API for incremental builds
  and support for packages published with the Gleam build tool.
