# Seattle University WebOps Enterprise Architecture

This document describes the repository architecture used for the Seattle University Web Operations GitHub Enterprise organization and local development environment.

The goal of this structure is to clearly separate:

* CMS artifacts
* compiled applications
* platform tooling
* internal documentation

This ensures the WebOps ecosystem remains organized, scalable, and maintainable as the number of repositories grows.

---

# Root Architecture

```
enterprise/webops
├── .github
├── cms
│   └── t4
│       ├── components
│       ├── pagelayout
│       └── compiled-apps
├── platform
└── docs
```

---

# CMS Layer

The CMS directory contains repositories that directly support the TerminalFour CMS.

```
cms/t4
```

This layer contains:

* T4 Content Type components
* Page Layout templates
* compiled applications integrated into the CMS

---

# Components

Each TerminalFour Content Type is stored in its own repository.

Example:

```
cms/t4/components
├── cms-t4-7279-accordion
└── cms-t4-8084-program-faq
```

### Naming Convention

```
cms-t4-[content-type-id]-[component-name]
```

Example:

```
cms-t4-8084-program-faq
```

This ensures repositories map directly to their T4 Content Type IDs.

---

# Page Layout

Page Layout templates used by the CMS are stored here.

Example:

```
cms/t4/pagelayout
└── cms-t4-6907517-su-website-2023-full-width
```

---

# Compiled Applications

Applications compiled outside the CMS and injected into TerminalFour.

These typically include Vue, JavaScript, or other frontend applications.

Example:

```
cms/t4/compiled-apps
└── be-legendary-app
```

These repositories contain:

* source code
* build scripts
* compiled output deployed into CMS templates

---

# Platform

The platform directory contains infrastructure tools used by the WebOps team.

Example:

```
platform
├── t4-api-toolkit
├── search-proxy
└── media-tools
```

These tools support:

* CMS automation
* API integrations
* search infrastructure
* media management workflows

---

# Documentation

Internal WebOps documentation is stored in:

```
docs
```

Examples include:

* architecture documentation
* repository standards
* cloning instructions
* development workflows

Keeping documentation inside the architecture repository ensures it evolves with the platform.

---

# Design Principles

This architecture follows several guiding principles:

### Separation of Concerns

Each repository represents a distinct system component.

### Repository Independence

Components and tools can evolve independently.

### Scalability

New repositories can be added without restructuring the system.

### Clarity

Repository names clearly describe their purpose.

---

# Maintained By

Seattle University
Web Operations Team
