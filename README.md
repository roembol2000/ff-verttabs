# Firefox autohide vertical tabs

Vertical tab goodness

![Demo GIF](media/demo.gif)

## Why? I thought Firefox already has this built-in

While Firefox does have this feature built-in these days, it does not work very well when you have too many tabs open. The built-in tab list gets increasingly unresponsive the more tabs you have, and when you have a few hundred tabs open it just breaks down.

This setup handles thousands of tabs fine, without breaking a sweat. As I do daily-drive this, it gets updated very quickly as new Firefox versions come out that change the behaviour of the sidebar.

## Setup

Download the files from the [latest release](https://github.com/roembol2000/ff-verttabs/releases/latest) -> Source code (zip)

### Sidebery

- Install the Sidebery add-on
- If you don't want the tree style tabs, you can disable them in the Sidebery settings under "Tabs tree structure"
- In the Sidebery settings, go to the Style Editor and paste in the contents of `sidebery.css`

### Autohide

- Open your profile directory by typing `about:support` in the address bar and pressing the "Open Directory" button under "Profile Directory"
- If it doesn't already exist, create a "chrome" directory in the profile directory
- Add the contents of the "chrome" directory in this repository to yours
- Your directory structure should look something like the following:

```
[profile dir]/
├─ extensions/
├─ chrome/
│  ├─ css/
│  │  ├─ vertical-tabs.css
│  ├─ userChrome.css
├─ crashes/
├─ storage/
├─ addons.json
├─ ...
```

- We need to tell Firefox to look for our custom CSS files. Go to `about:config`, search for 'userprof', and double click the toolkit.legacyUserProfileCustomizations.stylesheets preference to switch it to true.
- Open the sidebar preferences in Firefox (press the gear icon at the bottom of the sidebar)
- Uncheck the "Open tools from sidebar" option
- Restart Firefox

### Configuration

- By default, the original tab bar will be disabled. If you wish to keep the original tab bar around, you can enable it at the top of the vertical-tabs.css file.
  - To get your window controls back, right click on some blank space on the top bar and go to "Customize Toolbar...". There, turn on "Title Bar" at the bottom.
- You can also change the width and transition time / delay here.

## Updating

If an update broke the autohiding, I will try to fix the CSS. To update, simply replace the contents of the 'vertical-tabs.css' file with the new version in your userchrome directory (which can be found using the steps above). Check the release notes below for any additional instructions.

- 2023-11-27 (v1.0.0): Initial release
- 2024-11-29 (v2.0.0): Fix compatibility with Firefox 133
- 2025-06-27 (v2.1.0): Fix compatibility with Firefox 140
- 2026-10-07 (v3.0.0): Fix compatibility with Firefox 157 ("Nova" redesign)
  - In the sidebar settings ("Customize sidebar"), disable "Open tools from sidebar".
    - You might need to for example open the bookmarks sidebar before can go to the settings, press <kbd>Ctrl</kbd> + <kbd>B</kbd> or <kbd>Cmd</kbd> + <kbd>B</kbd> to access the bookmarks.
  - Update the contents of the Style Editor in Sidebery with the new contents of `sidebery.css`.

## Thank you for using!

Please share :)
