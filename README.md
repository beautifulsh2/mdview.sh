# MDView - Advanced Markdown Viewer and Renderer

## Overview

MDView is a powerful and beautiful Python-based command-line tool designed for rendering and viewing Markdown files with rich formatting directly in your terminal. It combines the flexibility of Markdown with advanced ANSI styling and syntax highlighting to deliver a visually appealing reading experience without leaving your terminal environment.

## Key Features

### Advanced Markdown Rendering
- Supports all standard Markdown syntax including headers, lists, emphasis, and code blocks
- Implements extended Markdown features like tables, task lists, and strikethrough text
- Custom ANSI styling for various Markdown elements with precise control over text appearance

### Syntax Highlighting
- Integrated Pygments-based syntax highlighting for code blocks
- Automatic language detection for accurate code representation
- Fallback formatting for unsupported languages

### Flexible Input Sources
- Read Markdown content from local files
- Fetch Markdown directly from GitHub raw URLs
- Process piped input from other commands

### Output Options
- Terminal-optimized ANSI output with rich formatting
- HTML output option for web-based rendering
- Word limit parameter for previewing long documents

## Installation

Install MDView with a single command:

```bash
wget https://raw.githubusercontent.com/beautifulsh2/mdview.sh/refs/heads/main/src/mdview.py -O mdview && chmod +x mdview
```

For system-wide availability, move the script to your PATH:

```bash
sudo mv mdview /usr/local/bin/
```

## Usage

Basic syntax:
```bash
mdview <filename.md|GitHub-raw-url> [word_limit] [--html]
```

### Examples

View a local Markdown file:
```bash
mdview README.md
```

Preview first 100 words of a document:
```bash
mdview documentation.md 100
```

Render a GitHub file as HTML:
```bash
mdview https://raw.githubusercontent.com/user/repo/main/README.md --html
```

Pipe content to MDView:
```bash
cat notes.md | mdview -
```

## Technical Implementation

MDView utilizes several advanced Python libraries to deliver its functionality:

- **Rich** library for terminal formatting and Markdown rendering
- **Pygments** for syntax highlighting of code blocks
- **Requests** for fetching remote Markdown content
- **Regex** for sophisticated pattern matching and text processing

The tool implements a custom ANSI styling system that provides precise control over text appearance in terminal environments, supporting combinations of bold, italic, underline, and other text decorations.

## Custom Formatting Options

MDView supports extensive text styling through its ANSI code system:

- Basic styles: bold, italic, underline
- Combined styles: bold-italic, bold-underline, italic-underline
- Special formatting: strikethrough, inverse, faint, blink
- Color support: yellow, blue, green text

## Advanced Features

### Table Support
- Automatic detection and formatting of Markdown tables
- Header row highlighting with bold and underline
- Proper column alignment preservation

### Task List Rendering
- Visual distinction between completed and pending tasks
- Custom checkbox symbols for different states
- Faint styling for pending tasks, green for completed

### Blockquote Styling
- Distinctive formatting for quoted text
- Optional color differentiation
- Preservation of nested quotes

## Integration Possibilities

MDView can be integrated into various workflows:

- Documentation preview system
- CI/CD pipeline for Markdown validation
- Git pre-commit hooks for documentation checks
- Combined with file watchers for live preview

## Performance Considerations

The tool is optimized for:
- Efficient processing of large Markdown files
- Minimal memory footprint
- Fast rendering even with complex formatting

## License

MDView is released under the MIT License. See the LICENSE file for full details.

## Contribution

While MDView is currently a stable tool, contributions for advanced features and optimizations are welcome through the GitHub repository.
