# UglifyJS TextMate Bundle

## Overview

A Textmate bundle which allows you to easily minify your javascript files using [UglifyJS]() by Mihai Bazon.

## Usage

Select one or more files in the file drawer and use the shortcut (command-shift-u) or select from the bundle action menu at the bottom of your Textmate window.

A new file will be created with your files combined and minified.

## Installing the bundle

The bundle currently relies on [NodeJS]() and the [UglifyJS npm package](). If you need to install these, follow the instructions in the next section, then return here to install the bundle.

    mkdir -p ~/Library/Application\ Support/TextMate/Bundles/
    cd ~/Library/Application\ Support/TextMate/Bundles/
    git clone git://github.com/nextmat/UglifyJS-tmbundle.git UglifyJS.tmbundle
    osascript -e 'tell app "TextMate" to reload bundles'

There are a couple of environment variables to set up in Textmate (menu) -> Preferences -> Advanced -> Shell Variables

1: The directory of `node` and and `uglifyjs` needs to be in your `PATH`. In most cases this is `/usr/local/bin` . You can verify the locations with:

    which node
    which uglifyjs

2: Add your `NODE_PATH` to the environment variables. Usually `/usr/local/lib/node` .

## Installing the UglifyJS package

The bundle currently relies on the UglifyJS package, which runs on top of NodeJS. There are multiple ways to get this installed, but homebrew is an excellent choice.

    brew install node  # install nodeJS
    # install npm (node package manager)
	# npm command

## Todo / Contributing

Planned improvements:

* Make bundle dependency-free by including UglifyJS and using Apple's built-in Webkit js intepreter
* More attractive result pages
* Interface improvements

I'll get to these as I can, if you feel so motivated I will happily accept patches!

## License
The UglifyJS.tmbundle is released under the MIT license.
Copyright 2011 Matt Sanders.

