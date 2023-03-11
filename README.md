# vscode-cmake

Generic template to run C++ projects in vscode using cmake.

## Requirements 

- `Linux C++ compiler`
- `Linux C++ debugger`
- `CMake v3.2+`
- `CCache`

## Defaults

- Executable name: `app`
- Compiler: `gcc`
- Debugger: `gdb`
- C++ verstion: `std=c++17`
- Warnings: All seen as errors (`-Werror`)

## Keybindings

Change the `keybindings.json` of vscode with: 

```json
[
    {"key": "f6",
        "command": "workbench.action.tasks.runTask",
        "args": "normalRun"
    },
    {"key": "f4",
        "command": "workbench.action.tasks.runTask",
        "args": "cleanTask"
    },
]
```
