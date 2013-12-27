# Dependencies

* Install Xcode [**Command Line Tools**](https://developer.apple.com/downloads/index.action?name=for%20Xcode%20-):
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

Restart your shell or call `source ~/.bash_profile` to reload your profile.

Finally, do:

* `rbenv install 2.1.0`
* `rbenv global 2.1.O`

## rbenv explanation

rbenv is a ruby utility that allows you to have multiple ruby versions on a system. It's especially useful to have a development environment that is exactly the same as your production platform. Moreover, on Mac OS X, it is also used to bypass the default system Ruby installation. We use Bundler with rbenv to have local gems for a project.

**DO NOT USE** the default system installation of Ruby. Indeed, OSX needs ruby (and some gems) for certain tasks. If you override a gem, it may conflict with the system. That's why it's better to set another global ruby installation.

[More info here](https://github.com/sstephenson/rbenv).

### Install a Ruby version

Type `rbenv install -l` to print a list of all available ruby versions.

Then, by executing `rbenv install x.x.x`, you will install the x.x.x version. You can list the installed versions with `rbenv versions`. The one with the * is the currently used version. You can set a global version with `rbenv global x.x.x` and a local one with `rbenv local x.x.x`.

Check the result with the `ruby -v` command.

**Each version has its own gems.**

### Ruby-build

Note that we had installed `ruby-build` along with `rbenv` when using `brew install rbenv ruby-build`. Ruby-build is a plugin for rbenv that allows us to install a ruby version with the `rbenv install` command, and automate a version uninstallation with the `rbenv uninstall` command.

### .ruby-version

When you call `rbenv local x.x.x`, it creates a `.ruby-version` file in your current folder. If you type `rbenv versions`, you can see that the currently set Ruby is not your global one.
