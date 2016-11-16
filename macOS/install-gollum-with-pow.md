## Installation
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

## Configuration
Clone a github repository
```shell
git clone https://github.com/ecaj/TIL ~/GitHub/TIL
```shell
Create and edit `config.ru` file
```
cd ~/GitHub/TIL
sudo vim config.ru
```
Add the following:
```ruby
require 'rubygems'
require 'gollum/app'

gollum_path = File.expand_path(File.dirname(__FILE__)) # CHANGE THIS TO POINT TO YOUR OWN WIKI REPO
wiki_options = {}
wiki_options[:live_preview] = true # Equivalent to --live-preview
wiki_options[:allow_uploads] = true # Equivalent to --allow-uploads
wiki_options[:per_page_uploads] = true # When :allow_uploads is set, store uploads under a directory named after the page, as when using --allow-uploads page

Precious::App.set(:gollum_path, gollum_path)
Precious::App.set(:default_markup, :markdown) # set your favorite markup language
Precious::App.set(:wiki_options, wiki_options)
run Precious::App


## Reference
- [Personal Wiki using GitHub and Gollum on OS X](http://www.nomachetejuggling.com/2012/05/15/personal-wiki-using-github-and-gollum-on-os-x/)
- [Setup Ruby On Rails on macOS 10.12 Sierra](https://gorails.com/setup/osx/10.12-sierra)
- [GitHub | gollum installation](https://github.com/gollum/gollum/wiki/Installation)