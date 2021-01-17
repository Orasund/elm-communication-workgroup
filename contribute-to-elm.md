# How to Contribute to Elm

## Which contribituions are welcome?

### Big Contributions

Don't try add any big contribution to any of the elm/* packages.

If you have an idea, try to implemented outside of elm/* and then write about it on discourse. Do not expect that idea to be included into elm.

Success stories:

[Making Dict 170% faster](https://groups.google.com/g/elm-dev/c/--fK-wMoDig/m/p6zF4-5sAgAJ?pli=1)

[Faster List.map](https://discourse.elm-lang.org/t/a-faster-list-map-for-elm/6721)

### Small Contributions

Regarding small contributions, add an issue to the corresponding elm/package. But don't expect it to be fixed any time soon. It may take up to 2 years.
A checklist for a good issue can be found [here](https://github.com/elm/expectations/blob/master/guidelines-for-issues.md).

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

