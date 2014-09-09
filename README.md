# Myapp

This README outlines the details of collaborating on this Ember application.

A short introduction of this app could easily go here.

## Prerequisites

You will need the following things properly installed on your computer.

* [Git](http://git-scm.com/)
* [Node.js](http://nodejs.org/) (with NPM) and [Bower](http://bower.io/)

## Installation

First of all install the Node

* `sudo apt-get install nodejs`

Then Run

* `node -v`

```
$ node -v

v0.11.11

$ npm -v

1.3.25

```

### NVM Install script

To install you could use the [install script][2] using cURL:

    curl https://raw.githubusercontent.com/creationix/nvm/v0.15.0/install.sh | bash

or Wget:

    wget -qO- https://raw.githubusercontent.com/creationix/nvm/v0.15.0/install.sh | bash

<sub>The script clones the nvm repository to `~/.nvm` and adds the source line to your profile (`~/.bash_profile`, `~/.zshrc` or `~/.profile`).</sub>

You can customize the install source, directory and profile using the `NVM_SOURCE`, `NVM_DIR` and `PROFILE` variables. Eg: `curl ... | NVM_DIR=/usr/local/nvm bash` for a global install.

<sub>*NB. The installer can use Git, curl, or wget to download NVM, whatever is available.*</sub>

### Manual install

For manual install create a folder somewhere in your filesystem with the `nvm.sh` file inside it.  I put mine in a folder called `nvm`.

Or if you have `git` installed, then just clone it:

    git clone https://github.com/creationix/nvm.git ~/.nvm

To activate nvm, you need to source it from your shell:

    source ~/.nvm/nvm.sh

I always add this line to my `~/.bashrc`, `~/.profile`, or `~/.zshrc` file to have it automatically sourced upon login.
Often I also put in a line to use a specific version of node.


`nano ~/.bashrc`

and paste `source ~/.nvm/nvm.sh` anywhere is file `ctr+x` save.

`nano ~/.profile`

and paste `source ~/.nvm/nvm.sh` anywhere is file `ctr+x` save.


## Usage

You can create an `.nvmrc` file containing version number in the project root directory (or any parent directory).
`nvm use`, `nvm install`, `nvm exec`, and `nvm run` will all respect an `.nvmrc` file.

To download, compile, and install the latest v0.10.x release of node, do this:

    nvm install 0.10

And then in any new shell just use the installed version:

    nvm use 0.10

Or you can just run it:

    nvm run 0.10 --version

Or, you can run any arbitrary command in a subshell with the desired version of node:

    nvm exec 0.10 node --version

If you want to see what versions are installed:

    nvm ls

If you want to see what versions are available to install:

    nvm ls-remote

To restore your PATH, you can deactivate it.

    nvm deactivate

To set a default Node version to be used in any new shell, use the alias 'default':

    nvm alias default 0.10




* `git clone https://github.com/ahmadhasankhan/StartedEmber.git` this repository
* change into the new directory
* `npm install`
* `bower install`

## Running / Development

* `ember server`
* Visit your app at http://localhost:4200.

### Code Generators

Make use of the many generators for code, try `ember help generate` for more details

### Running Tests

* `ember test`
* `ember test --server`

### Building

* `ember build` (development)
* `ember build --environment production` (production)

### Deploying

Specify what it takes to deploy your app.

## Further Reading / Useful Links

* ember: http://emberjs.com/
* ember-cli: http://www.ember-cli.com/
* Development Browser Extensions
  * [ember inspector for chrome](https://chrome.google.com/webstore/detail/ember-inspector/bmdblncegkenkacieihfhpjfppoconhi)
  * [ember inspector for firefox](https://addons.mozilla.org/en-US/firefox/addon/ember-inspector/)

