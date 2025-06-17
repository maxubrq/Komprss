# Komprss

**Komprss** is a fast, safe, and flexible archive compression engine written in Rust. It's the compression counterpart to [Xtrakt](https://github.com/your-org/xtrakt), built for efficient file packaging into formats like `.zip`, `.tar.gz`, and `.7z`.

## 🚀 Features

- 📦 Compress to `.zip`, `.tar.gz`, `.7z`, and more
- 🧱 Recursive folder compression
- 🔐 Password-protected ZIP/7z support (where supported)
- ⚡ Optimized for speed and minimal memory usage
- 🧰 CLI & Library API
- 📂 Cross-platform support (Linux, macOS, Windows)

---

## 🛠️ CLI Usage

```bash
komprss compress ./my_folder --format zip --output my_archive.zip
````

With password:

```bash
komprss compress ./secret --format 7z --password "hidden" --output secret.7z
```

---

## 🧑‍💻 Library Usage (Rust)

```rust
use komprss::Compressor;

fn main() {
    let compressor = Compressor::new();
    compressor
        .compress_dir("my_folder", "archive.zip", "zip")
        .unwrap();
}
```

---

## 🗃️ Supported Formats

| Format    | Compression | Password Support |
| --------- | ----------- | ---------------- |
| `.zip`    | ✅           | ✅ (basic)        |
| `.tar`    | ✅           | ❌                |
| `.tar.gz` | ✅           | ❌                |
| `.7z`     | ✅           | ✅                |

> Password support may require external binaries or native bindings (planned).

---

## 📦 Project Structure

```
komprss/
├── src/
│   ├── compressor.rs     # Core compression logic
│   ├── formats/          # Format-specific compressors
│   ├── cli.rs            # CLI interface
│   └── lib.rs
├── examples/
└── Cargo.toml
```

---

## 🧪 Running Tests

```bash
cargo test
```

---

## 🤝 Contributing

We welcome contributions! Check [CONTRIBUTING.md](CONTRIBUTING.md).

---

## 📄 License

MIT License — see [LICENSE](LICENSE).

---

Built to complement [Xtrakt](https://github.com/your-org/xtrakt) — the archive extraction engine.
