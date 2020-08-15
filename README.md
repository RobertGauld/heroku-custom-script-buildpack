# Heroku Custom Script Buildpack

A [heroku buildpack](http://devcenter.heroku.com/articles/buildpacks) for running custom scripts at the
compile and release stages of the build process.

## Usage

At least one of build/compile or build/release must be present.

```
heroku buildpacks:add --index @ https://github.com/robertgauld/heroku-custom-script-buildpack.git
```

```
echo -e "echo 'This is my compile script'" > build/compile
git add .sh; git commit -m 'Added compile script for heroku build'
git push
```

```
echo -e "echo 'This is my release script'" > build/release
git add .sh; git commit -m 'Added release script for heroku build'
git push
```
