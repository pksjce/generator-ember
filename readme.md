# Ember.js Generator [![Build Status](https://secure.travis-ci.org/yeoman/generator-ember.png?branch=master)](http://travis-ci.org/yeoman/generator-ember)

Maintainer: [Anthony Bull](https://github.com/inkredabull)


## Pre-reqs
 
First, this generator requires that Ruby and Compass are installed and in your path.

  `which ruby && which compass`

If you do not see two paths, follow [these instructions](https://github.com/gruntjs/grunt-contrib-compass#compass-task).

Second, if you have not installed yo yet via npm, do this:

  `npm install -g yo grunt-cli bower`

## Usage

After installing yo, execute these steps one after another:

- `npm install -g generator-ember`
- `mkdir webapp && cd webapp`
- `yo ember`
- `npm install -g grunt-mocha` 
- `grunt server`

A page with "Welcome to Ember.js" should appear in your browser.

## Generators

Available generators:

* ember 
* ember:view
* ember:controller
* ember:model

### ember

Creates the basic infrastructure for your app. 

### ember:view

Creates a view and template given an arg, as in

  `yo ember:view Foo`

__KNOWN ISSUE: IF YOU ADD A NEW VIEW, REGARDLESS OF WITH WHICH GENERATOR, YOU HAVE TO RESTART THE SERVER.__ 

### ember:controller

Creates a view, handlebar, controller and route given an arg, as in:

  `yo ember:controller Bar`

(and updates router.js, overwrite when prompted)

see: http://localhost:9000/#/bar

### ember:model

Creates a model, view, handlebar, controller, and route given an arg, as in: 

`yo ember:model Baz name:string postal_code:number`

see http://localhost:9000/#/baz
 
## Options

* `--skip-install`

  Skips the automatic execution of `bower` and `npm` after scaffolding has finished.

* `--test-framework=[framework]`

  Defaults to `mocha`. Can be switched for another supported testing framework like `jasmine`.

* `--coffee`

  Enable support for CoffeeScript.


## Troubleshooting

### `-bash: yo: command not found`

You need to make sure that npm is on your path.  Add the following to your .bash_profile (or .bashrc):

`PATH=/usr/local/share/npm/bin:$PATH`

### `You specified the templateName ... but it did not exist.`

You probably added a view; restart the server.

## History

### 0.5.0 (2013-07-13)

* Added basic scaffolding
* By default, include Ember Data

### 0.4.1 (2013-07-13)

* Reverted changes for testing improvement

### 0.4.0 (2013-07-11)

* Added testing improvement
* Upgraded to RC6
* Upgraded to grunt-contrib-compass 0.3.0

### 0.3.1 (2013-06-18)

* Added install step to address [PhantomJS issue](https://github.com/yeoman/generator-webapp/issues/92)

### 0.3.0 (2013-06-16)

* Upgraded to Ember 1.0 RC5
* Support for scaffolding out CoffeeScript via `--coffee`
* Support for jasmine as alternative test framework via `--test-framework`
* Automatic script inclusions via [`grunt-neuter`](https://github.com/trek/grunt-neuter)
* New prompt


## Credits

The Ember code is taken directly from the [1.0 RC6](https://github.com/emberjs/starter-kit/archive/v1.0.0-rc.6.zip)


## Contribute

See the [contributing docs](https://github.com/yeoman/yeoman/blob/master/contributing.md)

When submitting an issue, please follow the [guidelines](https://github.com/yeoman/yeoman/blob/master/contributing.md#issue-submission). Especially important is to make sure Yeoman is up-to-date, and providing the command or commands that cause the issue.

When submitting a bugfix, write a test that exposes the bug and fails before applying your fix. Submit the test alongside the fix.

When submitting a new feature, add tests that cover the feature.


## License

[BSD license](http://opensource.org/licenses/bsd-license.php)
