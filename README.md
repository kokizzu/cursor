<h1 align="center">AtomicGo | cursor</h1>

<p align="center">
<img src="https://img.shields.io/endpoint?url=https://atomicgo.dev/api/shields/cursor&style=flat-square" alt="Downloads">

<a href="https://github.com/atomicgo/cursor/releases">
<img src="https://img.shields.io/github/v/release/atomicgo/cursor?style=flat-square" alt="Latest Release">
</a>

<a href="https://codecov.io/gh/atomicgo/cursor" target="_blank">
<img src="https://img.shields.io/github/workflow/status/atomicgo/cursor/Go?label=tests&style=flat-square" alt="Tests">
</a>

<a href="https://codecov.io/gh/atomicgo/cursor" target="_blank">
<img src="https://img.shields.io/codecov/c/gh/atomicgo/cursor?color=magenta&logo=codecov&style=flat-square" alt="Coverage">
</a>

<a href="https://codecov.io/gh/atomicgo/cursor">
<!-- unittestcount:start --><img src="https://img.shields.io/badge/Unit_Tests-2-magenta?style=flat-square" alt="Unit test count"><!-- unittestcount:end -->
</a>

<a href="https://opensource.org/licenses/MIT" target="_blank">
<img src="https://img.shields.io/badge/License-MIT-yellow.svg?style=flat-square" alt="License: MIT">
</a>
  
<a href="https://goreportcard.com/report/github.com/atomicgo/cursor" target="_blank">
<img src="https://goreportcard.com/badge/github.com/atomicgo/cursor?style=flat-square" alt="Go report">
</a>   

</p>

---

<p align="center">
<strong><a href="#install">Get The Module</a></strong>
|
<strong><a href="https://pkg.go.dev/atomicgo.dev/cursor#section-documentation" target="_blank">Documentation</a></strong>
|
<strong><a href="https://github.com/atomicgo/atomicgo/blob/main/CONTRIBUTING.md" target="_blank">Contributing</a></strong>
|
<strong><a href="https://github.com/atomicgo/atomicgo/blob/main/CODE_OF_CONDUCT.md" target="_blank">Code of Conduct</a></strong>
</p>

---

<p align="center">
  <img src="https://raw.githubusercontent.com/atomicgo/atomicgo/main/assets/header.png" alt="AtomicGo">
</p>

<p align="center">
<table>
<tbody>
</tbody>
</table>
</p>
<h3  align="center"><pre>go get atomicgo.dev/cursor</pre></h3>
<p align="center">
<table>
<tbody>
</tbody>
</table>
</p>

<!-- gomarkdoc:embed:start -->

<!-- Code generated by gomarkdoc. DO NOT EDIT -->

# cursor

```go
import "atomicgo.dev/cursor"
```

Package cursor contains cross\-platform methods to move the terminal cursor in different directions. This package can be used to create interactive CLI tools and games, live charts, algorithm visualizations and other updatable output of any kind.

Works niceley with https://github.com/atomicgo/keyboard

Special thanks to github.com/k0kubun/go\-ansi which this project is based on.

## Index

