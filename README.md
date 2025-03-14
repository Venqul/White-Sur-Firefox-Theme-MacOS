## Details about this fork of WhiteSur
This is a customized version of WhiteSur, designed with [Neptune](https://github.com/yiiyahui/Neptune-Firefox) integration and [ATBC](https://github.com/easonwong-de/Adaptive-Tab-Bar-Colour) compatibility. It includes added features like a Safari-style homepage and buttons. For a seamless dark mode experience, pair it with this Firefox [theme](https://addons.mozilla.org/en-US/firefox/addon/dark-theme-for-whitesur/).
<p align="center"><img width="45%" src="https://github.com/user-attachments/assets/ba54b08b-e259-4de1-8561-83978ee4cf68"><img width="45%" src="https://github.com/user-attachments/assets/ac27d055-4959-4285-bf8a-599fcdabf2f5"></p>


### **Color Themes:**
<p align="center"><img width="50%" src="https://github.com/user-attachments/assets/1e53d35a-57d6-4897-9527-cbfab1e539b8"></p>
<p align="center">
<a href="https://addons.mozilla.org/en-US/firefox/addon/safari-15-dark-theme/">DARK THEME 1</a>
</p>

<p align="center"><img width="50%" src="https://github.com/user-attachments/assets/ff72f684-3839-4e27-bef1-988ba713bc6b"></p>
<p align="center">
<a href="https://addons.mozilla.org/en-US/firefox/addon/dark-theme-for-whitesur/">DARK THEME 2</a>
</p>

<p align="center"><img width="50%" src="https://github.com/user-attachments/assets/f3ae6eea-64df-4e2e-a030-76957ae1ce52"></p>
<p align="center">
<a href="https://addons.mozilla.org/en-US/firefox/addon/safari-15-light-theme/">LIGHT THEME</a>
</p>



- To skip to the original `README.md`, please click [here](#firefox-whitesur-theme)
- For Details About ATBC Compatability by Eason Wong, head [here](https://github.com/easonwong-de/White-Sur-Firefox-Theme-MacOS) 
- For Details About Neptune, head [here](https://github.com/yiiyahui/Neptune-Firefox)
### Quick Link

[Installation](#installation-macos)  
~~1. [Command](#installation-flags)~~  
2. [Manual](#manual-installation-macos--windows)

### Browser Configurations

Go to `about:config`

-   Set `toolkit.legacyUserProfileCustomizations.stylesheets` to `true`
-   Set `svg.context-properties.content.enabled` to `true`
-   Set `layout.css.color-mix.enabled` to `true`
-   Set `layout.css.backdrop-filter.force-enabled` to `true` (optional)
-   Set `layout.css.color-mix.color-spaces.enabled` to `true` (optional)

### Theme Configuations

The theme can be configured in `userChrome.css` and `userContent.css`.

These are some examples:

-   Configuations in `userChrome.css`

    -   `extension-menu-in-grid.css` (On by default) <br>

    <img width="50%" src="https://raw.githubusercontent.com/easonwong-de/WhiteSurFirefoxThemeMacOS/master/githubpreview/extension-menu-in-grid.png"><br>

    -   `hide-single-tab.css` (Remove buttons from the tab bar to take effect) <br>

    <img width="50%" src="https://raw.githubusercontent.com/easonwong-de/WhiteSurFirefoxThemeMacOS/master/githubpreview/hide-single-tab.png"><br>

    -   `mini-tabbar.css` <br>

    <img width="50%" src="https://raw.githubusercontent.com/easonwong-de/WhiteSurFirefoxThemeMacOS/master/githubpreview/mini-tabbar.png"><br>

    -   ~~`tab-preview-on-hover.css` (Requires [Tab Preview On Hover](https://github.com/easonwong-de/Tab-Preview-On-Hover)) <br>~~

    <img width="50%" src="https://raw.githubusercontent.com/easonwong-de/WhiteSurFirefoxThemeMacOS/master/githubpreview/tab-preview-on-hover.png"><br>

-   Configuations in `userChrome.css`
    -   `apple-style-homepage.css`
    -   `apple-style-twp-popup.css`

The whole configuation list can be found under `chrome -> WhiteSur -> customs`.

<br>

Additional `README.md` ends here.


<br><br>

## Firefox WhiteSur theme

<p align="center">
<img width="120" src="https://github.com/AdamXweb/WhiteSurFirefoxThemeMacOS/raw/master/githubpreview/safarifirefox.png?raw=true">
	<br>
A <code>MacOS</code> & <code>Windows</code> Firefox theme to look more like Big Sur Safari. (For Firefox 70+)</p>

![Preview](githubpreview/whitesur.gif?raw=true)

## Description

Aim is to make Firefox look more like MacOS Big Sur Safari.\
This is a CSS theme adapted to work on MacOS from the Linux GTK theme.\
Based on https://github.com/vinceliuice/WhiteSur-gtk-theme/tree/master/src/other/firefox \
(This is a quick modification, and is not written from scratch.)

## Installation (MacOS)

Download the [latest release](https://github.com/AdamXweb/WhiteSurFirefoxThemeMacOS/releases/), or clone the repo above.\
A script has been added to streamline the installation process.\
Open terminal in the directory of the repo, and run `bash install.sh`\
Follow the prompts

### Installation flags

The script supports the following flags

-   `-c` To enable close button on the left hand side
-   `-f` To specify the default firefox folder (it will try to find the profile folder to place the theme within)
-   `-l` Default location of most Linux installations
-   `-u` Remove the animation on URL bar to be clickable throughout
-   `-n` Removes the identity colour from tabs
-   `-r` Remove the theme

e.g. To install with script, with close button left hand side: `bash install.sh -c`

### Manual installation (MacOS & Windows)

Copy `chrome` and `configuration` folers into your Firefox Profile Directory

To find your Firefox Profile Directory you can:

1. Go to `about:support` in Firefox.
2. Application Basics > Profile Directory > Open Directory.
3. Copy folders mentioned above into the profile folder. (usually has `-release` at the end).
4. If you are using Firefox 69+:
    1. Go to `about:config` in Firefox.
    2. Search for `toolkit.legacyUserProfileCustomizations.stylesheets` and set it to `true`.
5. Restart Firefox.
6. Done!

#### Manual theme overrides:

To manually add a custom override, copy the `*.css` from the `custom` folder of whichever option you are after. Place it in the `chrome/WhiteSur/parts` foder within the profile directory you opened above.\
Next, import the `.css` file you just specified. To do this, open `chrome/WhiteSur/theme.css` in the same directory above and add the line\
`@import "parts/NAMEOFOPTION.css";` above the line that says `@namespace xul...`\
That's it, the theme should load your overriden settings

#### Swap navbar close buttons on Windows:

`windows-swapclose.css` contains the styles required to swap the close buttons, as well as to re-order the close button from MacOS styling to Windows.
Follow the directions above for the manual theme override to activate.

### Manual colour override:

The theme obeys your system UI colour preferences. If you want to override it e.g. always have the dark theme, then you'll have to do the following.\
The solution if you don't want to change your System UI colour is to do add the following to your `about:config`\
Add: `ui.systemUsesDarkTheme` with the number value with 1 for dark, and 0 for light.\
![Screen Shot 2021-05-04 at 7 10 19 pm](https://user-images.githubusercontent.com/6800453/116982626-60317980-ad0c-11eb-96aa-0879b05c98fc.png)

Please note, you won't be able to change the System UI colour if you are using `privacy.resistFingerprinting`. This apparently is for both web pages and the System UI.

## Known bugs

If it is a fresh install of Firefox, the script for MacOS should enable the settings automatically, however users who have toggled settings may need to do the `about:config` in step 4 above.\
If for any reason the WhiteSur theme doesn't activate after using the script, follow steps 4.1 and 4.2 to toggle the stylesheets from within the Firefox settings.

The tab background colour can be overwritten by themes installed through firefox extentions.
e.g. if you are using a dark theme in light mode, tab backgrounds that are inactive are affected.
Fix: Change the installed theme to appropriate colour scheme to avoid issues.

If you're looking to change the directory to run the script, you can always type `bash` then drag the file into terminal. You can also type `cd` and then drag the folder and press enter to navigate to the directory.\
Alternatively, if you're running Catalina, the default teminal is zsh, meaning you can change folders by typing the name to enter the folder e.g. `WhiteSurFirefoxThemeMacOS`

Q: "Why bother doing this, and not just use safari?" \
A: I've used safari for quite a few years, and was rather disappointed with the change in extensions, particularly with content blocking. This prompted me to use uBlock origin on Firefox, and to customise it to have the best aesthetics, and simplest transition.

### New bugs

If you've found a new bug, please report it as a new issue with the templates provided.

Thanks!

## Screenshot

### Windows

![Preview](githubpreview/whitesurwindows.gif?raw=true)

### MacOS

![Preview](githubpreview/whitesur.gif?raw=true)
