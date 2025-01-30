# inucat.github.io

GitHub Pages repo

To test locally, run:

```sh
bundle install
bundle exec jekyll serve
```

## Starting from Ruby setup

### macOS

```sh
brew install rbenv
rbenv install -l
rbenv install 3.4.1
rbenv init
```

### Debian

```sh
git clone https://github.com/rbenv/rbenv.git ~/.rbenv
~/.rbenv/bin/rbenv init

# Re-login or opening a new terminal may be required.
# Sourcing the start up file shown can be enough. For Debian:
#   . ~/.bash_profile
# In a new or sourced shell:
git clone https://github.com/rbenv/ruby-build.git "$(rbenv root)"/plugins/ruby-build
rbenv install -l
rbenv install 3.4.1
rbenv global 3.4.1
```
