# Rules

## Version

> Version is summary information about `Computer Program`,
> it follows format `major.minor.patch` where `major`, `minor` and `patch`
> is unsigned integer number, begin from zero

Example: `0.0.0`, `0.1.0`, `1.2.3`, `2.3.4`

## Major

> `major` represents for a  of life time of Computer Program and
> that life time is defines by human, depends on specific context

Example:

* `0.y.z` - research and development
* `1.y.z` - `0.y.z` CPI is stable enough to public for using and long term
  support
* `2.y.z` - an special CPI was found, detach from `1.y.z` to research and
  development, it is ok while `1.y.z` is still maintain and using
* `3.y.z` - `2.y.z` is stable enough to pulic for using and long term support

## Minor

> `minor` represents for `CPI` which corresponds with current `major`

Example:

* `x.0.z` has `CPI = {function-a}`
* `x.1.z` has `CPI = {function-a, function-c}`
* `x.2.z` has `CPI = {function-a, function-b, function-c}`

## Patch

> `patch` represents for `NCPI`

Example:

* `x.y.0` has `NCPI = {execution-time-60, bug-A, bug-B}`
* `x.y.1` has `NCPI = {execution-time-50, bug-A}`
* `x.y.2` has `NCPI = {execution-time-40}`

It is impossible to define full NCPI. For example, the `bugs`, we have no idea
it is existed unless it is occurs. So the main point of `patch` that shows
changes instead of define NCPI.

## Increase Major, Minor and Patch by a Unit

> Increase `major`, `minor` and `patch` by plus one to current value.

Example:

* `1.y.z` => `2.y.z` => `3.y.z` => ....
* `x.1.z` => `x.2.z` => `x.3.z` => ...
* `x.y.1` => `x.y.2` => `x.y.3` => ...

## Reset Minor and Patch on Major Increment

> On `major` increment, reset `minor` and `patch` to zero

Example: `0.y.z` => `1.0.0`

## Reset Patch on Minor Increment

> On `minor` increment, reset `patch` to zero

Example: `x.1.z` => `x.2.0`

## Delopment Term Support Version

> Even `major` represent for `DTS` - Delopment Term Support Version

Example: `0.x.y`, `2.x.y`, `4.x.y`

DTS is uses for programs which is in under under development. On this
versions, `CPI` is under researching and changing anytime without guarantee
for backward compatible with previous version.

## Increase Minor on Development Term Support Version

> On `DTS` version, `minor` must be increase if and only if `CFA` is applied
> to Computer Program, include: `create`, `delete`, `input-change`,
> `output-change`

Increment shows that `CPI` is changed and it is not guarantee to backward
compatible with previous versions. For example, upgrade from `x.1.z` to
`x.2.z` may be break all of program and require to rewrite few parts or all of
code.

## Long Term Support Version

> Odd `major` represents for `LTS` - Long Term Support is represent

Example: `1.x.y`, `3.x.y`, `5.x.y`

LTS is use for programs which is stable, need to reduces maintain cost while
new `CFI` can be added.

## Increase Minor on Long Term Suppport Version

> On `LTS` version, `minor` must be increase if and only if `CFA` are applied
> to Computer Program, include: `create`

Increment shows that just only new `PCFI` is add to `CPI` so new version is
guarantee for backward compatible with previous versions. For example, upgrade
from `x.1.z` to `x.2.z` does not requires to rewrite source code.

## Increase Patch

> `patch` must be increase if an only if `CFA` is applied to Computer Program,
> include: `implementation-change`

As a result, increase `patch` does not change `CFI` so it guarantee for
backward compatible with previous versions which has similar `marjor` and
`minor`.  For example, upgrade from `x.y.1` to `x.y.2` does not requires to
rewrite source code.

## First Version

> First version must be `0.1.0`

First version is `DTS` version, it shows that program under development, does
not ready to use in long term, does not support much and unstable.

## Jump from DST to next LTS

> On `DST` version, `major` must be increase if an only if `CFI` is freeze and
> implementation is stable

Example: After freeze `CFI` and massive tests on `0.y.z` then release `1.0.0`.

## Jump from LTS to next DST

> On `LTS` version, `major` must be increase if and only if `CFA` is applied
> to Computer Program include `remove`, `input-change`, `output-change`,
> special `create` where special `create` is defined by human

Example:

* There are an bad `CFI` which need to change then `1.x.y` jump to `2.0.0`
* A new `CFI` suppose to make big change of using program then `1.x.y` jump to
  `2.0.0`
