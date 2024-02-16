# template-rust-lib
Base template for a Rust library crate with CI, config files, and branch protection

## Usage
- Generate a new repo via the green "Use this template" button
- Run the following to remove template language:
```
# Replace all occurrences with the desired library name
$ grep -ir template . --exclude-dir .git --exclude deny.toml
# Replace all occurrences as needed
$ grep -r "EDIT AS NEEDED" .
# Then rewrite this `README`
```
- Create a branch protection rule for `main` and enable the following as needed:
  - Require a pull request before merging
    - Require 1 approval
    - Dismiss stale pull request approvals when new commits are pushed
    - Require approval of the most recent reviewable push
  - Require status checks to pass before merging (optional, after CI has been triggered)
    - E.g. `linux-test`, `msrv`, and `lints`
  - Require a merge queue using `squash and merge` (optional, only allowed if repo is public)
  - Allow force pushes if needed to bypass above restrictions when necessary
- Enable full write access for Lurk Lab members by adding the `lurk-dev` team in `Settings->Collaborators and teams`
- Edit licenses and `deny.toml` as needed

## License

MIT or Apache 2.0
