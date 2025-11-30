# MCP-Universe-Research-0030 Setup Guide

## Project Overview
This repository contains the MCP-Universe-Research-0030 project, a comprehensive evaluation framework for LLMs using the novel Model Context Protocol (MCP) technique.

## Repository Structure

### Branches
- **main**: Production-ready code with basic README
- **dev**: Development branch with full project structure and automation

### Directory Structure (dev branch)
```
├── benchmark/          # Benchmarking tools and evaluation metrics
│   └── __init__.py
├── agents/            # Agent implementations and configurations
│   └── __init__.py
├── mcp_server/        # MCP server implementations and utilities
│   └── __init__.py
├── scripts/           # Automation and utility scripts
│   └── issue_automation.py
├── .github/workflows/ # GitHub Actions workflows
│   └── issue-automation.yml
└── docs/              # Documentation
    └── SETUP_GUIDE.md
```

## GitHub Automation

### Issue Label Automation
The repository includes automated issue handling based on labels:

1. **Bug Issues** (`bug` label): Automatically receives comment: "Thank you. We will fix it."
2. **Feature Requests** (`feature` label): Automatically receives comment: "Thank you, we will consider to include this feature."
3. **Discussion Issues** (`discussion` label): Automatically receives comment: "Thanks for starting this discussion! We welcome community input."

### Implementation
- **GitHub Actions Workflow**: `.github/workflows/issue-automation.yml`
- **Python Script**: `scripts/issue_automation.py` (for testing/local development)

### Testing the Automation
To test the automation, create issues with the following titles and labels:
1. "Bug in benchmark logic" (label: `bug`)
2. "Feature: New agent scoring metric" (label: `feature`)
3. "Discussion: Evaluation metrics alignment" (label: `discussion`)

## Getting Started

### Prerequisites
- Python 3.8+
- Git
- GitHub account with repository access

### Setup Instructions
1. Clone the repository:
   ```bash
   git clone https://github.com/sarahmoon71560sarahmoon/harmony.git
   cd harmony
   ```

2. Switch to dev branch:
   ```bash
   git checkout dev
   ```

3. Install Python dependencies (when available):
   ```bash
   pip install -r requirements.txt
   ```

4. Test the automation script:
   ```bash
   python scripts/issue_automation.py --label bug --issue-number 1 --dry-run
   ```

## Development Workflow

1. **Feature Development**: Work on the `dev` branch
2. **Testing**: Test changes locally before pushing
3. **Pull Requests**: Create PRs from `dev` to `main` for production releases
4. **Issue Management**: Use appropriate labels for automatic handling

## MCP Integration
The project leverages the Model Context Protocol (MCP) for evaluating LLM capabilities. Reference the official MCP repository: https://github.com/modelcontextprotocol

## Contributing
1. Fork the repository
2. Create a feature branch
3. Make your changes
4. Test thoroughly
5. Submit a pull request

## License
[Add appropriate license information here]