AutoFileName: Autocomplete Filenames in Sublime Text
=====================================================
Do you ever find yourself sifting through folders in the sidebar trying to remember what you named that file? Can't remember if it was a jpg or a png? Maybe you just wish you could type filenames faster. *No more.*

Whether you're making an `img` tag in HTML, setting a background image in CSS, or linking a `.js` file to your HTML (or whatever else people use filename paths for these days...), you can now autocomplete the filename. Plus, it uses the built-in autocomplete (<kbd>Ctrl</kbd><kbd>Space</kbd>), so no need to learn another *pesky* shortcut.

Installation
------------
You can manually clone this repo into Sublime Text's `Packages` directory (find it via `Preferences -> Browse Packages...`), but the easiest method is to [install](https://sublime.wbond.net/installation) and use [Package Control](https://sublime.wbond.net/). Hit <kbd>Ctrl</kbd><kbd>Shift</kbd><kbd>P</kbd> on Win/Lin, <kbd>⌘</kbd><kbd>Shift</kbd><kbd>P</kbd> on OSX, navigate to `Package Control: Install Package`, search for `AutoFileName` and you're all set!

Usage
-----
If you are looking to autocomplete an image path in an HTML `<img>` tag:
    <img src="../|" />

Pressing <kbd>Ctrl</kbd><kbd>Space</kbd> will activate AutoFileName.  A list of available files will be ready to select.

###*Looking for an even more automatic and seamless completion?*  

Add the following to your User Preferences file (`Packages/User/Preferences.sublime-settings` or `Preferences -> Settings - User`):
    
    "auto_complete_triggers":
    [
      {
         "characters": "<",
         "selector": "text.html"
      },
      {
         "characters": "/",
         "selector": "string.quoted.double.html,string.quoted.single.html, source.css"
      }
    ]

With this, there's no need to worry about pressing <kbd>Ctrl</kbd><kbd>Space</kbd>, autocompletion with appear upon pressing `/`.
