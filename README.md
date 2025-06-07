# A2A-LangGraph: Currency Exchange Agent

A specialized currency exchange rate agent built with LangGraph and A2A SDK, following the Agent-to-Agent (A2A) protocol.

## Overview

This project implements a dedicated Currency Exchange Agent that helps users get real-time exchange rates between different currencies. The agent is built using the LangGraph framework and conforms to the Agent-to-Agent (A2A) protocol, enabling interoperability with other A2A-compatible systems.

## Features

- **Real-time Currency Exchange Rates**: Access up-to-date exchange rates via the Frankfurter API
- **Interactive Conversations**: Ask about currency exchange rates in natural language
- **Streaming Responses**: Get real-time updates as the agent processes your request
- **A2A Protocol Compliant**: Built following the Agent-to-Agent protocol specifications
- **Modular Architecture**: Separate agent implementation, execution, and server components

## Components

- **agent.py**: Core implementation of the Currency Agent using LangGraph and LangChain
- **agent_executor.py**: Handles the execution of agent tasks and manages responses
- **agent_server.py**: Provides an HTTP server with A2A protocol support
- **agent_client.py**: Example client for interacting with the Currency Agent

## Prerequisites

- Python 3.12 or higher
- OpenAI API key (for the LLM)

## Installation

1. Clone this repository:
   ```bash
   git clone <repository-url>
   cd a2a-langgraph
   ```

2. Create and activate a virtual environment:
   ```bash
   python -m venv .venv
   source .venv/bin/activate  # On Windows, use: .venv\Scripts\activate
   ```

3. Install dependencies:

   Option A: Using pip:
   ```bash
   pip install -e .
   ```

   Option B: Using UV (faster installation):
   ```bash
   pip install uv
   uv venv
   uv pip install -e .
   ```

4. Create a `.env` file with your OpenAI API key:
   ```
   OPENAI_API_KEY=your_api_key_here
   ```

## Usage

### Starting the Agent Server

Run the server component:

```bash
python agent_server.py
```

By default, the server runs on `localhost:10000`. You can specify a different host or port:

```bash
python agent_server.py --host 0.0.0.0 --port 8000
```

### Using the Agent Client

Run the client script to interact with the agent:

```bash
python -m agent_client
```

The client will automatically discover the agent capabilities and allow you to query exchange rates.

### Example Queries

- "What is the exchange rate between USD and EUR?"
- "How much is 100 GBP in JPY?"
- "Convert 50 CAD to AUD"

## Architecture

The project follows a modular architecture:

1. **Core Agent (agent.py)**: Implements the currency conversion logic using LangGraph, tools, and LLMs
2. **Agent Executor (agent_executor.py)**: Manages execution flow and handles responses
3. **Server (agent_server.py)**: Provides an HTTP interface following A2A protocol
4. **Client (agent_client.py)**: Example implementation for interacting with the agent

## License

[Add your license information here]

## Contributing

[Add your contribution guidelines here]

## Acknowledgements

- [LangGraph](https://github.com/langchain-ai/langgraph) - For the agent framework
- [A2A SDK](https://github.com/microsoft/agent-protocol) - For the Agent-to-Agent protocol implementation
- [Frankfurter API](https://www.frankfurter.app/) - For providing currency exchange rate data