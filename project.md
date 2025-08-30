---
title: Design
has_children: true
nav_order: 1
---

We will try to imitate cargo as much as possible.

`coffee` follows an opinionated idea of how a project should be structured.

# Project structure

We describe below the standard structure of a project, where all directories and
files shown are mandatory, but the directories might be emtpy.

```
/
├── deps/                 # External dependencies
├── src/                  # Main source code
│   └── Makefile          # Build configuration
├── test/                 # Testing assets
│   ├── unit/             # Unit tests
│   ├── integration/      # Integration tests
│   └── configs/          # Sample TOML configurations
└── build/                # Build artifacts (generated)
    ├── bin/              # Compiled binaries
    └── obj/              # Intermediate object files
Coffee.toml


