# Haggle - AI-Powered Price Finding Bot

An intelligent Telegram bot that helps users find product prices and deals using AI agents. Built with NestJS, LangGraph, and OpenAI.

## Features

- **Multi-Agent Architecture**: Uses LangGraph to coordinate specialized AI agents
- **Price Discovery**: Web scraping and price comparison capabilities via Computer Use Agent (CUA)
- **Telegram Integration**: Real-time chat interface for seamless user interaction
- **Intelligent Routing**: Supervisor agent automatically routes queries to appropriate specialists
- **Memory Management**: Persistent conversation context across interactions

## Tech Stack

- **Backend**: NestJS, TypeScript
- **AI/ML**: LangGraph, LangChain, OpenAI GPT-4o-mini
- **Web Scraping**: Scrapybara
- **Chat**: Telegram Bot API (Grammy)
- **Deployment**: Docker

## Quick Start

### Prerequisites

- Node.js 20+
- Yarn or npm
- OpenAI API key
- Telegram Bot Token

### Installation

```bash
# Install dependencies
yarn install

# Set up environment variables
cp .env.example .env
# Add your OPENAI_API_KEY and TELEGRAM_BOT_TOKEN
```

### Development

```bash
# Start in development mode
yarn run start:dev

# Run tests
yarn run test

# Build for production
yarn run build
```

### Docker

```bash
# Build and run with Docker
docker build -t haggle-bot .
docker run -p 3000:80 haggle-bot
```

## Architecture

The bot uses a multi-agent system:

1. **Supervisor Agent**: Routes user queries to appropriate specialists
2. **Price Finder Agent**: Handles product searches and price comparisons
3. **General Agents**: Handle general conversation and information requests

## API Endpoints

- `GET /api/v1/core` - Health check
- WebSocket connection for real-time chat via Telegram

## License

MIT
