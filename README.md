# MCP Kakao Local

The MCP connects to the [Kakao Local API](https://developers.kakao.com/docs/latest/ko/local/common) and Kakao Map. 카카오 로컬 API 및 카카오맵에 연결하는 MCP 서버.

<a href="https://glama.ai/mcp/servers/@yunkee-lee/mcp-kakao-local">
  <img width="380" height="200" src="https://glama.ai/mcp/servers/@yunkee-lee/mcp-kakao-local/badge" alt="Kakao Local MCP server" />
</a>

## Prerequisites

Before you begin, ensure you have the following installed:

* **Python:** Version 3.13 or higher
* **uv:** You can find installation instructions [here](https://github.com/astral-sh/uv).
* **Kakao Developers:** You need API credentials from the [Kakao developers](https://developers.kakao.com/).

## Configuration

1. **Create a `.env` file:**  Create a file in the project root.

2. **Add API Credentials:** Edit the `.env` file and add your Kakao REST API credentials.
    ```.env
    REST_API_KEY="YOUR_REST_API_KEY_HERE"
    ```
    Please verify the exact environment variable names required by checking `src/mcp_kakao_local/kakao_local_client.py`.

## Running the MCP

1. **Sync Dependencies:** Navigate to the project root directory in your terminal and run the following command. This will create a virtual environment (if one doesn't exist) and install all dependencies specified in `pyproject.toml`.
    ```bash
    uv sync
    ```

2. **Run:**: You can run the MCP server using `uv`.
    ```bash
    uv run src/mcp_kakao_local
    ```

    For development,
    ```bash
    source .venv/bin/activate
    mcp dev src/mcp_kakao_local/server.py
    ```