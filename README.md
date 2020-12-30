Clone (use --recurse-submodules)

```
git clone --recurse-submodules GITHUB_URL
```

Check out a given branch (and the corresponding commits at each submodule)

```
git checkout --recurse-submodules --force BRANCH
```

Now you need to install, link and locally build the packages linked by lerna.

```
// install and link all npm packages
lerna bootstrap

// OPTION 1

    // EDIT LERNA.JSON: Remove the "linked-thougts" row, and then run
    lerna run build

    // ADD the line again to LERNA.JSON and then run the app
    cd linked-thoughts
    npm run dev

// OPTION 2

    // instead of `lerna run build`, use
    lerna run dev --parallel
```

If you work on a submodule and want to link to the working branch

```
TBW
```
