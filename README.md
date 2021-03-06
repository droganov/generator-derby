## Derby 0.6 generator [![Build Status](https://travis-ci.org/derbyparty/generator-derby.svg?branch=master)](https://travis-ci.org/derbyparty/generator-derby)

[Yeoman](http://yeoman.io) generator that scaffolds out a [Derby](http://derbyjs.com) 0.6 project.

[![NPM](https://nodei.co/npm/generator-derby.png?downloads=true)](https://nodei.co/npm/generator-derby/)

### Features

* Derby 0.6
* Express 4
* Pure JavaScript/CoffeeScript
* optional Jade
* optional Stylus
* optional Markdown
* optional Bootstrap 3
* optional Redis
* optional [derby-login](https://github.com/derbyparty/derby-login)
* optional [racer-schema](https://github.com/derbyparty/racer-schema)
* optional [bower](http://bower.io/) settings files

### Getting Started

- Install: `npm install -g yo`
- Install: `npm install -g generator-derby`
- Make a project dir: `mkdir myproject`
- Go into the dir: `cd myproject`
- Run: `yo derby` or `yo derby --coffee`

### Generators

#### `yo derby`
Create a new Derby project.

#### `yo derby app-name`
Create a new additional Derby app. Inside existing Derby-project (created by generator-derby).

#### `yo derby:mini`
Create a new mini javascript Derby-project based on `derby-starter`. This is 
useful for bug reports and simple experiments.

How to use:

- Make a project dir: `mkdir buggy`
- Go into the dir: `cd buggy`
- Generate: `yo derby:mini`
- Start: `npm start`
 
The created project has the very simple structure:

`index.js` - the very basic derby-app.
`index.html` - html-file for the app.
`server.js` - bootstraping server-part

Note: you should have `mongo` and `redis` installed (At the moment `derby-starter`
required `redis`, so make sure you have it).  

#### `yo derby:component component-name`
Creates a [Derby component][] inside current folder.

Run inside of an project (created with `yo derby`) in the `/components/` folder, the new component will
be put into `/components/<component-name>`.

Run with name started with `d-` prefix, the new component will be a new package, ready for
publishing to NPM.

The package and class name will be derived from the dashed name, f.e `d-new-comp`.

### Options

* `--skip-install`

  Skips the automatic execution of `npm` after scaffolding has finished.

* `--coffee`

  Add support for [CoffeeScript](http://coffeescript.org/).
  
#### Notes
If you use redis in your derby-project take into account REDIS_URL is in the 
format: `redis://[db-number[:password]@]host:port[?option=value]` see 
[redis-url](https://github.com/ddollar/redis-url)  

To debug you app in the browser console use: `APP` and `MODEL` global variables.
  
## MIT License
Copyright (c) 2015 by Artur Zayats

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.

[Derby component]: https://github.com/codeparty/derby/blob/master/docs/guides/components.md
