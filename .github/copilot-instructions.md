---
description: "Rules for C# and .NET development"
applyTo: "**/*.cs"
---

# C# Development Standards

## 1. Syntax & Modern Features
- **File-Scoped Namespaces:** Use `namespace MyProject;` instead of block-scoped braces.
- **Implicit Typing:** Use `var` only when the type is clearly evident from the right-hand side (e.g., `var users = new List<User>();`).
- **Primary Constructors:** Prefer primary constructors for classes and structs (C# 12+).
- **Target-Typed New:** Use `List<string> list = new();` where the type is already declared.

## 2. Naming Conventions
- **Interfaces:** Prefix with a capital `I` (e.g., `IRepository`).
- **Async Methods:** Always suffix asynchronous methods with `Async` (e.g., `GetRecordAsync`).
- **Private Fields:** Use camelCase with an underscore prefix (e.g., `_logger`).

## 3. Performance & Safety
- **Null Safety:** Enable and respect nullable reference types. Use null-conditional operators (`?.`) and null-coalescing (`??`).
- **Resource Management:** Use `using` declarations (e.g., `using var stream = ...`) for `IDisposable` types to ensure automatic cleanup.
- **Async/Await:** Avoid `.Result` or `.Wait()` to prevent deadlocks; always use `await`.

## 4. Documentation & Clean Code
- **XML Comments:** Provide `<summary>` tags for all public methods and properties.
- **Line Length:** Keep code lines under 120 characters for readability.
- **Braces:** Always include braces `{ }` even for single-line statements.