# VS Code Editor with Golang

**Table of Contents**
<!-- TOC -->

- [VS Code Editor with Golang](#vs-code-editor-with-golang)
    - [Install Go Extension](#install-go-extension)
    - [VS Code Shortcuts](#vs-code-shortcuts)
    - [Go Code Misc](#go-code-misc)
        - [var_dump](#var_dump)
        - [blank identifier](#blank-identifier)

<!-- /TOC -->

## Install Go Extension

[Go Programming in VS Code](https://code.visualstudio.com/docs/languages/go)

* Press `Cmd + Shift + x` to open the Extensions Sidebar
* Find and Install `Go (ms-vscode.go)` Extension

[Enable Go Auto Completion](https://github.com/Microsoft/vscode-go/wiki/Go-tools-that-the-Go-extension-depends-on)

* Press `Cmd + Shift + p` to open the Command Palette
* Enter `Go: Install/Update Tools`
* Select top checkbox to select all
* Select `Ok`

*Add Link in Go Source to Project Root for AutoComplete*

```
cd ~/go/src/link
PROJECT=golang-hello-world
ln -s ~/code/$PROJECT $PROJECT
unset PROJECT
tree -L 1 ~/go/src/link
```

>     └── golang-hello-world -> /Users/45950/code/golang-hello-world

## VS Code Shortcuts

[Key Bindings for Visual Studio Code](https://code.visualstudio.com/docs/getstarted/keybindings)

>     Cmd + k then Cmd + s

Toggle [Integrated Terminal](https://code.visualstudio.com/docs/editor/integrated-terminal)

>     Ctrl + `

Toggle Comments

>     Shift + Alt + a

## Go Code Misc

### var_dump

>     // var_dump
>     fmt.Printf("%+v\n", lines)

### blank identifier

>     // key, value
>     for i, line := range lines {
>       fmt.Println(i, line)
>     }

*use the blank identifier, an underscore, to discard the var*

>     for _, line := range lines {
>       fmt.Println(line)
>     }
