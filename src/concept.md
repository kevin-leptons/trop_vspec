# Concepts

## Computer Program

> `Computer Program` is set of Computer Functions `P = {f1, f2, ..., fn}`
> where `f1, f2,...` is Computer Functions

Example: `calculation = {sum-number, sub-number, mul-number, div-number}`

## Computer Function

> `Computer Function` is represents by `F = (T, I, O, M)` where `T` is
> identity of function, `I` is input, `O` is ouput and `M` is implementation

Example: `F = (sum-number, a, b, return a + b)`

## Computer Function Action

> `CFA` - Computer Function Action is on of `create`, `remove`, `ouput-change`,
> `input-change` and `implementation-change`

* `create` - add a new function
* `remove` - delete already existed function
* `output-change` - specification of ouput is changed
* `input-change` - specification of input is changed
* `implement-change` - implementation of function is changed

## Computer Function Interface

> `CFI` - Computer Function Interface is represents by `E = (T, I, O)` where
> `T` is identity of function, `I` is input and `O` is output

Example: `E = (sum-number, a, b)`

As showed, Computer Function Interface is Computer Function without `M` -
Implementation.

## Public Computer Function Interface

> `PCFI` - Public Computer Function Interface is `CFI`
> which is export to use by caller, where caller can be user or other program

## Computer Program Interface

> `CPI` - Computer Program Interface is set `R = {r1, r2,..., rn}`
> where `r1, r2...` is `PCFI`

Example:

* `API` - Application Program Interface represents for computer program using
  as library such as function calling or network communication.
* `CLI` - Command Line represents for computer program as commands on terminal
  device.
* `UI` - User Interface represents for computer program using as
  end-application via I/O devices such as monitor and mouse

## Non Computer Program Interface

> `NCPI` - Non Computer Program Interface is set of concepts which is not
> `CPI`

Example: `X = {function-implement, performance, security, bug}`
