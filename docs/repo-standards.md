# SeattleU WebOps Repository Standards

This document defines repository naming, structure, and development standards for the Seattle University Web Operations GitHub organization.

These standards ensure consistency across repositories and help maintain a scalable development environment as the WebOps ecosystem grows.

---

# Repository Naming Conventions

Repository names should clearly reflect their purpose and align with the WebOps architecture.

---

## TerminalFour Components

Each TerminalFour content type should have its own repository.

Naming format:

```
cms-t4-[content-type-id]-[component-name]
```

Example:

```
cms-t4-8084-program-faq
cms-t4-7279-accordion
```

Using the T4 Content Type ID ensures a direct relationship between the CMS configuration and the repository.

---

## Page Layout Repositories

Page layout repositories should follow this naming format:

```
cms-t4-[layout-id]-[layout-name]
```

Example:

```
cms-t4-6907517-su-website-2023-full-width
```

---

## Compiled Applications

Applications built outside the CMS should use descriptive names.

Example:

```
be-legendary-app
```

These repositories typically contain:

* source code
* build scripts
* compiled output used by CMS templates

---

## Platform Tools

Infrastructure or automation tools should describe their function.

Examples:

```
t4-api-toolkit
search-proxy
media-cli
cache-warmer
```

These repositories support the broader WebOps platform.

---

# Repository Structure

Most repositories should include the following basic structure:

```
README.md
.gitignore
src/ (if applicable)
docs/ (optional)
```

The README should describe:

* the repository purpose
* how it integrates with the WebOps platform
* basic development instructions

---

# Branching Strategy

Repositories should use the following branch structure.

Primary branch:

```
main
```

Feature development should occur in feature branches.

Example:

```
feature/program-faq-schema
feature/search-improvements
```

Hotfix branches may be used for urgent production fixes.

Example:

```
hotfix/navigation-bug
```

---

# Commit Message Format

Commit messages should follow a clear and consistent format.

Recommended format:

```
type(scope): description
```

Examples:

```
feat(faq): add structured data output

fix(layout): correct navigation rendering

docs: update cloning guide
```

Common commit types include:

```
feat
fix
docs
refactor
chore
```

---

# Repository Ownership

Repositories are maintained by the Seattle University Web Operations team.

Major architectural decisions should be documented within the repository or within the organization documentation.

---

# Design Principles

These standards support several key principles.

### Consistency

Repositories follow predictable naming patterns.

### Clarity

Repository purpose should be immediately obvious.

### Independence

Components and tools should be able to evolve independently.

### Scalability

The repository structure should support future platform growth.

---

# Maintained By

Seattle University
Web Operations Team
