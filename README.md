# Rust CI basic steps

- cache `.cargo` and `target` with `actions/cache`
- install nightly toolchain and do `fmt` with `dtolnay/rust-toolchain`
- install `rust-toolchain.toml` toolchain and `clippy` with `dtolnay/rust-toolchain`
- check that `Cargo.lock` is updated
- verify `fmt`

helpful action (before checkout):
```yaml
- name: Maximize build space
  uses: easimon/maximize-build-space@v10
  with:
    root-reserve-mb: 4096
    remove-dotnet: 'true'
    remove-android: 'true'
    remove-haskell: 'true'
    remove-codeql: 'true'
```
