# txt-sectumsempra

A minimalistic file chunking utility that splits large text files into smaller chunks of equal size.

## Goal

Split a large text file into smaller chunks of equal size (N MB each).

## Product Requirements Document (PRD)

1. **Input**: Accept any text file regardless of size.
2. **Output**: Generate files of equal size of N MB each.
3. **CLI Interface**: `cargo run absolute-path-input.txt size-in-MB` & output files will be placed in a new folder `input-start-timestamp` with names `input-part-0` to `input-part-N`.
4. **Validation**: Verify output files match input checksum.

## Installation

```bash
# Clone the repository
git clone https://github.com/yourusername/txt-sectumsempra.git
cd txt-sectumsempra

# Build the project
cargo build --release
```

## Usage

```bash
# Basic usage
cargo run -- <absolute-path-input.txt> --size <size-in-MB>

# Example
cargo run -- /home/amuldotexe/Downloads/threads_amuldotexe_1731404941.txt --size 1
```

The output files will be placed in a new folder named `input-start-timestamp` with names ranging from `input-part-0` to `input-part-N`.

### Features

- **Universal Input**: Accepts any text file regardless of size
- **Equal-sized Chunks**: Generates output files of exactly N MB each
- **Data Integrity**: Validates output files against input checksum

### Project Structure

```
txt-sectumsempra/
├── src/           # Source code
├── tests/         # Test files
├── txt-ref/       # Reference files
└── Cargo.toml     # Project dependencies
```

### Dependencies

- `sha2`: For checksum calculation
- `clap`: Command-line argument parsing

## Development

To run tests:
```bash
cargo test
```

## License

This project is open source and available under the MIT License.
