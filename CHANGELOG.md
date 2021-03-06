### Unreleased

### 0.4.6 - 2018-07-05

* Support VSCode workspaces
* Code lens for running unit tests

### 0.4.5 - 2018-06-03

* Undo the change to target directory default (unnecessary with Rust 1.26.1)

### 0.4.4 - 2018-05-17

* Update the VSCode client library dependency
* Fix the target directory

### 0.4.3 - 2018-05-14

* Set the target directory default to work around a but in the stable RLS
* `extern crate` snippet
* remove non-workspace mode

### 0.4.2 - 2018-04-29

* Added `rust-client.rlsPath` setting for easier RLS development and debugging
  (and deprecated the `rls.path` setting)
* Bug fixes for race conditions.
* Increased the default `rust.wait_to_build` time.
* Updated LS client
* Added `cargo bench` task
* Added `rust.target_dir` and `rust.all_targets` settings


### 0.4.0 - 2018-03-04

* Added `rust.racer_completion` to allow disabling racer to work around a
  [performance issue](https://github.com/rust-lang-nursery/rls/issues/688).
* Spinner UI improvements.
* Added a `cargo check` task.
* The local active toolchain channel is now the default `rust-client.channel`.
* Added `rust.jobs` to allow limiting the number of parallel Cargo jobs.
* Added support for workspaces.
* Improved startup experience when using workspaces.
* Deglob is now a code action instead of a command.
* Warns and no longer crashes RLS if a single file is opened instead of a
  folder.
* Warns if Cargo.toml is not in the root of a workspace.

### 0.3.2 - 2017-11-07

* Added `rust-client.rustupPath` to override rustup location.
* Added properties to control enabling of Cargo features.
* Fixed an issue where nightly was used instead of the configured channel.

### 0.3.1 - 2017-10-04

* Bug fix in RLS detection.

### 0.3.0 - 2017-09-29

* Change the default for `rust-client.rls-name` to `rls-preview` to handle the
  renaming of the RLS.
* Remove `rust-client.showStdErr` property.

### 0.2.3 - 2017-09-21

* Warns if Config.toml is missing (likely due to opening a Rust file outside a
  project, which previously crashed)
* Automatically continue line comments
* Automatically set LD_LIBRARY_PATH (only useful when not using Rustup)
* Configure the toolchain and component name for the RLS
* Command to restart the RLS
* Better workflow around creating build tasks
* A better logo - more colour!

### 0.2.2 - 2017-08-21

* Highlights errors from build tasks
* Find all impls
* Adds cargo clean task
* Auto-detect `--lib` or `--bin`
* Adds an opt-out option for creating tasks.json
* Add a command to update the RLS and an option to do so on startup
* Deprecate `RLS_PATH` and `RLS_ROOT` env vars
* Changes to the RLS:
  - Easier to use deglob refactoring
  - Debugging and troubleshooting [instructions](https://github.com/rust-lang-nursery/rls/blob/master/debugging.md)

### 0.2.1 - 2017-08-09

* Fix bug installing the rls

### 0.2.0 - 2017-08-07

* Unicode (fixed width) spinner
* Logging and debugging options in configuration
* Deglob command is in the Rust category
* Don't check tests by default (still configurable)
* Set `RUST_SRC_PATH` for Racer
* Travis CI for the repo
* Performance and robustness improvements in the RLS, support for required options
  here, including
  - blacklist large and non-very useful crates (configurable)
  - configure compiler data
  - don't error on missing options
  - stabilise renaming
  - don't crash on non-file URLs
  - Racer and Rustfmt updates
  - only use Racer for code completion (never for 'goto def', still configurable)
  - improve startup build/index time
  - handle stale compiler data better
  - add an option to only build/index on save (not on change)
  - rebuild if Cargo.toml changes

### 0.1.0 - 2017-07-17

* First release
