# MCP Demo (Python)

This is a simple MCP (Modular Command Platform) demo server written in Python.

## Prerequisites

- Python 3.11+
- [pipx](https://pypa.github.io/pipx/) (recommended for global CLI install)
- (Optional) [python-dotenv](https://pypi.org/project/python-dotenv/) if you want to use environment variables from a `.env` file

## Setup

1. **Clone the repository:**
   ```sh
   git clone <your-repo-url>
   cd mcp_demo
   ```

2. **Install globally using pipx (recommended):**
   ```sh
   pipx install .
   ```
   This will make the `mcp-demo` command available globally in your shell.

   If you update the code, run:
   ```sh
   pipx reinstall mcp-demo
   ```

3. **(Optional) Create a `.env` file if you need environment variables.**

## Running the MCP Server

You can now run the MCP server from anywhere using:
```sh
mcp-demo
```

Or, you can still use `uv` and the stdio transport. Here is an example JSON configuration to add the server:

```json
"mcp": {
    "servers": {
        "simple-app-stdio": {
            "type": "stdio",
            "command": "mcp-demo"
        }
    }
}
```

- Adjust the `command` path as needed for your environment.

Alternatively, you can run the server directly (if not using pipx):
```sh
uv run --directory . server.py
```

## Features

- Simple calculator tool (add two numbers)
- Easily extensible with more tools

## File Overview

- `server.py`: Main MCP server implementation
- `main.py`: (empty or for future use)
- `pyproject.toml`: Project metadata and dependencies

---

Feel free to extend this demo with more tools and features!