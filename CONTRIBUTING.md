# Contributing to Flutter App Launcher

Thank you for your interest in contributing to Flutter App Launcher! We welcome contributions from the community.

## Code of Conduct

By participating in this project, you are expected to uphold our Code of Conduct. Please report unacceptable behavior to the project maintainers.

## How to Contribute

### Reporting Bugs

Before creating bug reports, please check the existing issues to avoid duplicates. When creating a bug report, please include:

- A clear and descriptive title
- Steps to reproduce the issue
- Expected vs actual behavior
- Your environment (Flutter version, platform, device, etc.)
- Screenshots or code snippets if applicable

Use our [Bug Report Template](.github/ISSUE_TEMPLATE/bug_report.yml) when filing issues.

### Suggesting Features

Feature requests are welcome! Please use our [Feature Request Template](.github/ISSUE_TEMPLATE/feature_request.yml) and include:

- A clear description of the problem you're trying to solve
- Your proposed solution
- Any alternative solutions you've considered
- Use cases and examples

### Pull Requests

1. **Fork the repository** and create your branch from `develop`
2. **Follow the coding standards** outlined below
3. **Write comprehensive tests** for your changes
4. **Update documentation** as needed
5. **Run all checks locally** before submitting
6. **Create a Pull Request** using our template

## Development Setup

### Prerequisites

- Flutter SDK 3.35.1 or later
- Dart SDK (included with Flutter)
- Git
- IDE with Flutter support (VS Code, IntelliJ, etc.)

### Environment Setup

1. **Clone the repository:**
   ```bash
   git clone https://github.com/your-username/flutter_app_launcher.git
   cd flutter_app_launcher
   ```

2. **Get dependencies:**
   ```bash
   flutter pub get
   ```

3. **Run code analysis:**
   ```bash
   flutter analyze
   ```

4. **Run tests:**
   ```bash
   flutter test
   ```

### Platform-Specific Setup

#### Android
- Android Studio with Android SDK
- Java 17 or later
- Android device or emulator

#### iOS
- Xcode (latest stable version)
- iOS Simulator or physical device
- macOS development machine

#### macOS
- Xcode with macOS development tools
- macOS development machine

## Coding Standards

### Code Style

We use strict linting rules based on `package:lints/strict.yaml`. Please ensure your code:

- Follows Dart language conventions
- Uses single quotes for strings
- Has trailing commas in function calls and constructors
- Is properly formatted with `dart format`
- Has comprehensive documentation comments
- Uses descriptive variable and function names

### Code Quality

- **Write tests** for all new functionality
- **Maintain test coverage** above 90%
- **Document public APIs** with comprehensive dartdoc comments
- **Handle errors gracefully** with proper exception handling
- **Follow platform conventions** for native implementations

### Commit Messages

Use clear and descriptive commit messages:

```
type(scope): description

Longer explanation if needed

Fixes #123
```

Types:
- `feat`: New feature
- `fix`: Bug fix
- `docs`: Documentation changes
- `style`: Code style changes (formatting, etc.)
- `refactor`: Code refactoring
- `test`: Adding or fixing tests
- `chore`: Maintenance tasks

### Branch Naming

Use descriptive branch names:
- `feature/add-ios-support`
- `fix/android-launch-issue`
- `docs/update-readme`

## Testing

### Running Tests

```bash
# Unit tests
flutter test

# Integration tests (requires platform setup)
flutter test integration_test/

# Test with coverage
flutter test --coverage
```

### Test Requirements

- **Unit tests** for all business logic
- **Integration tests** for platform implementations
- **Widget tests** for UI components (if applicable)
- **Documentation tests** to verify examples work

### Test Structure

```dart
void main() {
  group('FeatureName', () {
    setUp(() {
      // Setup code
    });

    testWidgets('should do something', (tester) async {
      // Test implementation
    });

    tearDown(() {
      // Cleanup code
    });
  });
}
```

## Documentation

### API Documentation

- Use triple-slash comments (`///`) for public APIs
- Include examples in documentation
- Document parameters, return values, and exceptions
- Keep documentation up to date with code changes

```dart
/// Launches an external application by its identifier.
///
/// The [appId] parameter specifies the application to launch.
/// On Android, this should be the package name (e.g., 'com.example.app').
/// On iOS, this should be the bundle identifier or URL scheme.
/// On macOS, this should be the bundle identifier or application name.
///
/// Returns `true` if the app was successfully launched, `false` otherwise.
///
/// Throws [PlatformException] if the platform is not supported or if there's
/// an error during the launch process.
///
/// Example:
/// ```dart
/// bool launched = await FlutterAppLauncher.launchApp('com.spotify.music');
/// if (launched) {
///   print('Spotify launched successfully');
/// } else {
///   print('Failed to launch Spotify');
/// }
/// ```
Future<bool> launchApp(String appId) async {
  // Implementation
}
```

### README Updates

When adding new features, update the README.md with:
- Installation instructions
- Usage examples
- API documentation links
- Platform compatibility information

## Release Process

### Version Numbering

We follow [Semantic Versioning](https://semver.org/):
- **Major** (`1.0.0`): Breaking changes
- **Minor** (`0.1.0`): New features, backward compatible
- **Patch** (`0.0.1`): Bug fixes, backward compatible

### Release Checklist

- [ ] All tests pass
- [ ] Documentation is updated
- [ ] CHANGELOG.md is updated
- [ ] Version number is bumped in pubspec.yaml
- [ ] Create release tag
- [ ] Publish to pub.dev (maintainers only)

## Getting Help

- **Questions?** Open a [Discussion](https://github.com/your-username/flutter_app_launcher/discussions)
- **Bug Reports?** Use the [Bug Report Template](.github/ISSUE_TEMPLATE/bug_report.yml)
- **Feature Ideas?** Use the [Feature Request Template](.github/ISSUE_TEMPLATE/feature_request.yml)
- **Security Issues?** Email maintainers directly (see SECURITY.md)

## Recognition

Contributors will be recognized in our README.md and release notes. Thank you for helping make Flutter App Launcher better!

---

By contributing to Flutter App Launcher, you agree that your contributions will be licensed under the same license as the project.