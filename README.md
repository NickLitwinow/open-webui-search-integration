# Open WebUI Search Integration

An integrated solution that combines Open WebUI with search capabilities, enabling enhanced AI interactions with web search functionality. This project provides a comprehensive interface for AI assistants with integrated search capabilities.

## What is This Project?

This project focuses on creating a powerful user interface for AI assistants that integrates web search capabilities. It's built around Open WebUI but extends its functionality with search integration, making it suitable for advanced AI applications.

## Key Features

- **Open WebUI Integration**: Base interface for AI chat and interactions
- **Search Integration**: Enhanced search capabilities for AI responses
- **Model Extension Support**: Easy integration with various AI models
- **Docker-based Deployment**: Simple setup and deployment
- **Privacy-focused**: Local processing with minimal data collection

## Architecture

This setup includes:
1. **Open WebUI** - The main AI chat interface
2. **Search Integration Layer** - Provides web search capabilities to AI assistants
3. **Model Extension Support** - Framework for integrating various AI models

## Getting Started

### Prerequisites
- Docker and Docker Compose installed

### Quick Start

```bash
# Start all services
docker-compose up -d

# Stop all services
docker-compose down
```

### Access

- **Open WebUI Interface**: http://localhost:3000
- **Search Integration API**: http://localhost:8080/search

## Configuration

### Open WebUI Settings
Configuration is managed through environment variables in docker-compose.yml. Key settings include:
- ENABLE_RAG_WEB_SEARCH=True
- RAG_WEB_SEARCH_ENGINE=searxng
- SEARXNG_QUERY_URL=http://searxng:8080/search?q=<query>

### Model Integration
The system is designed to work with various AI models including:
- Ollama models
- Local LLMs
- Cloud-based AI services

## Security

### Environment Setup
For production use, ensure proper environment variables are set in .env file.

## Development

### Customizing Open WebUI
1. Modify docker-compose.yml to change container configurations
2. Adjust environment variables for different model integrations
3. Extend functionality through plugins

### Extending Search Capabilities
The search integration can be extended to support:
- Additional search engines
- Custom search parameters
- Advanced filtering options

## Project Structure

```
.
├── docker-compose.yml     # Docker orchestration
├── .env                   # Environment variables
├── README.md              # This file
└── searxng/               # SearXNG configuration
    └── settings.yml       # Search engine settings
```

## Integration Points

### With Ollama
The system is designed to work seamlessly with Ollama for local AI model execution.

### With Other AI Services
Support for various AI services and models through the Open WebUI framework.

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgements

- [Open WebUI](https://github.com/open-webui/open-webui) - The AI chat interface
- [SearXNG](https://github.com/searxng/searxng) - Search engine backend (when integrated)
