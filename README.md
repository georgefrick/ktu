# ktu
a knowledge transfer site - I share what I learn in very brief notes.

# GO 

## Commands
* **go run** compiles and executes a program. 
* **go install** compiles packages and creates binary executable files or package archive files.

## Packages 
* `package mypackage`
* A package is a directory containing .go files.
* If a program is part of main package, then go install will create a binary file.
* If a program is not part of main package, a package archive file is created with go install command.
* Go exports a variable if a variable name starts with Uppercase.
* Variables not starting with an uppercase letter are private to the package.
* You can nest packages.

## Main Function
* `func main()`

## Init Function
* `func init()`
* Init function is called by Go when a package is initialized.
* Can have multiple init functions in a file or a package.
* Order of the execution is according to the order of declaration.
* If init functions accross a package, they are run in alphabetical file name order.

## Importing
* `import "mypackage"`
* `import (**alias** "mypackage" ...other imports on their own line)`
* Go first searches for package directory inside GOROOT/src directory.
* If not found in GOROOT/src, then it looks for GOPATH/src.
* Reference nested packages by providing relative path to nested package.
* an imported package is initialized only once per package

## Variables
* Top most scope is package scope.
* You are not allowed to re-declare global variable with same name in the same package.
* Variables must be declared and assigned in order.
* **When variables are defined in package scope, they are declared in initialization cycles.**

## Language
* _ is very important to know, it lets you assign things to nothing
