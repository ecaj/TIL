```shell
# install Homebrew
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

# install rbenv
brew install rbenv ruby-build

# Add rbenv to bash so that it loads every time you open a terminal
echo 'if which rbenv > /dev/null; then eval "$(rbenv init -)"; fi' >> ~/.bash_profile
source ~/.bash_profile

# Install Ruby
rbenv install 2.3.1
rbenv global 2.3.1
ruby -v

git config --global color.ui true
git config --global user.name username
ssh -T git@github.com

# install icu4c
brew install icu4c

# install gollum
gem install gollum
gem install github-markdown

# install pow
curl get.pow.cx | sh

```

## Reference
- [Personal Wiki using GitHub and Gollum on OS X](http://www.nomachetejuggling.com/2012/05/15/personal-wiki-using-github-and-gollum-on-os-x/)
- [Setup Ruby On Rails on macOS 10.12 Sierra](https://gorails.com/setup/osx/10.12-sierra)
- [GitHub | gollum installation](https://github.com/gollum/gollum/wiki/Installation)