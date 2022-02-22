# wyvern

Wyvern is a (planned) python-lookalike programming langauge that compiles to [wizard](https://wizard-lang.org).

Unlike python, though:
* Everything is immutable
* There are no side effects (all effects are managed)
* Instead of classes, there are interfaces
* Instead of objects, there are records
* Uses all of wizard's tooling
* Compiles to machine code via wizard
* Supports concurrency from the ground up

Unlike wizard, wyvern has a syntax that more closely resembles languages from the imperative and OO traditions, while semantically remaining pure and referentially integral. It does this by introducing familiar-looking language constructs that help the programmer to use functional features by re-framing them.

For example, variable shadowing allows workflows like this:

```
x = 1
x = x + 1
...
```

to be rendered semantically as:

``` clojure
(let [x 1]
  (let [x (+ x 1)]
    ...))
```

**Wyvern hasn't been started yet!**
