# Running one elm-review from top level

1. Add "fake" `elm-json` with source directories setup to point towards each elm project 

```
    "source-directories": [
        "packages/oak/src",
        "packages/birch/src",
        "packages/maple/src"
    ],
```

2. Add `elm-review` as dependancy on the project
3. Init elm-review and add rules
4. run `elm-review` from top level

``` 
yarn elm-review
```
