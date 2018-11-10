# About

## How to use

Build

```
bundle exec nanoc
```

Preview

```
bundle exec nanoc view
```

## How to deploy to GitHub Pages

1. First Time setup

```
% rm -rf output
% git clone . output
% cd output
output@master% git checkout --orphan gh-pages
output@gh-pages% git rm -rf .
output@gh-pages% git commit --m 'Create gh-pages branch' --allow-empty

output@gh-pages% git remote rm origin
output@gh-pages% git remote add origin repo-url
```

2. Subsequent deploy

*Do this from root directory, not output*

```
% bundle exec nanoc # build pages
% bundle exec nanoc deploy # deploy, that's it!
```
