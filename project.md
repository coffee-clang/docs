---
title: Design
---

We will try to imitate cargo as much as possible.

`coffee` follows an opinionated idea of how a project should be structured.

## Project structure

We describe below the standard structure of a project, where all directories and
files shown are mandatory, but the directories might be empty.

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
```

The `deps` directory contains a separate directory for each dependency.
Notice that each dependency might have some dependencies; in that case the
subdependencies are stored using a unique name that is also used to identify the
exported symbols. Such name is the hash of the concatenation of the dependency
path.

##  `Coffee.toml`

####  package.name = <text>

The name of the package.

`package.name = coffee`


package.description = <text>
package.license = <text>
_package.version_ = <text>
_package.standard_ = <text>
_package.authors_ = <list of texts>
_package.readme_ = <filename>
_package.repository_ = <url>
_package.homepage_ = <url> 
_package.keywords_ = <list>

_dependencies.<package_name>_ = { version = "1.0" }

_bin.name_ = "rv"
bin.name = { name = "rv.o" , type = "lib" }


