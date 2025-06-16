# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Munin is an automated job search and tailored resume creation tool built with Python 3.12. The project uses modern Python tooling with strict quality standards.

## Development Commands

### Environment Setup
```bash
uv sync                    # Install dependencies
```

### Code Quality
```bash
uv run python -m black .              # Format code
uv run python -m ruff check .         # Lint code  
uv run python -m ruff format .        # Format with Ruff
uv run python -m pyright .            # Type checking
```

### Testing
```bash
# Testing framework not yet implemented - likely pytest when added
```

## Architecture

The project uses modern Python patterns with strict type checking and validation:

- **Package Manager**: UV (ultra-fast Python package resolver)
- **Type Checking**: Pyright in strict mode
- **Data Validation**: Pydantic 2.11.3 for structured data handling
- **HTTP Client**: Requests for API integration
- **Code Quality**: Black + Ruff with comprehensive rule set (ALL rules enabled)

## Important Configuration

- **Python Version**: Exactly 3.12 (strict requirement)
- **Import Organization**: Custom isort sections for networking, validation, and typing libraries
- **Stub Path**: `src/munin/stubs` for type stubs
- **Cache Directory**: `./uv/cache` for UV package cache

## Code Standards

- All code must pass Pyright strict type checking
- Comprehensive linting with minimal Ruff rule exceptions
- Preview features enabled for both Black and Ruff
- Cross-platform support (Windows/Linux) configured