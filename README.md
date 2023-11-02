# Expandable notifications

This extension makes notification in the notification list expandable. 

## DISCLAIMER

This repository was originally posted on the [GNOME GitLab](https://gitlab.gnome.org/) page, however my account has been deleted there so this is a repost to make sure issues can still be created and the code can still be reviewed. Sadly, the history is missing due to this.

## Donations

I worked on this extension purely for my Bachelor's thesis, so I'm sorry if it's not well maintained. You can always motivate me through a [donation](https://ko-fi.com/kaanginam), but it's really not a necessity!

When there is something urgent (like a GNOME shell version change), you may also feel free to contact me on [twitter](https://twitter.com/kaanginam).

## Requirements

Please make sure to use the appropriate extension version when using certain gnome-shell versions! Otherwise there are no requirements.

## Installation

The extension can be installed through the [GNOME Shell extension page](https://extensions.gnome.org/extension/4463/expandable-notifications/), or by moving the extension folder in this repository to ~/.local/share/gnome-shell/extensions. 

## What exactly does it do?

Expanding a notification means displaying its full description and its actions. Usually, in the notification list, only 1 line of the description is displayed and no actions are possible to be taken.

There are 3 modes available:
- AUTO
- ARROW
- CRITICAL (default)

The *AUTO* mode expands every notification in the notification list. They cannot be unexpanded again.

The *ARROW* mode adds an arrow to every notification in the notification list. This arrow allows the user to expand a notification by choice. Every notification in the list is expandable. After a notification is expanded, it can be unexpanded again.

The *CRITICAL* mode combines both of these modes. Notifications with critical urgency are expanded automatically. There is still an arrow added to the notification, so the user can unexpand it again. Any other notification acts the same as a notification in *ARROW* mode.

The default option is currently *CRITICAL*, but this is open to change. 

### Changing mode

You can change settings by using the `gsettings` command, here is an example:

```gsettings --schemadir ~/.local/share/gnome-shell/extensions/expandable-notifications@kaan.g.inam.org/schemas/ set org.gnome.shell.extensions.expandable-notifications-settings expand-mode AUTO```

Add any mode you wish to use at the end (in full caps).

## License
This is licensed under the GNU General Public License v3.0.
