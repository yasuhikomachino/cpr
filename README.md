# CPR

A shell script that creates a private repository on GitHub and automatically sets up initial files (README.md and .gitignore).

## Requirements

- Git
- GitHub CLI (gh)
- Bash

## Setup

### Method 1: Create Symbolic Link (Recommended)

```bash
# Clone the repository
git clone https://github.com/yasuhikomachino/cpr.git
cd cpr

# Make executable
chmod +x cpr

# Create symbolic link
sudo ln -s $(pwd)/cpr /usr/local/bin/cpr
```

Or, install to user local

```bash
mkdir -p ~/.local/bin
ln -s $(pwd)/cpr ~/.local/bin/cpr

# Ensure ~/.local/bin is in your PATH
echo 'export PATH="$HOME/.local/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc
```

### Method 2: Set Alias

```bash
# Add to ~/.bashrc or ~/.zshrc
echo 'alias cpr="~/path/to/cpr/cpr"' >> ~/.bashrc
source ~/.bashrc
```

### Method 3: Add to PATH

```bash
# Add script directory to PATH
echo 'export PATH="$HOME/path/to/cpr:$PATH"' >> ~/.bashrc
source ~/.bashrc

# Make executable (if needed)
chmod +x cpr
```

## Usage

```bash
cpr my-new-project
```

Specify the repository name as an argument.

## Features

- Automatically creates a private repository on GitHub
- Creates a local directory (same as repository name)
- Initializes Git repository
- Generates README.md (containing only the repository name)
- Generates .gitignore file (with common exclusion patterns)
- Creates initial commit
- Automatically pushes to GitHub

## License

MIT License
