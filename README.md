# Hello World in GoLang

## References

* [gobyexample.com - hello world](https://gobyexample.com/hello-world)

## Install GoLang

### Mac

```
brew install golang
```

```
cat << EOF >> ~/.profile
# --- Go ---
GOPATH="$HOME/go"
PATH=$GOPATH/bin:$PATH
EOF
```

## Create Repository

```
mkdir ~/code/golang-hello-world
```

```
cat << EOF > hello-world.go
package main

import "fmt"

func main() {
    fmt.Println("hello world")
}
EOF
```

```
git commit -m 'added hello world go script'
git remote add origin git@github.com:jmcmaster05/golang-hello-world.git
git push -u origin master
```

## Go Local Development

### Execute Go Script

```
time \
go run hello-world.go
```
>     hello world

_Execution Time 0m0.366s_

### Compile Go Binary to Working Directory

```
go build hello-world.go
ls -alh
```

>     -rw-r--r--   1 45950  TCSD001\Domain Users    75B Jul 17 11:46 hello-world.go
>     -rwxr-xr-x   1 45950  TCSD001\Domain Users   2.0M Jul 17 12:20 hello-world

### Execute Go Binary from Working Directory

```
time \
./hello-world
```

>     hello world

_Execution Time 0m0.013s_

## Go Get Deployment

### Add Repository to Go Path

```
go get -v github.com/jmcmaster05/golang-hello-world
```

>     github.com/jmcmaster05/golang-hello-world (download)

Repository must have at least one file with extension `.go` or the following error message will appear:

>     can't load package: package github.com/jmcmaster05/golang-hello-world:
>     no Go files in /Users/45950/go/src/github.com/jmcmaster05/golang-hello-world

```
cd ~/go/src/github.com/jmcmaster05/golang-hello-world
git log | head -n 5
```

>     commit 7ab9e6e434b393a02601f3f998f61e371455195f
>     Author: Joe McMaster <45950@dfw184016l.containerstore.com>
>     Date:   Tue Jul 17 12:08:44 2018 -0500
>         added install golang notes

### Compile Binary to Bin

```
go install github.com/jmcmaster05/golang-hello-world
tree ~/go/bin | grep golang-hello-world
ls -alh ~/go/bin | grep golang-hello-world
```

>     ├── golang-hello-world
>     -rwxr-xr-x  1 45950  TCSD001\Domain Users   2.0M Jul 17 12:18 golang-hello-world

### Execute Go Binary from Bin

```
golang-hello-world
```

>     hello world
