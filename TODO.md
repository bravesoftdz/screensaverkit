
# TODO

* Add checkbox to enable/disable multi-monitor support
* Ability to override root registry path
* Ability to override default mouse movement trigger (5 pixels)
* Ability to define mode if single/mirroring/extend
* Main/Settings from registration by injection

# Inspiration

http://traccar.codeplex.com/site/search?query=screensaver&sortBy=Relevance&devStatus=4&licenses=|&refinedSearch=true
https://social.msdn.microsoft.com/Search/en-US?query=screensaver&pgArea=header&emptyWatermark=true&ac=4
http://www.gifsaver.io

----------------------------------------------------------------------------------------

https://support.microsoft.com/en-us/help/182383/info-screen-saver-command-line-arguments
https://msdn.microsoft.com/en-us/library/windows/desktop/ms646284(v=vs.85).aspx

Yes, but no example that I know of. A kiosk application only differs from a normal application in only a few areas. Nothing changes as far as how you develop the application.

1. Oversized controls. Typically, you use large controls and fonts for the interface. It makes things easier to read and use for all age groups.

2. Durability. You have to harden the application so it can stand up to potential abuse. This means using try...finally and try...except statements liberally. You have to trap all errors that would normally raise exceptions, and exit your application. By trapping the errors you ensure that the user is never kicked out to the operating system or browser.

3. Secure Hardware. This means you take the target device and put in into an enclosure that will prevent users from accessing hardware buttons and ports. Today I see iPads inside secure kiosk cases in many businesses. You can do an internet search for "kiosk case" to see the wide variety of options in this area. You have to pick what works best for your retail scenario.

4. Remote Servicing. If you can, build in a way to monitor, diagnose and restart the application. That way you do not have to be in front of the device to perform simple maintenance tasks.

I can see where IW would allow you more hardware choices than if you were to choose a VCL application. FireMonkey is also an option because it is cross-platform. With an IW application you will have to set high SessionTimeOut values, or do something else, to keep the application from timing out after long periods of inactivity. That would not be true with VCL or FireMonkey.
