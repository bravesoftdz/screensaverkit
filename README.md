
# ScreensaverKit

![Main](screenshots/main.png)

## About

ScreensaverKit is a screensaver toolkit written in Delphi, that supports easily building screensavers for Windows platform.

## Features

* Multi monitor support (duplicates across all monitors)
* Provides hotkey binding internally
* Provides settings supports for options persistence
* Supports building screensavers for Windows 10 platform
* True screensaver mode (hide taskbar, full screen, etc.)
* Single instance checks to disallow screensaver from running more than once
* Mouse and keyboard detection to exit the screensaver has been optimized
* Handling external changes to screensaver screen(s)

## Demo features

* Supports IE rendering engine
* Customizable URL
* Customizable splash background color and logo (default is black without logo)
* Hotkey binding to start screensaver (Achieved by accessing the screensavers settings, and clicking on create shortcut, which creates a desktop shortcut binded to the hotkey Ctrl+Alt+L)
* An indefinite progress bar that reacts to normal and erroneous url loading
* Support for JPG logos
* Made embedded IE chromeless (no scrollbars, no borders, no clickable content)

### Prerequisites

The ScreensaverKit library has no external dependencies on third party libraries or frameworks.

But the demo examples utilize modules from [JCL](https://github.com/project-jedi/jcl) and [JVCL](https://github.com/project-jedi/jvcl), therefore you must have it installed into your Delphi development environment before attempting to run them.

## API
<!--
### Constructor

`TMaximalRectangle.Create(bound);`

| Names | Required | Type | Description
| --- | --- | --- | ---
| bound | `false` | `TRect` | bounding rectangle

### Properties

| Names | Description
| --- | ---
| Count | count of added obstacles
| Obstacles | returns an array of added obstacles
-->
### Methods

| Names | Description
| --- | ---
| `Screensaver.Initialize` | sets bounding rectangle
| `Screensaver.Run` | adds an obstacle

## Usage

The key difference between a ScreensaverKit based application, and a standard Delphi application is the usage of `Screensaver.Initialize` and `Screensaver.Run`. We do not reference or use `Application` or any of it's methods and variables.

Here is an example setup from one of the accompanied demo examples.

```delphi
program InternetScreensaver;

uses
  Main in 'Main.pas' {MainForm},
  Settings in 'Settings.pas' {SettingsForm},
  UNulContainer in 'UNulContainer.pas',
  IntfDocHostUIHandler in 'IntfDocHostUIHandler.pas',
  UContainer in 'UContainer.pas',
  ScreensaverKit in '..\..\src\ScreensaverKit.pas',
  ScreensaverKit.SettingUtils in '..\..\src\ScreensaverKit.SettingUtils.pas',
  ScreensaverKit.WebBrowserUtils in '..\..\src\ScreensaverKit.WebBrowserUtils.pas',
  ScreensaverKit.ShortcutUtils in '..\..\src\ScreensaverKit.ShortcutUtils.pas';

{$R *.res}
{$E scr}

begin
  Screensaver.Initialize;
  Screensaver.Run;
end.
```

Kindly notice the usage of the `{$E} ` compiler directive. This sets the compiled binary file to have a `SCR` extension, which is the default extension for Windows based screensavers. *Notice*: This can be commented, and when run within the Delphi IDE, a special screensaver debug mode will kick in.

<!--

### Installation

## Contributing

Please read [CONTRIBUTING.md](CONTRIBUTING.md) for details on our code of conduct, and the process for submitting pull requests to us.

## Versioning

We use [SemVer](http://semver.org/) for versioning. For the versions available, see the [tags on this repository](https://github.com/your/project/tags).

-->

## License

ScreensaverKit is licensed under the MIT License. See [LICENSE](LICENSE.md) for details.
