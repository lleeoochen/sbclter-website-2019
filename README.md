# SBC LTER website, 2019

## Installing jekyll on mojave:

followed instructions here:
https://desiredpersona.com/install-jekyll-on-macos/

Differences from high sierra instructions:
1. mojave does not install macOS SDK headers. 
2. use of sudo not recommended - better to put ruby in a user dir and set the path.
there is more on that page about managing multiple versions of ruby.

also might be useful info here
https://github.com/jekyll/jekyll-help/issues/73

### command history:

open /Library/Developer/CommandLineTools/Packages/macOS_SDK_headers_for_macOS_10.14.pkg
### <follow gui instructions >

### install homebrew (if you need it)
  /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

### install ruby
  brew install ruby
 
### check version
  ruby -v

### update bash profile with Ruby paths
  echo 'export PATH="/usr/local/opt/ruby/bin:$PATH"' >> ~/.bash_profile
  echo 'export PATH=$HOME/gems/bin:$PATH' >> ~/.bash_profile
  
### source it to relaunch terminal
   source ~/.bash_profile 

### check versions
  which ruby
  gem env
  
### install jekyll
   gem install bundler jekyll

### TO RUN JEKYLL:
cd bootstrap4-minimal
jekyll serve --incremental

### possible error, on Mac Mojave: "... Invalid US-ASCII character "\xE2" on line 6"
### run this cmd before jekyll serve:
export LANG=en_US.UTF-8