- [func Bottom()](<#func-bottom>)
- [func ClearLine()](<#func-clearline>)
- [func ClearLinesDown(n int)](<#func-clearlinesdown>)
- [func ClearLinesUp(n int)](<#func-clearlinesup>)
- [func Down(n int)](<#func-down>)
- [func DownAndClear(n int)](<#func-downandclear>)
- [func Hide()](<#func-hide>)
- [func HorizontalAbsolute(n int)](<#func-horizontalabsolute>)
- [func Left(n int)](<#func-left>)
- [func Move(x, y int)](<#func-move>)
- [func Right(n int)](<#func-right>)
- [func SetTarget(w Writer)](<#func-settarget>)
- [func Show()](<#func-show>)
- [func StartOfLine()](<#func-startofline>)
- [func StartOfLineDown(n int)](<#func-startoflinedown>)
- [func StartOfLineUp(n int)](<#func-startoflineup>)
- [func TestCustomIOWriter(t *testing.T)](<#func-testcustomiowriter>)
- [func Up(n int)](<#func-up>)
- [func UpAndClear(n int)](<#func-upandclear>)
- [type Area](<#type-area>)
  - [func NewArea() Area](<#func-newarea>)
  - [func (area *Area) Clear()](<#func-area-clear>)
  - [func (area *Area) Update(content string)](<#func-area-update>)
- [type Writer](<#type-writer>)


## func [Bottom](<https://github.com/atomicgo/cursor/blob/main/utils.go#L9>)

```go
func Bottom()
```

Bottom moves the cursor to the bottom of the terminal. This is done by calculating how many lines were moved by Up and Down.

## func [ClearLine](<https://github.com/atomicgo/cursor/blob/main/cursor.go#L67>)

```go
func ClearLine()
```

ClearLine clears the current line and moves the cursor to it's start position.

## func [ClearLinesDown](<https://github.com/atomicgo/cursor/blob/main/utils.go#L71>)

```go
func ClearLinesDown(n int)
```

ClearLinesDown clears n lines downwards from the current position and moves the cursor.

## func [ClearLinesUp](<https://github.com/atomicgo/cursor/blob/main/utils.go#L64>)

```go
func ClearLinesUp(n int)
```

ClearLinesUp clears n lines upwards from the current position and moves the cursor.

## func [Down](<https://github.com/atomicgo/cursor/blob/main/cursor.go#L26>)

```go
func Down(n int)
```

Down moves the cursor n lines down relative to the current position.

## func [DownAndClear](<https://github.com/atomicgo/cursor/blob/main/utils.go#L41>)

```go
func DownAndClear(n int)
```

DownAndClear moves the cursor down by n lines, then clears the line.

## func [Hide](<https://github.com/atomicgo/cursor/blob/main/cursor.go#L62>)

```go
func Hide()
```

Hide the cursor. Don't forget to show the cursor at least at the end of your application with Show. Otherwise the user might have a terminal with a permanently hidden cursor, until they reopen the terminal.

## func [HorizontalAbsolute](<https://github.com/atomicgo/cursor/blob/main/cursor.go#L47>)

```go
func HorizontalAbsolute(n int)
```

HorizontalAbsolute moves the cursor to n horizontally. The position n is absolute to the start of the line.

## func [Left](<https://github.com/atomicgo/cursor/blob/main/cursor.go#L41>)

```go
func Left(n int)
```

Left moves the cursor n characters to the left relative to the current position.

## func [Move](<https://github.com/atomicgo/cursor/blob/main/utils.go#L47>)

```go
func Move(x, y int)
```

Move moves the cursor relative by x and y.

## func [Right](<https://github.com/atomicgo/cursor/blob/main/cursor.go#L36>)

```go
func Right(n int)
```

Right moves the cursor n characters to the right relative to the current position.

## func [SetTarget](<https://github.com/atomicgo/cursor/blob/main/cursor.go#L15>)

```go
func SetTarget(w Writer)
```

SetTarget allows for any arbitrary io.Writer to be used for cursor movement \(will not work on Windows\).

## func [Show](<https://github.com/atomicgo/cursor/blob/main/cursor.go#L55>)

```go
func Show()
```

Show the cursor if it was hidden previously. Don't forget to show the cursor at least at the end of your application. Otherwise the user might have a terminal with a permanently hidden cursor, until they reopen the terminal.

## func [StartOfLine](<https://github.com/atomicgo/cursor/blob/main/utils.go#L18>)

```go
func StartOfLine()
```

StartOfLine moves the cursor to the start of the current line.

## func [StartOfLineDown](<https://github.com/atomicgo/cursor/blob/main/utils.go#L23>)

```go
func StartOfLineDown(n int)
```

StartOfLineDown moves the cursor down by n lines, then moves to cursor to the start of the line.

## func [StartOfLineUp](<https://github.com/atomicgo/cursor/blob/main/utils.go#L29>)

```go
func StartOfLineUp(n int)
```

StartOfLineUp moves the cursor up by n lines, then moves to cursor to the start of the line.

## func [TestCustomIOWriter](<https://github.com/atomicgo/cursor/blob/main/cursor_test_linux.go#L9>)

```go
func TestCustomIOWriter(t *testing.T)
```

## func [Up](<https://github.com/atomicgo/cursor/blob/main/cursor.go#L20>)

```go
func Up(n int)
```

Up moves the cursor n lines up relative to the current position.

## func [UpAndClear](<https://github.com/atomicgo/cursor/blob/main/utils.go#L35>)

```go
func UpAndClear(n int)
```

UpAndClear moves the cursor up by n lines, then clears the line.

## type [Area](<https://github.com/atomicgo/cursor/blob/main/area.go#L11-L13>)

Area displays content which can be updated on the fly. You can use this to create live output, charts, dropdowns, etc.

```go
type Area struct {
    // contains filtered or unexported fields
}
```

### func [NewArea](<https://github.com/atomicgo/cursor/blob/main/area.go#L16>)

```go
func NewArea() Area
```

NewArea returns a new Area.

### func \(\*Area\) [Clear](<https://github.com/atomicgo/cursor/blob/main/area.go#L21>)

```go
func (area *Area) Clear()
```

Clear clears the content of the Area.

### func \(\*Area\) [Update](<https://github.com/atomicgo/cursor/blob/main/area.go#L29>)

```go
func (area *Area) Update(content string)
```

Update overwrites the content of the Area.

## type [Writer](<https://github.com/atomicgo/cursor/blob/main/utils.go#L78-L81>)

Writer is an expanded io.Writer interface with a file descriptor.

```go
type Writer interface {
    io.Writer
    Fd() uintptr
}
```



Generated by [gomarkdoc](<https://github.com/princjef/gomarkdoc>)


<!-- gomarkdoc:embed:end -->

---

> [AtomicGo.dev](https://atomicgo.dev) &nbsp;&middot;&nbsp;
> with ❤️ by [@MarvinJWendt](https://github.com/MarvinJWendt) |
> [MarvinJWendt.com](https://marvinjwendt.com)
