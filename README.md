# MCP Demo (Python)

This is a simple MCP (Modular Command Platform) demo server written in Python.

## Prerequisites

- Python 3.11+
- [uv](https://github.com/astral-sh/uv) (a fast Python package manager and runner)
- (Optional) [python-dotenv](https://pypi.org/project/python-dotenv/) if you want to use environment variables from a `.env` file

## Setup

1. **Clone the repository:**
   ```sh
   git clone <your-repo-url>
   cd mcp_demo
   ```

2. **Install dependencies using uv:**
   ```sh
   uv pip install -r requirements.txt
   ```
   Or, if you use a `pyproject.toml`:
   ```sh
   uv pip install -r pyproject.toml
   ```

3. **(Optional) Create a `.env` file if you need environment variables.**

## Running the MCP Server

You can run the MCP server using `uv` and the stdio transport. Here is an example JSON configuration to add the server:

```json
"mcp": {
    "servers": {
        "simple-app-stdio": {
            "type": "stdio",
            "command": "/Library/Frameworks/Python.framework/Versions/3.11/bin/uv",
            "args": [
                "run",
                "--directory",
                "/Users/mikeqiu/code/python/mcp_demo",
                "server.py"
            ]
        }
    }
}
```

- Adjust the `command` and `--directory` paths as needed for your environment.

Alternatively, you can run the server directly:
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