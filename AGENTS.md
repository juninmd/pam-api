```markdown
# AGENTS.md File Guidelines

These guidelines are designed to ensure consistent, maintainable, and high-quality code for all AI coding agents within this repository. Adherence to these principles is crucial for the long-term health and success of the project.

## 1. DRY (Don't Repeat Yourself)

*   **Single Responsibility Principle:** Each agent component should have a clearly defined and focused responsibility. Avoid creating overly complex agents with multiple functions that perform similar tasks.
*   **Code Reuse:** Design agents to be reusable across different projects or scenarios.  Implement abstractions and interfaces where possible to promote modularity.
*   **Pattern Matching:** Utilize pattern matching extensively to reduce boilerplate and improve readability.
*   **Abstraction:**  Create abstract classes or interfaces that encapsulate common functionality, allowing for easier adaptation and reuse.

## 2. KISS (Keep It Simple, Stupid)

*   **Minimize Complexity:** Strive for the simplest possible implementation. Avoid unnecessary features or complexities that can make the code harder to understand.
*   **Readability:** Prioritize clear and concise code. Use meaningful variable names, comments, and indentation.
*   **Efficiency:**  Focus on efficient algorithms and data structures.  Avoid inefficient solutions unless absolutely necessary.
*   **Testability:** Design components to be easily testable.

## 3. SOLID Principles

*   **Single Responsibility:**  Each class and object should have one primary responsibility.
*   **Open/Closed Principle:**  The system should be extensible without modifying the existing code.  Add new functionality through new classes without altering the core logic.
*   **Liskov Substitution Principle:**  Subclasses should be substitutable for their base classes without altering the correctness of the program.
*   **Interface Segregation Principle:**  Clients should not be forced to depend on methods they do not use.
*   **Dependency Inversion Principle:**  High-level modules (classes) should not depend on low-level modules (classes).  Instead, they should depend on abstractions.

## 4. YAGNI (You Aren't Gonna Need It)

*   **Avoid Over-Engineering:**  Do not implement features or functionalities that are not currently required.
*   **Future-Proofing:**  Design agents with flexibility in mind, allowing for potential future extensions without requiring significant changes.
*   **Focus on Core Requirements:**  Prioritize implementing the essential functionality for the current project goals.

## 5. Code Quality & Structure

*   **Line Length:**  Keep lines of code under 180 characters (approximately).
*   **Naming Conventions:**  Follow consistent naming conventions (e.g., camelCase, snake_case).
*   **Comments:**  Write clear and concise comments to explain complex logic or non-obvious design decisions.
*   **Error Handling:** Implement basic error handling to gracefully handle unexpected situations.
*   **Data Structures:**  Choose appropriate data structures for the task.  Consider using collections for efficient data manipulation.
*   **Testing:** All code must have at least 80% test coverage.

## 6.  File Structure & Organization

*   **Modular Design:**  Each agent should be organized into logical modules with well-defined responsibilities.
*   **Clear Separation of Concerns:** Ensure modules are independent and avoid dependencies between them.
*   **Documentation:** Include a concise `README.md` file explaining the purpose of each agent and its dependencies.
*   **Version Control:**  Use a version control system (e.g., Git) to track changes to the code.

## 7.  Testing

*   **Unit Tests:** Focus on creating unit tests for individual agents and functions.
*   **Test Driven Development:** Utilize test-driven development practices.
*   **Mocking/Stubbing:**  *Only* use mocks or stubs for testing purposes.  Do not rely on real implementations.

## 8.  Code Style

*   **Consistent Formatting:** Use a consistent code formatting style (e.g., black fork, whitespace).
*   **Indentation:**  Use consistent indentation.
*   **Error Detection:** Employ static code analysis tools to identify potential issues.

## 9.  Documentation (Within Files)

*   **Docstrings:**  All functions and classes should have comprehensive docstrings explaining their purpose, parameters, and return values.
*   **Comments:** Use comments to explain complex logic and non-obvious design choices.

## 10.  Commit Strategy

*   **Small, Focused Commits:**  Break down large changes into small, manageable commits.
*   **Meaningful Commit Messages:** Write clear and descriptive commit messages.

These guidelines are designed to promote a high-quality, maintainable, and efficient codebase.  They are intended to be a living document and should be reviewed and updated as needed.
```