---
applyTo: "**/*.{cpp,hpp,h,c}"
---

# C/C++ Code Review Instructions

These instructions apply specifically to C and C++ (`.c`, `.cpp`, `.h`, `.hpp`) files in this repository.

## Style

- Use **4 spaces** for indentation (no tabs).
- Maximum line length is **100 characters**.
- Use `snake_case` or `PascalCase` for file names (be consistent within a module).
- Use `PascalCase` for class and struct names.
- Use `snake_case` for function and variable names.
- Use `UPPER_SNAKE_CASE` for macros and compile-time constants.

## Documentation

- Every public function and class **must** have a doc comment (Doxygen-style preferred).
- Describe parameters, return values, and any side effects.

## Memory Management

- Prefer RAII and smart pointers (`std::unique_ptr`, `std::shared_ptr`) over raw pointers.
- Every `new` must have a corresponding `delete`; prefer containers and smart pointers to avoid manual management.
- Check for memory leaks, dangling pointers, and double-free issues.

## Error Handling

- Use exceptions or return codes consistently — do not mix both styles within a module.
- Check return values of system calls and library functions.
- Never ignore errors silently.

## Safety

- Avoid unsafe functions (e.g., `strcpy`, `sprintf`) — prefer their bounded equivalents (e.g., `strncpy`, `snprintf`).
- Validate all external inputs.
- Avoid undefined behaviour (e.g., signed integer overflow, out-of-bounds access).

## Modern C++

- Prefer modern C++ features (C++11 and later): range-based for, `auto`, lambdas, `nullptr` over `NULL`.
- Use the standard library (`<algorithm>`, `<vector>`, etc.) instead of reinventing common operations.
