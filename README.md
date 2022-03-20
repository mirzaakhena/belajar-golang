# Learn Golang

## How to start your golang programming

1. create a `go mod`

```
$ go mod helloworld
```

2. create a go file named main.go

```
package main

import "fmt"

func main() {
  fmt.Println("hello world")
}
```

3. run the application

```
$ go run main.go
```

4. build the application

```
$ go build
```

5. run the application (standalone)

```
$ ./helloworld
```

6. install the application into os

```
$ go install
```

7. run the application (standalone)

```
$ helloworld
```

## How to Print to console

```
print
fmt.Printf("")
fmt.Println("")
fmt.Print("")
fmt.Sprint("")
```

```
fmt.Printf("%s %d %f %t %v\n", "Hello", 5, 3.142857, true, 10)
```

```
fmt.Printf("%10s", "hello")
```

```
fmt.Printf("%10d", 12)
```

```
fmt.Printf("%10.2f", 3.1428573242424223562)
```

```
x := fmt.Sprintf("%10.2f", 3.1428573242424223562)
fmt.Printf("%s\n", x)
```

## Data type, variable, constant, value assignment, assertion, and casting

```
int, string, float64, bool, []byte, func, struct, interface
```

assignment value

```
var x int
x = 4

var x int = 4

var x = int(4)

var x = 4

x := 4
```

constant

```
const x = "hello"
const y = 7
```

```
x := "abcdef"
fmt.Printf("%s\n", x[0])
fmt.Printf("%v\n", x[2:4])
fmt.Printf("%v\n", strings.HasPrefix(x, "a"))
fmt.Printf("%v\n", strings.HasSuffix(x, "f"))

var x = "kasur rusak"
fmt.Printf("%v\n", strings.Index(x, "a"))
fmt.Printf("%v\n", strings.LastIndex(x, "a"))

strings
strconv
time
```

## Looping

```
// forever
for {

}

// for while
i := 0
for i < 10 {
  i++
}

// for i
for i := 0; i < 10; i++ {

}

// for range
for k, v := range x {

}
```

```
break for exit from loop
continue to ignore the next statement but continue the loop
```

## Conditional

```
if 1+1 == 2 {

}

if 1+1 == 2 {

} else {

}

x := "senin"
if x == "senin" {

} else if x == "selasa" {

}

x := "senin"
if x == "senin" {

} else if x == "selasa" {

} else {

}

x := 5
switch x {
  case 1, 2:
  case 3:
  default:
}
```

## Array and Slice

array

```
var x [2]int

var x = [2]int{}

x := [2]int{}

```

slice

```
var x []int

var x = []int{}

x := []int{}

x = make([]int, 0)

append

```

## Map

```
x := map[string]int{}
x["hello"] = 3
delete

value, exist := x["apa"]

```

## Function

```
func Something()  {

}

func Something(x int) {

}

func Something(x int) string {
  return ""
}

func Something(x int) (string, float64) {
  return "", 3.7
}

x := func(x int) (string) {
  return ""
}
```

Accessing function

```
a, b := Something(23)

a, _ := Something(23)

_, b := Something(23)

_, _ := Something(23)

```

Variadic function

```
func Something(x... int)  {

}
```

Closure

```

func Something(a func())  {
  a()
}

func Something() func()  {
  return func() {}
}
```

# struct

```
type Something struct {
  Nama string `json:"nama"`
  Umur int    `json:"umur"`
}

```

# method

```
type Something struct {

}

func (x *Something) Hello() {

}

```

# interface

```
type Something interface {

}
```

# composition

```
type Onething struct {

}

type Something struct {
  Onething
}


type Onething interface {
  DoSomething()
}

type Something interface {
  Onething
}



```

# package

```
code layout and structure
public
private
```

# pointer

```
var x int = 10
var p *int = &x

fmt.Printf("%v", *p)

```

# go routine and channel

```
go func() {}

```

# other thing

```
interface{}
create your own type
casting
sorting
assertions

out of memory
accessing wrong data type
accessing index out of bound

```
