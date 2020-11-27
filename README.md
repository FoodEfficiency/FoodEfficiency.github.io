# FoodEfficiency.github.io
Public home page

## GitHub Pages

Open [GitHub](https://github.com) in browser and log in.

Find `User` - `Your organizations' and click `New organization`.  Create new organization `FoodEfficiency`, then invite other members and maybe also select `Settings` to finish creation.

Select `+` - `New repository` and create a public repository named `FoodEfficiency.github.io` as public workspace for the public home page; maybe including README, `.gitignore` and License (MIT) files.

Select Settings on repository to select template or set custom domain.

Now clone the repository to get started:

    cd Work
    git clone https://github.com/FoodEfficiency/FoodEfficiency.github.io
    cd FoodEfficiency.github.io

## Use Jekyll to build static site

### Prepare ...

Lock to latest Ruby version

```sh
cd ~/Work/FoodEfficiency.github.io
asdf install ruby 2.7.1
asdf local ruby 2.7.1
git add .tool-versions
git commit -m "Lock Ruby version using asdf"
```

### Prepare Gemfile for Jekyll install

```sh
# mkdir docs
bundle init
echo 'gem "jekyll", "~> 3.9.0"' >> Gemfile
bundle install
git add Gemfile*
git commit -m "Initial Gemfile"
```

### Initialize Jekyll site

```sh
bundle exec jekyll new . --force # will fail as Gemfile changed
bundle install
bundle exec jekyll new . --force
git add .
git commit -m "Jekyll new"
```

Add github-pages gem dependency to `Gemfile` and comment out jekyll gem, then run bundle install again

    # gem "jekyll", "~> 3.9.0"
    # gem "github-pages", group: :jekyll_plugins
    gem "github-pages", "~> 209", group: :jekyll_plugins

```
rm Gemfile.lock # conflicting versions og gem "rouge"
bundle install
git add .
git commit -m "Add github-pages gem"
```

### Test GitHub Pages site locally with Jekyll

Run Jekyll site locally

    bundle exec jekyll serve
    open http://localhost:4000

This will generate the static site and start a webserver on port 4000.
