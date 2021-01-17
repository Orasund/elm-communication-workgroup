# How to Contribute to Elm

## How to build and test a core package.

todo

## How to build the compiler?

```
; might need others also, but this is what I missed
$ sudo apt-get install ghc cabal-install
$ git clone https://github.com/elm/compiler.git
$ cd compiler
; not sure why this is needed, but without this worker is built instead of elm
$ rm -rf worker
$ cabal update
$ cabal new-build
$ cp dist-newstyle/build/x86_64-linux/ghc-8.4.4/elm-0.19.1/x/elm/build/elm/elm .
$ strip --strip-all elm
```
([source](https://discourse.elm-lang.org/t/communicating-about-elm-contributions/6729/48))

