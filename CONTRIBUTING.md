# Contributing to Empire of Ages

Thank you for your interest in contributing! This document provides guidelines for contributing to the project.

## Code of Conduct

- Be respectful and inclusive
- No harassment or discrimination
- Focus on constructive feedback
- Help others learn and grow

## How to Contribute

### Reporting Issues

1. Check if the issue already exists
2. Use a clear, descriptive title
3. Describe the problem in detail
4. Include steps to reproduce
5. Add screenshots/logs if relevant

### Suggesting Enhancements

1. Use a clear title
2. Provide a detailed description
3. Explain the benefits
4. List possible alternatives
5. Include examples if applicable

### Submitting Code

1. Fork the repository
2. Create a feature branch: `git checkout -b feature/feature-name`
3. Make your changes
4. Test thoroughly
5. Commit with clear messages: `git commit -m "Add: feature description"`
6. Push to your fork
7. Open a Pull Request

## Development Workflow

### Setup

```bash
git clone https://github.com/ascatgorbeh-crypto/Empire-of-Ages.git
cd Empire-of-Ages
```

### Branches

- `main`: Release-ready code
- `develop`: Development branch
- `feature/*`: Feature branches
- `bugfix/*`: Bug fix branches
- `hotfix/*`: Critical fixes

### Commit Messages

Format: `Type: Description`

Types:
- `Add`: New feature
- `Fix`: Bug fix
- `Update`: Modification to existing
- `Remove`: Deletion
- `Refactor`: Code restructuring
- `Docs`: Documentation
- `Test`: Tests
- `Style`: Formatting

Example:
```
Add: Implement unit training system
Fix: Resolve save file corruption issue
Update: Improve battle calculation accuracy
```

### Code Style

#### GDScript Guidelines

1. **Naming Conventions**
   - Classes: `PascalCase` (e.g., `GameManager`)
   - Functions: `snake_case` (e.g., `calculate_resources`)
   - Constants: `UPPER_SNAKE_CASE` (e.g., `MAX_POPULATION`)
   - Variables: `snake_case` (e.g., `player_health`)

2. **Code Structure**
   ```gdscript
   extends Node
   
   # Constants
   const MAX_VALUE = 100
   
   # Variables
   var current_value: int = 0
   var is_active: bool = false
   
   # Lifecycle
   func _ready() -> void:
       pass
   
   func _process(delta: float) -> void:
       pass
   
   # Public functions
   func public_method() -> void:
       pass
   
   # Private functions
   func _private_method() -> void:
       pass
   ```

3. **Comments**
   - Use clear, concise comments
   - Explain WHY, not WHAT
   - Use TODO for pending work

4. **Type Hints**
   - Always use type hints
   - Example: `func calculate_damage(attacker: Unit, defender: Unit) -> int:`

### Testing

Before submitting code:

1. Test in Godot editor
2. Test on target platform (Android/iOS if possible)
3. Check for errors in console
4. Run existing tests
5. Add new tests for new features

### Documentation

- Update README.md if needed
- Add comments to complex code
- Document new systems in docs/
- Update API documentation

## Pull Request Process

1. Update documentation
2. Ensure tests pass
3. Add description of changes
4. Link related issues
5. Wait for review
6. Address feedback
7. Get approval before merge

## Code Review

All submissions require review. Reviewers will check:
- Code quality
- Performance implications
- Test coverage
- Documentation
- Alignment with project goals

## Questions?

Open an issue or discussion on GitHub.

---

Thank you for contributing to Empire of Ages! 🏰
