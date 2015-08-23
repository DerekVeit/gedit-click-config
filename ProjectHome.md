## Description ##
This plugin provides configurable text selections based on single or multiple
left mouse button clicks, i.e.,
> single click, double click, triple click, quadruple click, quintuple click.

For example, a double click can be set to select names that include
underscores, or a quadruple click can be set to select a paragraph.

### Latest ###
**2012-07-12**
  * Version 1.4.0 is ready.  It is updated to run on gedit 3, but otherwise the functionality is the same.  Users of gedit 2 should still use 1.3.0, which is the last version for gedit 2.
  * I have redesigned the configuration GUI for assigning configurations to languages.  The drag-and-drop lists are gone.  Now clicking on Assign Languages shows a dialog suspiciously similar to the one in Class Browser 3g (thanks), which has a much more normal UI design.
  * Also for more normal UI design, the text entry boxes have been removed from the selector widgets (using GtkComboBox instead of GtkComboBoxEntry), so proper use of the Add button is more obvious.  No one complained, but I can't be the only one who found it a little tricky.

## Configuration ##
Regular expressions are used to specify types of text selections.  Several presets are included.  New selection types can be named and assigned to any of the left button clicks.

A set of selection type assignments for each of the five clicks can be saved with a name so that you can create different setups for different circumstances.  And you can assign a named configuration to any of the code languages that gedit detects so that Click Config will automatically use rules appropriate for each language.

![http://gedit-click-config.googlecode.com/files/Click_Config-1.4.0-configuration-screenshot.png](http://gedit-click-config.googlecode.com/files/Click_Config-1.4.0-configuration-screenshot.png)
![http://gedit-click-config.googlecode.com/files/Click_Config-1.4.0-Assign_Languages-screenshot.png](http://gedit-click-config.googlecode.com/files/Click_Config-1.4.0-Assign_Languages-screenshot.png)


The plugin also creates a submenu within gedit's Edit menu for accessing the
configuration window or directly making a selection.  This allows for hotkeys
to be set for any of the defined selections.

To modify menu shortcut keys, you may have to enable the feature.  In `gconf-editor`, navigate to /desktop/gnome/interface and check "can\_change\_accels".

Then, in gedit, while you have the menu item highlighted, press the hotkey combination you want to have assigned to it, or press Backspace to clear the hotkey assignment.

![http://gedit-click-config.googlecode.com/files/Click_Config-1.1-menu-screenshot.png](http://gedit-click-config.googlecode.com/files/Click_Config-1.1-menu-screenshot.png)

## Installation ##
  1. Download [Click\_Config-1.4.0.tar.gz](http://gedit-click-config.googlecode.com/files/Click_Config-1.4.0.tar.gz).
  1. Extract the files into your `~/.gnome2/gedit/plugins` or `~/.local/share/gedit/plugins` directory:
    * ![http://gedit-click-config.googlecode.com/files/Click_Config-1.1-files-screenshot.png](http://gedit-click-config.googlecode.com/files/Click_Config-1.1-files-screenshot.png)
  1. Restart gedit
  1. Activate the plugin in gedit Edit > Preferences > Plugins.

## Origin ##
  * Coding in Python, and wanting to follow the naming conventions of [PEP 8](http://www.python.org/dev/peps/pep-0008/).
  * Wanting to use gedit as my code editor but also easily select `underscore_names`.
  * Searching for an existing solution I found these thoughts:
    * Andrew Edwards on gedit-list suggested [using a configurable character set like in GNOME Terminal](http://mail.gnome.org/archives/gedit-list/2007-November/msg00036.html).
    * James Steward on [Ubuntu gedit Bug #413360](https://bugs.launchpad.net/ubuntu/+source/gedit/+bug/413360) suggested multiple selection types for single- double- triple- and quadruple- clicks. This is similar to behavior common in word processors.
    * Gregor Popović and Michael T on [GNOME Bugzilla Bug 500515](https://bugzilla.gnome.org/show_bug.cgi?id=500515) suggested making the configuration sensitive to the file type.

## Feedback and Support ##
Please use [the issues list](http://code.google.com/p/gedit-click-config/issues/list) to report bugs.
Use the [Click Config Google group](http://groups.google.com/group/click-config) to post questions, comments, or suggestions, etc.