# security.filecoin.io

## Building Hugo

```
hugo -D
```

or to run a server

```
hugo server
```


## Pushing to gh-pages branch

The `public/` directory for the compiled site has been added to `.gitignore`.

You can create a local `dist/` folder, copy compiled contents to it, commit the folder then run:

```
git subtree push --prefix dist origin gh-pages
```

