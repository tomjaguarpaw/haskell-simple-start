It's not completely obvious how to set up a simple build environment
to get started writing Haskell code.  This package is about as simple
as you can get whilst allowing you to write new modules and play with
them in the REPL.  It should work with Cabal 2.4 and 3.0.

```
% cabal v2-repl
Warning: The package list for 'hackage.haskell.org' is 16 days old.
Run 'cabal update' to get the latest list of available packages.
Resolving dependencies...
Build profile: -w ghc-8.0.2 -O1
In order, the following will be built (use -v for more details):
 - my-dummy-package-0.0.0.0 (lib) (first run)
Configuring library for my-dummy-package-0.0.0.0..
Preprocessing library for my-dummy-package-0.0.0.0..
GHCi, version 8.0.2: http://www.haskell.org/ghc/  :? for help
[1 of 2] Compiling MyModule         ( src/MyModule.hs, interpreted )
[2 of 2] Compiling My.Dotted.Module ( src/My/Dotted/Module.hs, interpreted )
Ok, modules loaded: My.Dotted.Module, MyModule.
*MyModule> import MyModule
*MyModule MyModule> myFunction 10
100
*MyModule MyModule> import My.Dotted.Module
*MyModule MyModule My.Dotted.Module> import Test.HUnit
*MyModule MyModule My.Dotted.Module Test.HUnit> runTestTT My.Dotted.Module.test
Cases: 1  Tried: 1  Errors: 0  Failures: 0
Counts {cases = 1, tried = 1, errors = 0, failures = 0}
```
