# Dune Analytics MCP Server

[![smithery badge](https://smithery.ai/badge/@kukapay/dune-analytics-mcp)](https://smithery.ai/server/@kukapay/dune-analytics-mcp)

A mcp server that bridges Dune Analytics data to AI agents.

## Features

- **Tools**: 
  - `get_latest_result`: Fetch the latest results of a Dune query by ID.
  - `run_query`: Execute a Dune query by ID and retrieve results.
- **CSV Output**: All results are returned as CSV-formatted strings for easy processing.

## Prerequisites

- Python 3.10+
- A valid Dune Analytics API key (get one from [Dune Analytics](https://dune.com/settings/api))

## Installation

### Installing via Smithery

To install Dune Analytics for Claude Desktop automatically via [Smithery](https://smithery.ai/server/@kukapay/dune-analytics-mcp):

```bash
npx -y @smithery/cli install @kukapay/dune-analytics-mcp --client claude
```

### Manual Installation

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/kukapay/dune-analytics-mcp.git
   cd dune-analytics-mcp
   ```

2. **Set Up Environment Variables**:
   Create a `.env` file in the project root:
   ```
   DUNE_API_KEY=your_api_key_here
   ```
   Alternatively, set it as a system environment variable:
   ```bash
   export DUNE_API_KEY="your_api_key_here"
   ```

## Usage

### Running the Server

- **Development Mode**:
  ```bash
  mcp dev main.py
  ```
  This starts the server with hot reloading for development.

- **Install for Claude Desktop**:
  ```bash
  mcp install main.py --name "Dune Analytics"
  ```
  Installs the server as a service for use with Claude Desktop.

### Tool Usage

1. **`get_latest_result(query_id)`**
   - **Description**: Retrieves the latest results of a specified Dune query.
   - **Input**: `query_id` (int) - The ID of the Dune query.
   - **Output**: CSV-formatted string of the query results.
   - **Example**:
     ```
     get_latest_result(query_id=4853921)
     ```

2. **`run_query(query_id)`**
   - **Description**: Executes a Dune query and returns the results.
   - **Input**: `query_id` (int) - The ID of the Dune query to run.
   - **Output**: CSV-formatted string of the query results.
   - **Example**:
     ```
     run_query(query_id=1215383)
     ```

### Example Commands in Claude Desktop

- "Get latest results for dune query 1215383"
- "Run dune query 1215383"


## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
