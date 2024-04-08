If you run `cargo deny check` you get this:

```bash
chris13524@peach cargo-deny-unreachable-code % cargo deny check
thread '<unnamed>' panicked at /Users/chris13524/.cargo/registry/src/index.crates.io-6f17d22bba15001f/krates-0.16.7/src/builder.rs:719:25:
internal error: entered unreachable code: unable to locate analytics for crate git+https://github.com/WalletConnect/utils-rs.git?tag=v0.8.0#wc@0.1.0 features([])
note: run with `RUST_BACKTRACE=1` environment variable to display a backtrace
```

But if you comment out the `wc` dependency then it checks fine:

```bash
chris13524@peach cargo-deny-unreachable-code % cargo deny check
advisories ok, bans ok, licenses ok, sources ok
```
