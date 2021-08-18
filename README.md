This repo is a port of the Chrome legacy browser extension and plug-in to Firefox

---

*Goal*
Bounce the navigation back to Chrome whenever the user is trying to open a web
page that is meant to be opened in Chrome. It is meant to be a companion to the
Chrome Legacy Browser Support Extension to allow for seamless switching between
Chrome and IE.


*Implementation*
Internet Explorer:
The plug-in is implemented as an Internet Explorer Add-on, and is packaged in a
Windows installer. The installer adds a DLL to the user's machine and registers
the plug-in in the browser (Tools -> Manage Add-ons). Once installed, the Add-on
monitors navigation requests in IE and checks if the url is any of the
whitelisted ones to be opened in IE. If not it will close the tab that started
the navigation and reopen the url in Chrome.
