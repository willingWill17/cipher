# Byterover Cipher - AI Agent Memory Framework

## Project Overview

Byterover Cipher is an open-source memory layer designed specifically for coding agents. It provides a robust framework with MCP (Model Context Protocol) integration, allowing memory persistence across various IDEs and AI tools (Cursor, Codex, Claude Code, Windsurf, Cline, Gemini CLI, VS Code, etc.).

### Key Features
- **MCP Integration**: Native support for the Model Context Protocol.
- **Dual Memory Layer**: Captures both System 1 (Programming Concepts & Business Logic) and System 2 (reasoning steps of the model).
- **Multi-Environment Support**: Works across different IDEs while sharing the same memory context.
- **Real-time Communication**: Includes API and WebSocket support for agent interactions.

## Architecture

The project is a TypeScript/Node.js monorepo using `pnpm`.
- `src/core/`: Contains the core logic for the AI memory agent, vector databases, and abstractions.
- `src/app/`: Contains the application layers:
  - `cli/`: Interactive command-line interface.
  - `mcp/`: Model Context Protocol server implementation.
  - `api/`: REST API server with WebSocket support.
  - `ui/`: Full-stack web application.

## Development Guidelines

1. **Language & Tools**: TypeScript, Node.js (>=20), `pnpm`.
2. **Formatting**: The project uses Prettier and ESLint. When generating code, adhere to standard TypeScript patterns, strict typing, and existing configurations.
3. **Execution**: The CLI entrypoint is at `dist/src/app/index.cjs` after building (`pnpm build`).

## AI Assistant Instructions

When assisting with this repository:
- Understand that this is a foundational framework for *other* AI agents to have memory.
- Prefer `pnpm` for any package management commands.
- Focus on robust typing and modularity. 
- When editing or analyzing MCP features, look into the `src/app/mcp` and `src/core` directories. 
- Always consider the impact on the Dual Memory Layer and existing database abstractions (SQLite, Postgres, etc.) when suggesting architectural changes.