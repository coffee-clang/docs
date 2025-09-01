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

####  package.name

The name of the package.
The value is a text.

`package.name = coffee`


#### package.description 

The description of the package.
The value is a text.


#### package.license 

The license of the package.
The value is a text, which can be a common abbreviation of a known license or
the text of the license


#### package.version

The version of the package.
The value is a text.

#### _package.standard_ 

The version of the C standard followed by the package.
The value is a text.

`package.standard = c23`

#### _package.authors_ = <list of texts>

The authors of the package.
The value is a text.

#### _package.readme_ = <filename>

The readme of the package.
The value is a text.

#### _package.repository_ = <url>

The repository of the package.
The value is an URL.

#### _package.homepage_ = <url> 

The homepage of the package.
The value is an URL.

#### _package.keywords_ = <list>

The keywords of the package.
The value is a text.

#### _dependencies.<package_name>_ = { version = "1.0" }

A dependency of the package.
The value is a JSON dictionary with the version of the required library.
The file contains a separate key for each dependency.

#### _bin.name_ = "rv"
#### bin.name = { name = "rv.o" , type = "lib" }

The version of the package.
The value is a text or a json dictionary with the `name` of the binary and its
`type`, that is the string `bin` or `lib`.

