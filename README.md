# Position Independent Python3

These python3 basement project is a collection of useful recipes and classes that can be
used by other projects. Most importantly it provides a python3 developer package
including a full portable python3 environment.

# Prerequisites

* The basement layer (https://github.com/BobBuildTool/basement)

# How to use

First you need to add the `pipython3` layer to your project. To do so add a
`layers` entry to `config.yaml`:

    bobMinimumVersion: "0.18"
    layers:
        - basement
        - pipython3

and then add this repository as submodule to your project:

    $ git submodule add https://github.com/BobBuildTool/pipython3.git layers/pipython3

To use all facilities of the python3 basement project you just need to inherit the `pipython3::rootrecipe`
class in your root recipe:

    inherit: [ "basement::rootrecipe", "pipython3::rootrecipe" ]

This will make your recipe a root recipe and already setup the sandbox with a
proper host toolchain. See the next chapter what tools and toolchains are readily
available.

# Provided tools

The following tools can be used by naming them in `{checkout,build,package}Tools`:

* pipython3
