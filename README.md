# SconsGD

This is experimental, it might not go anywhere.

Based on Scons Commit 32b4cc4932c378845da8891514c497eba86a6697

## Why

Here are some reasons, in no particular order that brought me to start experimenting with this:

- Less dependencies, less chance of breakage.
- The engine (Pandemoinum Engine) could be used to build itself. (It could even have some guis for customizing builds.)
- Since the way the engine works it's really easy to port methods one by one to native c++ code, which can potentially greatly increase compile speeds.
- No GIL, unlike in Python.
- Easier engine specific build optimizations, since the engine codebase could contain the tooling code.
- Weird features would be possible like the engine watching for file changes, and it could recompile files in the background.
- Maybe the c++ codebase could be edited from within the engine's own code editor. This in itself might not be that desirable, however why I think this might not be that bad of an idea, is that an engine specific code complete could be easily created, which wouldn't be nearly as resource hungry as something like clang-complete paired with vscode (Yes there are neovim, vim, emacs, but they all has the same issue to some degree. Also they are not that comfortable for some types of work, like codestyle refactorings). My issue with most of the simpler code complete solutions are Ref<>'s, they just cannot handle them properly.
- Also other optimizations could be added, more static typing, and also gdscript is easier to debug, and inspect than python (you need more tools to be installed, and you need more setup, more research etc).
- And last but not least more understanding for me of build environments.

On the negative side:

- It's more work, and more pain if some platform breaks something, or something new has to be added.
- Bootstrapping has to be possible, by either keeping the original build system intact, or making something simple.
- It can't optimize link speeds, and that takes the most time in a build.

All in all it can turn out to be a dumb idea, we will see. It will probably not be lost effort though in some way or another.
