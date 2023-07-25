Last updated 25 Jul

# Cleanup & Jekyll local install
Followed these steps https://jekyllrb.com/docs/installation/macos/

For this to work, 
- first I had to clean up all previous ruby version managers, rvm and rbenv. 
- also had to reinstall xcode & the CLT latest versions
- also cleaned up all warnings in `brew doctor` and 
- cleaned up my .zshrc and $PATH to scrub all references to rvm and other old crap

After this, `ruby-install ruby` was able to compile latest ruby successfully & I could continue with the Jekyll guide linked above

# Setting Jekyll up with github

Followed this guide 
https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/creating-a-github-pages-site-with-jekyll#creating-your-site


# issue with jekyll serve

```
zitaorban@peyote xiple.blog % bundle exec jekyll serve
Configuration file: /Users/zitaorban/github/xiple.blog/_config.yml
To use retry middleware with Faraday v2.0+, install `faraday-retry` gem
            Source: /Users/zitaorban/github/xiple.blog
       Destination: /Users/zitaorban/github/xiple.blog/_site
 Incremental build: disabled. Enable with --incremental
      Generating... 
       Jekyll Feed: Generating feed for posts
  Liquid Exception: undefined method `untaint' for "Welcome to Jekyll!":String in /_layouts/post.html
jekyll 3.9.2 | Error:  undefined method `untaint' for "Welcome to Jekyll!":String
```


https://github.com/github/pages-gem/issues/752#issuecomment-812866834

May need to use ruby 2.7.4 to match what github pages uses?
couldn't run `bundle add webrick`, can't find gemfile even after `gem install webrick`

Actual issue I'm having is described here: https://github.com/jekyll/jekyll/issues/9231

I had to edit `.rb`s in /Users/zitaorban/.gem/ruby/3.2.0/gems/liquid-4.0.3/ (`Cmd Shift .` to open hidden folder in VSCode) to remove references to taint and untaint functions that are temporarily broken due to jekyll not updating their liquid dependency to higher version

Will have to revert these changes back by finding references to `FIXME` and reverting to original

# considered adding Persephone theme
https://github.com/erlzhang/jekyll-theme-persephone/blob/master/docs/layouts.md


# How to run / start up server
bundle exec jekyll serve --drafts