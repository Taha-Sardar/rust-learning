# Learning Rust: Packages and Crates

## Packages and Crates

In Rust, a package is a bundle of one or more crates. A crate is a compilation unit in Rust, which can be a binary or a library. The `Cargo.toml` file defines the package and its dependencies.

### Types of Crates

1. **Binary Crate**: Generates an executable.
2. **Library Crate**: Provides functionality intended to be used by other programs.

## Initializing a Project with Cargo

Cargo is Rust's package manager and build system. To create a new project, you can use the following commands:

### Creating a New Binary Project

```sh
cargo new my_project
```

This command creates a new directory named `my_project` with the following structure:

```
my_project
├── Cargo.toml
└── src
    └── main.rs
```

### Creating a New Library Project

```sh
cargo new --lib my_library
```

This command creates a new directory named `my_library` with the following structure:

```
my_library
├── Cargo.toml
└── src
    └── lib.rs
```

### Building and Running the Project

To build the project, navigate to the project directory and run:

```sh
cargo build
```

To run the binary project, use:

```sh
cargo run
```

To run tests, use:

```sh
cargo test
```

Cargo also provides a command called cargo check. This command quickly checks your code to make sure it compiles but doesn’t produce an executable:

```sh
cargo check
```

When your project is finally ready for release, you can use:
 
```sh
cargo build --release 
```

to compile it with optimizations. This command will create an executable in target/release instead of target/debug.


### Adding Dependencies

To add dependencies, edit the `Cargo.toml` file and add the dependency under `[dependencies]`. For example:

```toml
[dependencies]
serde = "1.0"
```

Then, run `cargo build` to download and compile the dependencies.
