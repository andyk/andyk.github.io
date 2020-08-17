I build this blog using jekyll and rbenv on MacOS.

Here is what I did today to setup ruby and jekyll on my macbook pro and macbook air so that I can publish my blog via github pages.

I followed instructions at:
* pages.github.com, and transitively at...
* https://help.github.com/en/github/working-with-github-pages/creating-a-github-pages-site-with-jekyll and ...
* https://jekyllrb.com/docs/installation/macos/

```
# Homebrew was already installed:

# copied commands below from https://jekyllrb.com/docs/installation/macos/

# Install rbenv and ruby-build
brew install rbenv

# Set up rbenv integration with your shell
rbenv init

# restart shell

# Checked the installation. saw green/ok
curl -fsSL https://github.com/rbenv/rbenv-installer/raw/master/bin/rbenv-doctor | bash

rbenv install 2.7.1
rbenv global 2.7.1
ruby -v
# returns ruby 2.7.1p83 (2020-03-31 revision a0c7c23c9c) [x86_64-darwin19]
# before running, the default MacOS ruby was installed 2.6.1something

# Then ran: echo 'export PATH="$HOME/.gem/ruby/2.7.0/bin:$PATH"' >> ~/.bash_profile

# restart shell again

#make sure gem is looking at right place for jekyll
gem env

gem install --user-install bundler 
gem install jekyll --version "=3.8.7"  # chose v3.8.7 because of https://pages.github.com/versions/ 

# make sure jekyll 3.8.7 is installed and available at commandline.
jekyll --version

# Created github repo called andyk.github.io

cd ~/Development
git clone git@github.com:andyk/andyk.github.io.git
cd andyk.github.io.git

# these created the skeleton of my website/blog.
jekyll new .

# Then i edited the ./Gemfile that was created per instructions in https://help.github.com/en/github/working-with-github-pages/creating-a-github-pages-site-with-jekyll.
# I documented my edits in comments in that file.
```
