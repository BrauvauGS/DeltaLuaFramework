# DeltaLuaFramework

A reusable Lua framework for Delta DOP-100 HMIs, designed to make HMI scripting more structured, reusable, and comfortable to develop with Visual Studio Code.

## Features

- **Layer system:** Organize application logic into reusable layers.
- **LayerStack:** Manage layers and their lifecycle.
- **Signals:** Allow different parts of the application to communicate through signals.
- **DeltaTime:** Track elapsed time between updates.
- **VS Code autocompletion:** API definitions for Delta specific functions using Lua Language Server.
- **Lua 5.3:** Configured for the Lua version used by the target HMI.

## Requirements

- A compatible Delta DOP-100 HMI.
- Visual Studio Code.
- [Lua Language Server](https://github.com/LuaLS/lua-language-server), formerly known as sumneko.lua.
- Lua 5.3 runtime on the target HMI.

## Project Structure

```text
DeltaLuaFramework/
├── dop-api/
│   └── dop.lua
├── DeltaTime.lua
├── layer.lua
├── layerStack.lua
├── Main.lua
├── Signal.lua
├── .luarc.json
├── .gitignore
├── LICENSE
└── README.md
```

## VS Code Autocompletion

This project uses [Lua Language Server](https://github.com/LuaLS/lua-language-server), formerly known as sumneko.lua, to provide code completion, diagnostics, and language support in Visual Studio Code.

The `dop-api/dop.lua` file contains API definitions for Delta DOP-100 specific functions. These definitions allow Lua Language Server to recognize the Delta API and provide autocompletion while writing scripts.

The `.luarc.json` configuration adds the `dop-api` directory to the language server workspace library and configures Lua 5.3 as the target runtime.

### Setup

1. Install Lua Language Server in Visual Studio Code.
2. Open the `DeltaLuaFramework` project folder.
3. Make sure `.luarc.json` includes `./dop-api` in `workspace.library`.
4. Start writing your Lua scripts and use autocompletion for the Delta API functions covered by the definitions.

**Important:** The `dop.lua` file is intended exclusively for development tools. It does not implement Delta functions and must not be loaded or
