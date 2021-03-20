# My Bear Theme

I have created my own [Bear](https://bear.app/) theme, which is based on the  [D.Boring](bear://x-callback-url/change-theme?theme=D.Boring) theme and ~~a total rip-off from~~ inspired by the [iA Writer](https://ia.net/writer) the aesthetic. It uses:

- *iA Mono Writer Mono* of the open source [iA-Fonts](https://github.com/iaolo/iA-Fonts)
- A combination of the iA Writer color scheme, the original color scheme and some custom colours
- A huge font size because I'm blind 🤓

## Bear Doesn't Support Custom Themes

Unfortunately there is no official support for custom themes. Installing these themes could break your Bear installation. Also you'll have to re-install them after each update of the Bear App.

## Installation Using the `install` Script

First make sure you have the [iA Mono Writer Mono](https://github.com/iaolo/iA-Fonts/tree/master/iA%20Writer%20Mono/Static) installed. Then clone the the repo to your desired location and `cd` into it.

```
git clone https://github.com/lucaschultz/bear-theme.git
cd bear-theme
```

If you're lazy and have Bear installed in `/Applications` or `~/Applications` you can use the install script as is. It'll overwrite the [Dark Graphite](bear://x-callback-url/change-theme?theme=Dark%20Graphite), [D.Boring](bear://x-callback-url/change-theme?theme=D.Boring) and [Menlo](bear://x-callback-url/change-font?font=Menlo) Themes. Be sure use the `-b` option to backup the original theme/icon files:

```
sudo ./install -b
```

The script will create backups (an in-place copy of each respective original file in with appended `.bak` extension), copy the `.theme` and `.icns` files in the app bundle and restart Bear.

## Manual Installation
You can install the themes manually by copying the `.theme` files in `/Path/to/Bear.app/Contents/Resources/`. By renaming them to the file name of different theme, you can pick which theme to overwrite.

Same goes for the `.icns` files.

## Customising the Themes

I use [Sublime Text](https://www.sublimetext.com) to edit the theme files. The custom [build systems](https://www.sublimetext.com/docs/3/build_systems.html) in the [project file](https://github.com/lucaschultz/bear-theme/blob/main/bear-theme.sublime-project) (which uses the `install` script) allows previewing the changes to themes without manually copying the files after each change.

If you try to use this workflow and have trouble with the build system using `sudo` to run the `install` script you can (but probably shouldn't) [add](https://apple.stackexchange.com/a/388987) a `NOPASSWD` rule to your `sudoers` file.

## Pull Requests are Welcome

Especially lacks some love in the details. If you made some improvements on the themes: **I'm looking forward to your pull request** 🙂
