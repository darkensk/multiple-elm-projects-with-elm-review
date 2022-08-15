# Running `elm-review` inside each application

1. install `elm-review` dependency inside each package
2. init `elm-review` with template
3. specify `src` path inside `yarn review` script for each app
4. run `elm-review` from each package or from top level via workspaces

Third point is the tricky part since we want to run `elm-review` for each app individually. If we run it without limiting it to `src` folder only, it will go through all packages no matter which package it's ran from. However, when we specify `src` path, we'll recieve `NoUnused.Exports` errors since these functions are used out of scope.
