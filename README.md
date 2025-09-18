# JavaScript Binary Tool

A command-line binary written in JavaScript that demonstrates how to create executable scripts using Node.js.

## Features

- 🚀 **Executable Binary**: Can be run directly from the command line
- 🎨 **Colorful Output**: Uses ANSI colors for better user experience
- 🧮 **Calculator**: Simple mathematical expression evaluation
- 📁 **File Explorer**: List files and directories
- 💻 **System Info**: Display system and Node.js information
- 👋 **Interactive Commands**: Greeting and time display

## Installation

1. Ensure you have Node.js installed (version 14.0.0 or higher)
2. Make the script executable:
   ```bash
   chmod +x bin/js-tool
   ```

## Usage

### Direct Execution
```bash
./bin/js-tool [command] [options]
```

### Available Commands

| Command | Description | Example |
|---------|-------------|---------|
| `help`, `-h`, `--help` | Show help message | `./bin/js-tool help` |
| `version`, `-v`, `--version` | Show version info | `./bin/js-tool version` |
| `info` | Display system information | `./bin/js-tool info` |
| `time` | Show current date and time | `./bin/js-tool time` |
| `files [directory]` | List files in directory | `./bin/js-tool files /home` |
| `greet [name]` | Greet someone | `./bin/js-tool greet Alice` |
| `calc [expression]` | Simple calculator | `./bin/js-tool calc "2 + 2"` |

### Examples

```bash
# Show help
./bin/js-tool help

# Greet someone
./bin/js-tool greet "World"

# Calculate mathematical expressions
./bin/js-tool calc "15 * 3 + 5"

# List files in current directory
./bin/js-tool files

# Show system information
./bin/js-tool info

# Display current time
./bin/js-tool time
```

## Global Installation (Optional)

To install globally using npm:

```bash
npm install -g .
```

Then you can use it anywhere as:
```bash
js-tool help
```

## How It Works

1. **Shebang Line**: The script starts with `#!/usr/bin/env node` which tells the system to use Node.js to execute the file
2. **Executable Permissions**: The file has executable permissions set with `chmod +x`
3. **Command Line Arguments**: Uses `process.argv` to parse command line arguments
4. **Binary Configuration**: The `package.json` includes a `bin` field that maps the command name to the script

## File Structure

```
/workspace/
├── package.json          # Package configuration with bin field
├── bin/
│   └── js-tool          # Main executable script
└── README.md            # This documentation
```

## Technical Details

- **Platform**: Cross-platform (Linux, macOS, Windows)
- **Node.js Version**: Requires Node.js 14.0.0 or higher
- **Dependencies**: Uses only Node.js built-in modules (fs, path, child_process)
- **Error Handling**: Graceful error handling for invalid commands and expressions
- **Security**: Calculator function includes basic input validation

## License

MIT License