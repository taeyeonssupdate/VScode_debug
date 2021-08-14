# VScode_debug

The Debug profile for clang, clang++, gcc, g++, Java, python between macOS Windows.

## integrated terminal

```json
// launch.json
{
  "version": "87.87",
  "configurations": [
    {
      "name": "clang, clang++, gcc, g++",
      "type": "cppdbg", //DEBUG CONSOLE
      "preLaunchTask": "(tasks label name)"
    }
  ]
}
```

Type of cppdbg will appear in DEBUG CONSOLE<br>
For run in integrated terminal without <a href="https://github.com/formulahendry/vscode-code-runner"><img src="https://formulahendry.gallerycdn.vsassets.io/extensions/formulahendry/code-runner/0.11.5/1625846902825/Microsoft.VisualStudio.Services.Icons.Default" alt="Code Runner" width="36xp"/></a> use <a href="https://github.com/vadimcn/vscode-lldb"><img src="https://vadimcn.gallerycdn.vsassets.io/extensions/vadimcn/vscode-lldb/1.6.5/1624507502597/Microsoft.VisualStudio.Services.Icons.Default" alt="CodeLLDB" width="20xp"/></a> instead.

```json
// launch.json
{
  "version": "87.87",
  "configurations": [
    {
      "name": "clang, clang++, gcc, g++",
      "type": "lldb", // integrated terminal
      "preLaunchTask": "(tasks label name)"
    }
  ]
}
```
