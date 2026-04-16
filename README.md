# Magika

> Fork of [google/magika](https://github.com/google/magika) — AI-powered file type detection.

Magika uses a deep learning model to detect file content types with high accuracy, even when file extensions are missing or misleading.

## Features

- **Fast & accurate**: Powered by a lightweight deep learning model
- **Wide format support**: Detects 100+ file types
- **CLI & Python API**: Use from the command line or integrate into your Python projects
- **Rust bindings**: High-performance Rust implementation available

## Installation

```bash
pip install magika
```

Or install from source:

```bash
git clone https://github.com/your-org/magika.git
cd magika
pip install -e .
```

## Quick Start

### CLI

```bash
magika suspicious_file.bin
magika --recursive ./directory
```

### Python API

```python
from magika import Magika

m = Magika()
result = m.identify_path("suspicious_file.bin")
print(result.output.ct_label)  # e.g. "pdf"
print(result.output.score)     # confidence score
```

## Supported File Types

Magika supports detection of 100+ content types including:
- Documents: PDF, Word, Excel, PowerPoint
- Code: Python, JavaScript, TypeScript, Rust, Go, and more
- Archives: ZIP, TAR, GZIP, 7Z
- Media: JPEG, PNG, MP3, MP4
- And many more...

Run `magika --list-output-content-types` to see the full list.

## Development

### Prerequisites

- Python 3.8+
- Rust (for Rust bindings)

### Setup

```bash
pip install -e ".[dev]"
```

### Running Tests

```bash
pytest tests/
```

## Contributing

Contributions are welcome! Please open an issue or pull request.

See [CODEOWNERS](.github/CODEOWNERS) for maintainer information.

## License

Apache 2.0 — see [LICENSE](LICENSE) for details.

This project is a fork of [google/magika](https://github.com/google/magika), originally developed by Google.
