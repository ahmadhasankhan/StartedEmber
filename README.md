# Myapp

This README outlines the details of collaborating on this Ember application.

A short introduction of this app could easily go here.

## Prerequisites

You will need the following things properly installed on your computer.

* [Git](http://git-scm.com/)
* [Node.js](http://nodejs.org/) (with NPM) and [Bower](http://bower.io/)

## Installation

First of all install the Node

* `sudo apt-get install node`
* `sudo apt-get install npm` 


After installing Node, verify that Node is set up correctly by typing the following commands on the command line. Both should output help messages:

```
$ node -v

v0.11.11

$ npm -v

1.3.25

```

```
sudo apt-get update
sudo apt-get install nodejs

sudo apt-get update
sudo apt-get install -y \
git \
build-essential \
curl \
wget
```


### NVM Install script

To install you could use the [install script][2] using cURL:

    curl https://raw.githubusercontent.com/creationix/nvm/v0.15.0/install.sh | bash

or Wget:

    wget -qO- https://raw.githubusercontent.com/creationix/nvm/v0.15.0/install.sh | bash

<sub>The script clones the nvm repository to `~/.nvm` and adds the source line to your profile (`~/.bash_profile`, `~/.zshrc` or `~/.profile`).</sub>

You can customize the install source, directory and profile using the `NVM_SOURCE`, `NVM_DIR` and `PROFILE` variables. Eg: `curl ... | NVM_DIR=/usr/local/nvm bash` for a global install.

<sub>*NB. The installer can use Git, curl, or wget to download NVM, whatever is available.*</sub>


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

###Ember CLI

Once you’ve installed Node, you’ll need to install the Ember CLI globally with:

`npm install -g ember-cli`

This will give you access to the ember command-line runner.


###Bower

You’ll need to install Bower, a package manager that keeps your front-end dependencies (including JQuery, Ember, and QUnit) up to date. This is as easy as running:

`npm install -g bower`

This will give you access to the bower command-line runner.


###PhantomJS

By default, your integration tests will run on PhantomJS. You can install via npm:

`npm install -g phantomjs`


###Create a new project

Run the generator for your project:
`ember new my-new-app`

This will create a new my-new-app folder and generate an application structure for you.

Once the generation process finishes, launch the app:
```
cd my-new-app
ember server
```

navigate to http://localhost:4200 to see your new app in action.

navigate to http://localhost:4200/tests to see your test results in action.


###Cloning an existing project

* `git clone https://github.com/ahmadhasankhan/StartedEmber.git` this repository
* change into the new directory
* `npm install`
* `bower install`
* `npm install broccoli-merge-trees`
* `npm install broccoli-static-compiler`


###Upgrading an Ember CLI App

Use NPM to update to the latest released version of Ember CLI.
`npm install --save-dev ember-cli`

When you update to the latest version you may need to re-install files from the app blueprint and update Node NPM dependencies.
`ember init`

This will re-copy files from the project blueprint. You can choose to overwrite existing files or not. It will subsequently call npm install to update any changed dependencies.

## Running / Development

* `ember server`
* Visit your app at http://localhost:4200.

###Stylesheets

Ember CLI supports plain CSS out of the box. You can add your css styles to app/styles/app.css and it will be served at assets/application-name.css
For example, to add bootstrap in your project you need to do the following:

```
bower install --save-dev bootstrap
            OR
bower install bootstrap --save
```


In Brocfile.js add the following:

```
app.import('bower_components/bootstrap/dist/css/bootstrap.css');
app.import('bower_components/bootstrap/dist/js/bootstrap.js');
```
it’s going to tell Broccoli that we want this file to be concatenated with our vendor.css file.


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

## Refrences
* ember: http://emberjs.com/
* ember-cli: http://www.ember-cli.com
* creationix/nvm:  https://github.com/creationix/nvm
