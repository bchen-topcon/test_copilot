# C/C++ Coding Standards

This document defines C and C++ coding conventions for this repository, based on the
[Qt Coding Style](https://wiki.qt.io/Qt_Coding_Style) and
[Qt Coding Conventions](https://wiki.qt.io/Coding_Conventions).
For general standards that apply to all languages, see [`coding-standards.md`](coding-standards.md).

---

## Indentation

- Use **4 spaces** per indentation level — never tabs.
- Do not use more than one consecutive blank line to separate code blocks.

---

## Naming Conventions

- **Classes and structs**: `UpperCamelCase` (e.g., `MyWidget`, `DataProcessor`).
- **Functions and variables**: `lowerCamelCase` (e.g., `doSomething()`, `myVariable`).
- **Constants and macros**: `UPPER_SNAKE_CASE` (e.g., `MAX_BUFFER_SIZE`).
- **File names**: lowercase, matching the class name (e.g., `mywidget.cpp`, `mywidget.h`).
- **Acronyms in names**: treat as a single word in camel case (e.g., `XmlParser`, not
  `XMLParser`).

---

## Braces

- Opening brace for **control statements** (`if`, `for`, `while`, etc.) goes on the **same
  line** as the statement:

  ```cpp
  if (condition) {
      doSomething();
  } else {
      doSomethingElse();
  }
  ```

- Opening brace for **function and class definitions** goes on its **own line**:

  ```cpp
  class MyClass
  {
  public:
      void myFunction();
  };

  void MyClass::myFunction()
  {
      // ...
  }
  ```

- Use braces even for single-line bodies when the if/else chain mixes single and multi-line
  branches (keep braces symmetrical).

---

## Spaces and Declarations

- Put one space after keywords (`if`, `for`, `while`, `switch`, etc.).
- Attach `*` and `&` to the variable name, not the type: `char *pointer`, `int &ref`.
- Declare each variable on its own line, close to where it is first used.
- Use a blank line to group logically related statements, but never more than one blank line.

---

## Include Guards and Headers

- Every header file must have an include guard or `#pragma once`.
- Prefer angle brackets for Qt and system headers: `#include <QObject>`, `#include <vector>`.
- Use double quotes only for project-local headers: `#include "myclass.h"`.

---

## Documentation

- Every public function and class **must** have a doc comment explaining its purpose.
- Use Doxygen-compatible block comments (`/** ... */`) for API documentation, describing
  parameters, return values, and notable side effects.
- Short inline notes use `//`; longer explanations use `/* ... */`.

---

## Memory Management

- Prefer RAII. Use smart pointers (`std::unique_ptr`, `std::shared_ptr`) or Qt parent-child
  ownership rather than manual `new`/`delete`.
- Every `new` without a parent must have a corresponding `delete`; prefer containers and smart
  pointers to eliminate manual management.
- Check for memory leaks, dangling pointers, and double-free issues.

---

## Error Handling

- Use exceptions or return codes consistently within a module — do not mix both styles.
- Check return values of system calls and library functions.
- Never ignore errors silently.

---

## Safety

- Avoid unsafe functions (e.g., `strcpy`, `sprintf`) — prefer their bounded equivalents
  (e.g., `strncpy`, `snprintf`).
- Validate all external inputs.
- Avoid undefined behaviour (e.g., signed integer overflow, out-of-bounds array access).

---

## Modern C++

- Prefer modern C++ features (C++11 and later): range-based `for`, `auto`, lambdas, `nullptr`
  instead of `NULL`.
- Use the standard library (`<algorithm>`, `<vector>`, etc.) instead of reinventing common
  operations.
