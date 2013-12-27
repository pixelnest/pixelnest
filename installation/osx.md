# Dependencies

* Install Xcode [**Command Line Tools**](https://developer.apple.com/downloads/index.action?name=for%20Xcode%20-) (last version available):
  1. Open Xcode
  2. Click on "File"
  3. Click on "Open Developer Tool"
  4. Click on "More Developer Tools"
  5. Connect with your Apple ID
  6. Download the last version of the "Command Line Tools" utility
* Install [Homebrew](http://brew.sh)

# Ruby

First, we need rbenv:

* `brew install rbenv ruby-build`

Open your bash profile (on OSX, it should be `~/.bash_profile`) and add at the end of the file:

* `eval "$(rbenv init -)"`
