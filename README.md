# About

## How to use

Build

```
bundle exec nanoc
```

Preview

```
bundle exec view
```

## How to deploy with GitHub Pages

Source [nanoc.ws/doc/](https://nanoc.ws/doc/deploying/#with-git)

* Disable .git pruning
Make sure `.git` is excluded in `prune` in `nanoc.yml`

```
prune:
  auto_prune: true
  exclude: [ '.git' ]
```

* Setup github pages

```
% rm -rf output
% git clone . output
% cd output
output@master% git checkout --orphan gh-pages
output@gh-pages% git rm -rf .
```

* Push `gh-pages` branch manually

```
output@gh-pages% git remote rm origin
output@gh-pages% git remote add origin repo-url
```
