# Hello World in GoLang

## References

* [gobyexample.com - hello world](https://gobyexample.com/hello-world)

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
ls -al
```

>     -rw-r--r--  1 45950  TCSD001\Domain Users       75 Jul 13 18:33 hello-world.go
>     -rwxr-xr-x  1 45950  TCSD001\Domain Users  2093200 Jul 13 18:34 hello-world

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
go get github.com/jmcmaster05/golang-hello-world
```
### Compile Binary to Bin

```
go install github.com/jmcmaster05/golang-hello-world
tree ~/go/bin | grep golang-hello-world
ls -al ~/go/bin | grep golang-hello-world
```

>     ├── golang-hello-world
>     -rwxr-xr-x  1 45950  TCSD001\Domain Users   2093200 Jul 17 11:56 golang-hello-world

### Execute Go Binary from Bin

```
golang-hello-world
```

>     hello world
