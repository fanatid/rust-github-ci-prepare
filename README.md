# Rust CI basic steps

- maximize build space with `easimon/maximize-build-space`
- cache `.cargo` and `target` with `actions/cache`
- install nightly toolchain and do `fmt` with `dtolnay/rust-toolchain`
- install `rust-toolchain.toml` toolchain and `clippy` with `dtolnay/rust-toolchain`
- check that `Cargo.lock` is updated
- verify `fmt`
