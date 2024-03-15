Last updated 25 Jul

# Install Brew, git & VSCode
[Download VSCode](https://code.visualstudio.com/)

[Install Homebrew](https://brew.sh/)

[Install git](https://git-scm.com/download/mac)
`brew install git`

Clone repo via VSCode git tab.

`gem install jekyll`


Followed guide at [Installing Jekyll for macOS](https://jekyllrb.com/docs/installation/macos/) from step 2 onwards.

```
brew install chruby ruby-install xz
ruby-install ruby 3.1.3 # wondering if I could have installed latest ruby 3.3.0
echo "source $(brew --prefix)/opt/chruby/share/chruby/chruby.sh" >> ~/.zshrc
echo "source $(brew --prefix)/opt/chruby/share/chruby/auto.sh" >> ~/.zshrc
echo "chruby ruby-3.1.3" >> ~/.zshrc 
ruby -v
gem install jekyll
cd FIXME-repo-folder
bundle install
```


# How to run / start up server
bundle exec jekyll serve --drafts