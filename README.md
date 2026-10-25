My First MCP Server

A beginner-friendly implementation of the Model Context Protocol (MCP) using Python. This project demonstrates how to expose tools that AI applications can discover and call through an MCP server.

About the Project

The Model Context Protocol (MCP) is an open protocol that allows AI applications to connect to external tools, data sources, and services through a standardized interface.

In this project, I will build an MCP server from scratch to understand how MCP works, how tools are registered, and how an AI client can interact with them.

Objectives

- Understand the fundamentals of MCP.
- Build an MCP server using Python.
- Create and register custom tools.
- Learn how MCP clients discover and call tools.
- Test the server locally.
- Connect the server to a compatible MCP client.
- Explore error handling, security, and deployment.

Tech Stack

- Language: Python
- MCP SDK: Official Python MCP SDK ("mcp")
- Package management: Python "venv" and "pip"
- Development environment: Windows or Linux
- Communication: MCP transport, starting with STDIO

Project Structure

my-first-mcp-server/
├── server.py
├── pyproject.toml
├── README.md
└── .gitignore

Getting Started

1. Clone the repository

git clone <your-repository-url>
cd my-first-mcp-server

2. Create a virtual environment

Windows PowerShell

python -m venv .venv
.\.venv\Scripts\Activate.ps1

Linux

python3 -m venv .venv
source .venv/bin/activate

3. Install dependencies

Install the official MCP Python SDK:

python -m pip install "mcp[cli]"

4. Run the server

python server.py

The server should start and wait for an MCP client to communicate with it. With STDIO transport, it is normal for the server to produce no ordinary terminal output while waiting for requests.

Planned Features

- [ ] Create the basic MCP server.
- [ ] Implement a simple greeting tool.
- [ ] Implement basic arithmetic tools.
- [ ] Add a tool that retrieves useful information.
- [ ] Learn how tools are discovered and invoked.
- [ ] Test tool calls with the MCP Inspector.
- [ ] Connect the server to a compatible AI client.
- [ ] Add input validation and error handling.
- [ ] Document installation and usage.
- [ ] Add automated tests.

How MCP Works

1. An AI application connects to the MCP server.
2. The client discovers the tools provided by the server.
3. The AI application decides when a tool is useful.
4. The client sends a request to call the selected tool.
5. The server executes the tool and returns its result.
6. The AI application uses that result to respond to the user.

Important: An MCP server provides tools and data. The AI model and client determine how those capabilities are used.

Testing

The MCP Inspector can help you inspect the server, discover available tools, and test tool calls.

npx -y @modelcontextprotocol/inspector

Follow the Inspector's instructions to configure and launch your Python server.

Security Considerations

- Validate all tool inputs.
- Never hardcode API keys or passwords.
- Store secrets in environment variables.
- Avoid exposing sensitive files or system commands.
- Require authorization for tools that modify data or perform external actions.
- Treat tool inputs and external responses as untrusted data.

Learning Resources

- "Official MCP Documentation" (https://modelcontextprotocol.io/)
- "MCP Python SDK" (https://github.com/modelcontextprotocol/python-sdk)
- "MCP Inspector" (https://github.com/modelcontextprotocol/inspector)

License

This project is intended for learning and experimentation. A license can be added when the project is ready for public distribution.
