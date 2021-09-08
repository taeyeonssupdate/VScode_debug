# VScode Debug

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

### vscode extension

- <a href="https://marketplace.visualstudio.com/items?itemName=ms-vscode.cpptools"><img src="https://ms-vscode.gallerycdn.vsassets.io/extensions/ms-vscode/cpptools/1.5.1/1625825443917/Microsoft.VisualStudio.Services.Icons.Default" alt="C/C++" width="30xp"/></a>[C/C++](https://marketplace.visualstudio.com/items?itemName=ms-vscode.cpptools)

- <a href="https://marketplace.visualstudio.com/items?itemName=donjayamanne.python-extension-pack"><img src="https://donjayamanne.gallerycdn.vsassets.io/extensions/donjayamanne/python-extension-pack/1.6.0/1558116027906/Microsoft.VisualStudio.Services.Icons.Default" alt="Python Extension Pack" width="30xp"/></a>[Python Extension Pack](https://marketplace.visualstudio.com/items?itemName=donjayamanne.python-extension-pack)

- <a href="https://marketplace.visualstudio.com/items?itemName=vscjava.vscode-java-pack"><img src="https://vscjava.gallerycdn.vsassets.io/extensions/vscjava/vscode-java-pack/0.18.3/1628659034006/Microsoft.VisualStudio.Services.Icons.Default" alt="Java Extension Pack" width="30xp"/></a>[Java Extension Pack](https://marketplace.visualstudio.com/items?itemName=vscjava.vscode-java-pack)

- <a href="https://marketplace.visualstudio.com/items?itemName=vadimcn.vscode-lldb"><img src="https://vadimcn.gallerycdn.vsassets.io/extensions/vadimcn/vscode-lldb/1.6.5/1624507502597/Microsoft.VisualStudio.Services.Icons.Default" alt="CodeLLDB" width="30xp"/></a>[CodeLLDB](https://marketplace.visualstudio.com/items?itemName=vadimcn.vscode-lldb)

### macOS setup

#### Install ccommand line tools

```shell
xcode-select --install
```

#### Install HomeBrew

```shell
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

#### Install gcc compiler

```shell
brew install gcc
```
###### create alias to shellrc
bash:
```
echo 'alias gcc="/usr/local/bin/gcc-11"' >> ~/.bashrc 
echo 'alias g++="/usr/local/bin/g++-11"' >> ~/.bashrc 
```
zsh:
```
echo 'alias gcc="/usr/local/bin/gcc-11"' >> ~/.zshrc
echo 'alias g++="/usr/local/bin/g++-11"' >> ~/.zshrc 
```


#### Install JDK

```shell
brew install adoptopenjdk
```

#### Install python

```shell
brew install python
```

### Windows setup

#### GCC

- https://code.visualstudio.com/docs/cpp/config-mingw

1. [Download mingw-w64](http://mingw-w64.org/doku.php/download) >> [MingW-W64-builds](http://mingw-w64.org/doku.php/download/mingw-builds) remember Architecture: x86_64
2. add bin to PATH
3. reboot

#### python

- https://www.python.org/downloads/

#### JDK

- [OpenJDK 8 (LTS)](https://adoptopenjdk.net/)
