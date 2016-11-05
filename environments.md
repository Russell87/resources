# Installing and Configuring my Development Environment

This guide walks through the configuration and tools to replicate my current development environment. It is current as of Mac OS X Sierra and on-going WIP.

### Tools
* [iTerm 2](https://www.iterm2.com/)
* [Atom Editor](https://www.atom.io)
* [oh-my-zsh](https://github.com/robbyrussell/oh-my-zsh)
* [Smyck](https://github.com/hukl/Smyck-Color-Scheme)
* [Homebrew](http://brew.sh/)
* [Cask](https://caskroom.github.io/)


### Homebrew

``
ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
``

### Cask
Extension of Homebrew used to install Mac OS X applications & binaries.

``brew tap caskroom/cask``

### Atom Editor
Open source text editor from Github

``brew cask install atom``

### RBENV
Used to manage Ruby versions

``brew install rbenv ruby-build``

Add to oh-my-zsh

``
echo 'if which rbenv > /dev/null; then eval "$(rbenv init -)"; fi' >> ~/.zshrc
``


``
source ~/.zshrc
``

### Ruby
``
rbenv install ruby 2.3.1
rbenv global 2.3.1
ruby -v
``

### Heroku Toolbelt
``
brew install heroku-toolbelt
``

Run ``heroku login`` to install Heroku CLI

### Git: Installation
* Install
``brew install git``
* Verify
``git --version``

### Git: Configuration
* ``git config --global user.name "your-name"``
* ``git config --global user.email "your-email"``

### Git: Create, Commit, and Push
Create the repository.
* ``git init``

Create a README.
* ``touch README.md``

Check the status
* ``git status``

Add files
* ``git add .``

Commit the changes with a comment
* ``git commit -m "initial commit"``

Create a connection to the repository named origin
* ``git remote add origin https://github.com/username/repository-name.git``

Push the commit to master branch on origin repository
 * ``git push -u origin master``
