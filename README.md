### `Hello World Solana Program`

Start a new rust library project using

```bash
cargo init hello_world --lib

cd hello_world
```

Update `Cargo.toml` file with required rust library configurations

```
[lib]
name = "hello_world"
crate-type = ["cdylib", "lib"]
```

Install the `solana_program` package using

```
cargo add solana_program
```

Build the Solana Rust Program using

```bash
cargo build-bpf
```

Once built successfully without any error `.so` of the program will be added to the `/target/deploy` folder. You can deploy this to solana cluster using.

```
solana program deploy ./target/deploy/hello_world.so
```

Once successfully deployed it will return the programId of the Solana Program.