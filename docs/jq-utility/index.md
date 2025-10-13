# jq Utility: Command-Line JSON Processing

Welcome to the documentation for **jq**, the indispensable command-line tool often described as "sed for JSON."

In data-intensive fields-from log analysis to biomedical data pipelines-we frequently deal with massive data streams formatted as JSON Lines (`.jsonl`). As professionals transitioning from fields that demand **data integrity** and **regulatory precision** (like neuroscience), we understand the critical need to validate and transform these files quickly.

Rather than writing slow, resource-intesive scripts in Python or JavaScript just to inspect data, `jq` allows for **rapid, efficient, and precise** manipulation of structured data directly in the terminal. It provides the expressive power needed to relaibly slice, filter, and map complex data streams, ensuring quick validation and preparation for downstream analysis without ever loading the entire dataset into memory. This guide will help you master `jq`'s filter language and elevate your data processing efficiency.

# Installation

The best way to install `jq` depends on your operating system. For WSL (Linux) environments, use `apt-get`. For macOS environments, use Homebrew.

| Operating System          | Command                   |
|---------------------------|---------------------------|
| WSL/Linux (Debian/Ubuntu) | `sudo apt-get install jq` |
| macOS (Homebrew)          | brew install jq           |

## Getting Started
Ready to start querying data?
- [Start the Tutorial](./getting-started.md): Jump right in and learn how to filter, select, and project data using the `jq` filter language with practical, real-world examples.
- [See Full Command Reference](./reference.md): A comprehensive table of all `jq` functions and flags.