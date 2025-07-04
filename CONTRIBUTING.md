# 🧑‍💻 Contributing to Real-Time Tree Detector

Thank you for your interest in contributing! We welcome all kinds of contributions: bug reports, feature requests, documentation improvements, and code contributions.

---

## 📌 Quick Start

1. **Fork** this repository
2. **Clone** your fork locally:
   ```bash
   git clone https://github.com/YOUR_USERNAME/tree-detector.git
   cd tree-detector
   ```
3. **Set up the project:**
   ```bash
   uv sync  # install dependencies using uv
   pre-commit install  # enable code formatting checks
   ```

4. **Create a branch:**
   ```bash
   git checkout -b feature/my-new-feature
   ```

5. **Make your changes**, with proper docstrings, typing, and tests.

6. **Run tests and lint checks:**
   ```bash
   pytest
   pre-commit run --all-files
   ```

7. **Commit and push:**
   ```bash
   git commit -m "feat: Add my new feature"
   git push origin feature/my-new-feature
   ```

8. **Open a pull request (PR)** to the `main` branch from GitHub. Describe what your PR adds/changes and reference related issues if any.

---

## ✅ What You Can Contribute

Here are some ideas:

| Type | Examples |
|------|----------|
| 🐛 Bug fixes | Fix crashes, tracking bugs, or model inconsistencies |
| 🚀 Features | Add model support (e.g. YOLOv12), dataset loaders, GUI extensions |
| 🧪 Testing | Add unit/integration tests for key modules |
| 🧹 Refactoring | Improve modularity, typing, or performance |
| 📚 Documentation | Improve README, add usage examples, tutorials |
| 🌍 Datasets | Scripts for converting new public tree datasets |

---

## 🔍 Code Style Guide

We use the following standards:

- **Formatting:** `black`
- **Imports:** `isort`
- **Linting:** `ruff`
- **Type checking:** `mypy` (optional but encouraged)
- **Tests:** `pytest`, minimum 85% coverage
- **Commits:** [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/)

Example commit message:
```bash
feat(inference): add support for USB cameras with device ID
```

---

## 🧪 Running Tests

```bash
pytest
```

Tests are organized in the `/tests` directory and mirror the structure of the core modules.

---

## 💬 Opening Issues

Use the [Issues tab](https://github.com/yourusername/tree-detector/issues) to report bugs or request features.

When opening an issue, include:

- A clear title
- Steps to reproduce (if a bug)
- Expected vs. actual behavior
- Any logs, screenshots, or video clips (if applicable)

---

## 🙌 Community Guidelines

Please be respectful and inclusive. By participating, you agree to follow our [Code of Conduct](CODE_OF_CONDUCT.md).

---

## 🛠️ Maintainers

This project is actively maintained by:

- [Your Name](https://github.com/yourusername)
- [Contributors](https://github.com/yourusername/tree-detector/graphs/contributors)

---

## 💡 Tips

- Start with issues labeled **"good first issue"**
- Ask questions freely in Discussions (coming soon!)
- PRs are welcome even if not perfect — we'll help refine them!

---

Thank you for contributing! 💚

