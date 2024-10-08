# pure 

[![license](https://custom-icon-badges.demolab.com/github/license/brckd/template?logo=law)](LICENSE.md)

A programming language with a pure syntax.

> [!WARNING]  
> This language is still WIP. The following sections are just a proposal and subject to change.

## Syntax

Pure uses forward polish notation, i.e. function names are followed by their arguments. Arguments are matched by the amount of return values a function provides.
```pure
let a int 1
let b int 2
let c add a b
```

Arguments are parsed depending on their type.
```
int 1
float 0.1
str "Hello!"
# "Comments are actually just expressions with no return value."
```

##  Variables

Variables make it possible to refer to a value and override it. They can only be accessed after the first assignment.
```pure
set a int 1
set a add a 1
```

## Aliases

Aliases make it possible to refer to a value, but not override it. Thus, they can only be set once. However, they can be accessed from anywhere.
```pure
let b a
let a int 1
```

## Functions

Functions can be declared by creating an anonymous function and creating an alias for it.
```pure
let inc fn a fn b
  set a add a b
```

## Type Guards

Type guards can be used to limit the types of a function's parameters. They can be any function that has a specific type of parameter types. Usually, all possible parameter types are inferred.
```pure
let inc fn a fn b
  num ref a
  num b
  set a add a b
```

## Types

### Atomic

- `ref`
- `int`
- `flt`
- `str`
- `fn`

## Compound

- `struct`
- `union`

## Monads

- `opt`
- `res`
