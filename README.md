# template-rust-lib
Base template for a Rust library crate with CI, config files, and branch protection

## Notes
- The generated repo will have a protected `main` branch with the following required status checks:
  - `linux-tests`
  - `code-quality/msrv`
  - `code-quality/lints`
  - `code-quality/wasm-build`
- If the generated repo is public, it will enforce a merge queue using `squash and merge` by default
- Run the following after generating the new repo:
```
# Replace all occurrences with the desired library name
$ grep -ir template . --exclude-dir .git --exclude deny.toml
# Replace all occurrences as needed
$ grep -r "EDIT AS NEEDED" .
```

## License

MIT or Apache 2.0
