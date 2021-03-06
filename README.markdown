# Lighting - Control LIFX lights from your Mac [![GitHub release](https://img.shields.io/github/release/tatey/Lighting.svg)](https://github.com/tatey/Lighting/releases/latest) [![GitHub license](https://img.shields.io/github/license/tatey/Lighting.svg)](https://raw.githubusercontent.com/tatey/Lighting/master/LICENSE.txt)

A Mac OS X widget for toggling LIFX lights on and off via the [LIFX HTTP API](http://api.developer.lifx.com/docs).

![Video recording of using the widget](Screenshot-Preview.gif)

*Note: This is not an official LIFX project. Built on top of [LIFXHTTPKit](https://github.com/tatey/LIFXHTTPKit).*

## Installation

Requires Mac OS X 10.10 Yosemite.

1. Download the [latest zip file](https://github.com/tatey/Lighting/releases/latest),
   extract the binary, and drag into your Application folder.
2. Open "Lighting.app" and login with your personal access token.
3. Open Notification Center and add the "Lighting" widget.

Alternatively, you can install via Homebrew-Cask (Thanks @jamesottaway).

    $ brew cask install lighting

## Development

First, you need the following system dependencies:

* Swift 1.3 (Xcode 6.4)
* Mac OS X 10.10 Yosemite
* [Carthage](https://github.com/Carthage/Carthage)

Then, install the ppplication dependencies:

    $ carthage bootstrap --platform Mac

Finally, build the "Main" or "Widget" target.

### Main target

The main target is responsible for configuring the access token. It notifies
the widget when the access token changes.

![](Screenshot-Main-Target.jpg)

1. Open Lighting.xcodeproj
2. Select "Main > My Mac"
3. Run

### Widget Target

The widget target implements a view controller conforming to `NCWidgetProviding`
for toggling lights on and off.

![](Screenshot-Widget-Target.jpg)

1. Open Lighting.xcodeproj
2. Select "Widget > My Mac"
3. Run
4. Pick "Widget Simulator" when prompted to run the application

## Copyright

Following files, directories and their contents are copyright [Webalys Limited](http://streamlineicons.com).
You may not reuse anything therein without purchasing a license:

* Main/Images.xcassets/logged-in-icon-success.imageset/Icons-48px.png
* Main/Images.xcassets/logged-in-icon-success.imageset/Icons-48px@2x.png

All other files and directories are copyright Tate Johnson and licensed under
the GPLv3 license. See [LICENSE](LICENSE.txt).
