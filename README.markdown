# UglifyJS TextMate Bundle

## Overview

A TextMate bundle which allows you to easily minify your JavaScript files using [UglifyJS](https://github.com/mishoo/UglifyJS) by Mihai Bazon.

## Usage

Select one or more files in the file drawer. 

![Selecting files to compress](https://github.com/nextmat/UglifyJS.tmbundle/blob/master/Support/images/multi_select.png?raw=true)

Use the shortcut (command-shift-u) or select from the bundle action menu at the bottom of your Textmate window.

![Running the compress command](https://github.com/nextmat/UglifyJS.tmbundle/blob/master/Support/images/running.png?raw=true)

A new file will be created with your files combined and minified.

## Installing the bundle

The bundle currently relies on [node.js](http://nodejs.org/) and the [UglifyJS npm package](https://github.com/mishoo/UglifyJS). If you need to install these, follow the instructions in the next section, then return here to install the bundle.

``` bash
mkdir -p ~/Library/Application\ Support/TextMate/Bundles/
cd ~/Library/Application\ Support/TextMate/Bundles/
git clone https://github.com/nextmat/UglifyJS.tmbundle.git UglifyJS.tmbundle
osascript -e 'tell app "TextMate" to reload bundles'
```

There are a couple of environment variables to set up in TextMate (menu) → Preferences → Advanced → Shell Variables

1: The directory of `node` and `uglifyjs` needs to be in your `PATH`. In most cases this is `/usr/local/bin` . You can verify the locations with:

    which node
    which uglifyjs

2: The bundle should auto-detect your `NODE_PATH`. If it can't and complains, you should add your `NODE_PATH` to TextMate’s environment variables.

## Installing the UglifyJS package

The bundle currently relies on the UglifyJS package, which runs on top of NodeJS. There are multiple ways to get this installed, but [Homebrew](http://mxcl.github.com/homebrew/) is an excellent choice.

    brew install node  # install nodeJS
    # install npm (node package manager)
	# npm command

## ToDo / Contributing

Planned improvements:

* Make bundle dependency-free by including UglifyJS and using Apple's built-in Webkit js intepreter
* More attractive result pages
* Interface improvements
* Add a command for updating to the latest version of the bundle from inside TextMate

I'll get to these as I can, if you feel so motivated I will happily accept patches!

## License

The UglifyJS.tmbundle is released under the MIT license.

Copyright (c) 2011 Matt Sanders

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