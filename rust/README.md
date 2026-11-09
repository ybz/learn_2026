 ## Links

["Rust programming language" Book](https://doc.rust-lang.org/book/)

 ## Planned order

- Go through the book
- Go through 'Rust by example'
- Do the Rultlings course

 ## Tools

| Tool | What is it |
| --- | --- | 
| `rustc` | The rust compiler |
| `rustup` | The rust tool chain |

 ### Commands

All `cargo` commands run from the `rust/` directory (the workspace root).

| Command | What it does |
| --- | --- |
| `cargo new projects/<name>` | Create a new project; the workspace picks it up automatically |
| `cargo run -p <name>` | Build and run one project |
| `cargo build` | Build every project in the workspace |
| `cargo check` | Type-check without producing a binary (fast) |
| `cargo test -p <name>` | Run one project's tests |
| `cargo clippy` | Lint for common mistakes |
| `cargo fmt` | Format all code |

 ## Layout

```
rust/
  Cargo.toml            # workspace root, members = projects/*
  projects/
    hello_world/
      Cargo.toml        # one package per project
      src/main.rs
```

rust-analyzer in VS Code is pointed at `rust/Cargo.toml` via `.vscode/settings.json`
(`rust-analyzer.linkedProjects`), so it works even though the repo root has no `Cargo.toml`.
