<h1 align="center">AtomicGo | cursor</h1>

<p align="center">

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

<a href="https://github.com/atomicgo/cursor/issues">
<img src="https://img.shields.io/github/issues/atomicgo/cursor.svg?style=flat-square" alt="Issues">
</a>

<a href="https://opensource.org/licenses/MIT" target="_blank">
<img src="https://img.shields.io/badge/License-MIT-yellow.svg?style=flat-square" alt="License: MIT">
</a>

</p>

---

<p align="center">
<strong><a href="#install">Get The Module</a></strong>
|
<strong><a href="https://pkg.go.dev/github.com/atomicgo/cursor" target="_blank">Documentation</a></strong>
|
<strong><a href="https://github.com/atomicgo/atomicgo/blob/main/CONTRIBUTING.md" target="_blank">Contributing</a></strong>
|
<strong><a href="https://github.com/atomicgo/atomicgo/blob/main/CODE_OF_CONDUCT.md" target="_blank">Code of Conduct</a></strong>
</p>

---

<p align="center">
  <img src="https://raw.githubusercontent.com/atomicgo/atomicgo/main/assets/header.png" alt="AtomicGo">
</p>

## Description

Package cursor contains cross-platform methods to move the terminal cursor in
different directions. This package can be used to create interactive CLI tools
and games, live charts, algorithm visualization and other updatable output of
any kind.

Special thanks to github.com/k0kubun/go-ansi which this project is based on.

## Install

```console
# Execute this command inside your project
go get -u github.com/atomicgo/cursor
```

```go
// Add this to your imports
import "github.com/atomicgo/cursor"
```

## Usage

#### func  Bottom

```go
func Bottom()
```
Bottom moves the cursor to the bottom of the terminal. This is done by
calculating how many lines were moved by Up and Down.

#### func  ClearLine

```go
func ClearLine()
```
ClearLine clears the current line and moves the cursor to it's start position.

#### func  Down

```go
func Down(n int)
```
Down moves the cursor n lines down relative to the current position.

#### func  DownAndClear

```go
func DownAndClear(n int)
```
DownAndClear moves the cursor down by n lines, then clears the line.

#### func  Hide

```go
func Hide()
```
Hide the cursor. Don't forget to show the cursor atleast at the end of your
application with Show. Otherwise the user might have a terminal with a
permanently hidden cursor, until he reopens the terminal.

#### func  HorizontalAbsolute

```go
func HorizontalAbsolute(n int)
```
HorizontalAbsolute moves the cursor to n horizontally. The position n is
absolute to the start of the line.

#### func  Left

```go
func Left(n int)
```
Left moves the cursor n characters to the left relative to the current position.

#### func  Move

```go
func Move(x, y int)
```
Move moves the cursor relative by x and y

#### func  Right

```go
func Right(n int)
```
Right moves the cursor n characters to the right relative to the current
position.

#### func  Show

```go
func Show()
```
Show the cursor if it was hidden previously. Don't forget to show the cursor
atleast at the end of your application. Otherwise the user might have a terminal
with a permanently hidden cursor, until he reopens the terminal.

#### func  StartOfLine

```go
func StartOfLine()
```
StartOfLine moves the cursor to the start of the current line.

#### func  StartOfLineDown

```go
func StartOfLineDown(n int)
```
StartOfLineDown moves the cursor down by n lines, then moves to cursor to the
start of the line.

#### func  StartOfLineUp

```go
func StartOfLineUp(n int)
```
StartOfLineUp moves the cursor up by n lines, then moves to cursor to the start
of the line.

#### func  Up

```go
func Up(n int)
```
Up moves the cursor n lines up relative to the current position.

#### func  UpAndClear

```go
func UpAndClear(n int)
```
UpAndClear moves the cursor up by n lines, then clears the line.

---

> [AtomicGo.dev](https://atomicgo.dev) &nbsp;&middot;&nbsp;
> with ❤️ by [@MarvinJWendt](https://github.com/MarvinJWendt) |
> [MarvinJWendt.com](https://marvinjwendt.com)
