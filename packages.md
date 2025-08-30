---
title: Coffee Recipes
---


For each library or project that can be used we will have a separate directory
containing a `recipe.toml` file describing the project and how to transform it
so that it fits within the `coffee` structure.

The list of possible options of the `recipe.toml` file follows:

```
package.name = <text>
package.description = <text>
_package.version_ = <text>
_package.standard_ = <text>
_package.authors_ = <list of texts>
_package.readme_ = <filename>
_package.repository_ = <url>
_package.homepage_ = <url> 
package.license = <text>
_package.keywords_ = <list>
_package.transform_ = <code>

_dependencies.<package_name>_ = { version = "1.0" }

_bin.name_ = "rv"
bin.name = { name = "rv.o" , type = "lib" }
```
