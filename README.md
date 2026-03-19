# test_copilot

A sandbox repository for evaluating and developing AI coding agent workflows.

## Overview

This is a test/evaluation repository used to assess how AI coding agents (e.g., GitHub Copilot) interact with structured codebases, follow coding standards, and perform code reviews and modifications.

The project contains sample code in multiple languages, comprehensive documentation, and guidance for agent-based workflows.

## Project Structure

```
test_copilot/
├── AGENTS.md                          # AI agent guidance and workflows
├── README.md                          # This file
├── .github/
│   ├── copilot-instructions.md        # GitHub Copilot-specific rules
│   ├── instructions/
│   │   ├── cpp.instructions.md        # C++ coding conventions
│   │   └── python.instructions.md     # Python coding conventions
│   ├── ISSUE_TEMPLATE/
│   │   ├── bug_report.md              # Bug report template
│   │   └── feature_request.md         # Feature request template
│   └── PULL_REQUEST_TEMPLATE.md       # PR template
├── custom-instructions/               # Additional AI assistant instructions
├── docs/
│   ├── architecture.md                # System architecture
│   ├── contributing.md                # Contribution workflow
│   ├── coding-standards.md            # General coding standards
│   ├── cpp-coding-standards.md        # C++ specific standards
│   └── python-coding-standards.md     # Python specific standards
├── src/                               # Source code
│   └── README.md                      # Placeholder for source code
├── calculator.py                      # Python calculator module
├── test_calculator.py                 # Unit tests for calculator
└── hello_world.cpp                    # C++ hello world example
```

## Contents

### Python Components
- **[calculator.py](calculator.py)** – A simple calculator module with `add`, `subtract`, `multiply`, and `divide` functions.
- **[test_calculator.py](test_calculator.py)** – Unit tests using `pytest`.

### C++ Components
- **[hello_world.cpp](hello_world.cpp)** – A basic C++ hello world program.

### Documentation
- **[AGENTS.md](AGENTS.md)** – Guidance for AI coding agents working in this repository.
- **[docs/architecture.md](docs/architecture.md)** – High-level architecture overview.
- **[docs/contributing.md](docs/contributing.md)** – Contribution guidelines and workflows.
- **[docs/coding-standards.md](docs/coding-standards.md)** – General coding conventions.
- **[docs/python-coding-standards.md](docs/python-coding-standards.md)** – Python-specific conventions.
- **[docs/cpp-coding-standards.md](docs/cpp-coding-standards.md)** – C++-specific conventions.
- **[.github/copilot-instructions.md](.github/copilot-instructions.md)** – GitHub Copilot instructions.

## Getting Started

### Prerequisites
- **Python 3.7+** (for running Python code and tests)
- **C++ compiler** (for building C++ code) – e.g., `g++`, `clang`
- **pytest** (for running tests)

### Running Python Tests

Install dependencies:
```bash
pip install pytest
```

Run tests:
```bash
python -m pytest test_calculator.py -v
```

### Building C++ Code

Compile the hello world program:
```bash
g++ hello_world.cpp -o hello_world
./hello_world
```

## Key Conventions

All code in this repository follows the standards documented in `docs/`:

| Convention          | Reference                                  |
| ---                 | ---                                        |
| General standards   | [docs/coding-standards.md](docs/coding-standards.md) |
| Python standards    | [docs/python-coding-standards.md](docs/python-coding-standards.md) |
| C++ standards       | [docs/cpp-coding-standards.md](docs/cpp-coding-standards.md) |
| Agent workflows     | [AGENTS.md](AGENTS.md) |

### Summary
- **Indentation:** 4 spaces (Python/C/C++); 2 spaces (YAML/JSON/HTML)
- **Line length:** Max 100 characters
- **Line endings:** LF (`\n`)
- **Naming:** `snake_case` (Python vars/functions), `PascalCase` (classes), `UPPER_SNAKE_CASE` (constants)

## Contributing

Please see [docs/contributing.md](docs/contributing.md) for detailed contribution guidelines.

## License

No explicit open-source license is currently specified for this repository. All rights are
reserved by the repository owners; please contact the maintainers before reusing or
distributing this code.
