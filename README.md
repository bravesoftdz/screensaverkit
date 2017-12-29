
# ScreensaverKit

ScreensaverKit is a screensaver toolkit written in Delphi, that supports rapidly building screensavers for Windows platform.

![Main](screenshots/main.png)

### Features

* Supports building screensaver on Windows 10 platform
* Supports IE rendering engine
* Has customizable URL
* Has customizable splash background color and logo (default is total black)
* Multi monitor support (duplicates across all monitors)
* Hotkey binding to start screensaver (Achieved by accessing the screensavers settings, and clicking on create shortcut, which creates a desktop shortcut binded to the hotkey Ctrl+Alt+L)
* Cleaned up the settings screen
* Added an indefinite progress bar that reacts to url loading and error
* Support for JPG is added
* Mouse and keyboard detection to exit the screensaver has been optimized
* Made embedded IE chromeless (no scrollbars, no borders, no clickable content)
* Handled external changes to screensaver screen
* Fixes to screensaver mode (to Hide taskbar, full screen, etc)
* Single instance checks to disallow screensaver from running twice

### Requirements

* Windows 10
* Embarcadero Rad Studio XE8

### Prerequisites

Some demo examples utilizes modules from [Project JEDI](https://rometools.github.io/rome/), therefore you must have the following projects installed into your Delphi development environment.

* [JEDI Code Library](https://github.com/project-jedi/jcl/)
* [JEDI Visual Component Library](https://github.com/project-jedi/jvcl/)

<!--

### Installation

## Contributing

Please read [CONTRIBUTING.md](CONTRIBUTING.md) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags).

-->

## License

ScreensaverKit is licensed under the MIT License - see the [LICENSE](LICENSE.md) file for details.
