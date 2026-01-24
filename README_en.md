# gg

A simple and easy-to-use `.gitignore` file management tool that supports quick generation of gitignore templates for various languages, as well as adding custom files/folders to the ignore list.

## Features

- 🚀 Quickly generate `.gitignore` templates for multiple languages
- 📁 Intelligently find `.gitignore` files (automatically searches upward)
- ➕ Easily add files/folders to the ignore list
- 🔍 Automatically detect duplicates to avoid repeated additions
- 📝 Support for both relative and absolute paths

## Supported Language Templates

- `python` - Python language
- `go` - Go language
- `react` - React projects
- `c++` - C++ projects
- `c` - C language
- `matlab` - MATLAB projects
- `rust` - Rust language

More templates can be supported. Currently too busy to add more: https://github.com/github/gitignore

## Installation

### Method 1: Download the latest release package (Recommended)

- https://github.com/panyingyun/gg/releases

### Method 2: Using go install (Recommended)

```bash
go install github.com/panyingyun/gg@latest
```

After installation, make sure `$GOPATH/bin` or `$HOME/go/bin` is in your `PATH` environment variable, then you can use the `gg` command directly.

### Method 3: Build from source

```bash
git clone https://github.com/panyingyun/gg.git
cd gg
make build
sudo cp gg /usr/local/bin
```

### Download from Release

Visit the [Releases](https://github.com/panyingyun/gg/releases) page to download the binary file for your platform.

## Usage

### Generate Language Templates

```bash
# Generate Python template
gg python

# Generate Go template
gg go

# Generate React template
gg react

# Generate C++ template
gg c++

# Generate C template
gg c

# Generate MATLAB template
gg matlab

# Generate Rust template
gg rust
```

### Add Files/Folders to .gitignore

```bash
# Add a file
gg -f filename.txt

# Add a folder
gg -f directory/

# Use relative or absolute paths
gg -f ./path/to/file
gg -f /absolute/path/to/file
```

## How It Works

1. **Find .gitignore file**: The tool starts from the current directory and searches upward for a `.gitignore` file
2. **Create or update**: If a `.gitignore` file is found, content is appended; if not found, a new file is created in the current directory
3. **Smart path handling**: When adding files/folders, relative paths are automatically calculated to ensure correct paths

## Examples

```bash
# Generate .gitignore in a Go project
$ gg go
Successfully generated .gitignore file for go template
File location: /path/to/project/.gitignore

# Add build directory to ignore list
$ gg -f build/
Successfully added path to .gitignore: build/
File location: /path/to/project/.gitignore

# Add a specific file
$ gg -f config.local.yaml
Successfully added path to .gitignore: config.local.yaml
File location: /path/to/project/.gitignore
```

## License

This project is licensed under the GPLv3 License. See the [LICENSE](LICENSE) file for details.

## Contributing

Issues and Pull Requests are welcome!

## Support the Author

If you find gg helpful, feel free to buy the author a coffee ☕

<div style="display: flex; gap: 10px;">
  <img src="docs/alipay.jpg" alt="Alipay" width="200"  height="373"/>
  <img src="docs/wcpay.png" alt="WeChat Pay" width="200" height="373"/>
</div>
