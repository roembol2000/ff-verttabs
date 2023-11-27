# Firefox autohide vertical tabs

Vertical tab goodness

## Setup

### Sidebery

- Install the Sidebery add-on
- If you don't want the tree style tabs, you can disable them in the Sidebery settings under "Tabs tree structure"
- In the Sidebery settings, go to the Style Editor and paste in the contents of `sidebery.css`

### Autohide

- Open your profile directory by typing `about:support` in the address bar and pressing the "Open Directory" button under "Profile Directory"
- If it doesn't already exist, create a "chrome" directory in the profile directory
- Add the contents of the "chrome" directory in this repository to yours
- We need to tell Firefox to look for our custom CSS files. Go to `about:config`, search for 'userprof', and double click the toolkit.legacyUserProfileCustomizations.stylesheets preference to switch it to true.
