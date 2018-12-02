## NoiaButtons for Firefox Quantum (60+)

**[Releases & changelog](https://github.com/Aris-t2/Noiabuttons/releases)**

## Want to support this project?

**[[ Paypal Me ]](https://www.paypal.me/tkpay)**  

## Instructions / Howto / Readme

- [WebExtensions can not modify Firefox Quantums appearance properly](#webextensions-can-not-modify-firefox-quantums-appearance-properly)  
- [Where to find Firefox profile folder? The correct location for user styles.](#where-to-find-firefox-profile-folder-the-correct-location-for-user-styles)  
- [How to use custom user styles?](#how-to-use-custom-user-styles)  
- [How to find item ids and attributes?](#how-to-find-item-ids-and-attributes)  
- [How to modify custom user styles?](#how-to-modify-custom-user-styles)  
- [Available options](#available-options)  

## WebExtensions can not modify Firefox Quantums appearance properly

The only way to modify ui is adding custom CSS code to **userChrome.css** and **userContent.css** files inside browsers profile folder.  
Keep in mind CSS code can not create entirely new items, buttons or toolbars. It only can modify already present ui items.  

## Where to find Firefox profile folder? The correct location for user styles.

**1.** Find your profile folder ('profile names are different for everyone').  
`about:support > Profile Folder > Open Folder`  
or `about:profiles > Root Directory > Open Folder`  

**2.** User styles belong into `\chrome\` folder. Create it, if there is none yet. It should look like this afterwards:  
`\ PROFILE FOLDER NAME \chrome\`  

**3.** Copy `userChrome.css`, `userContent.css` and `\config\`, `\css\`, `\image\` folders into `\chrome\` folder. It should look like this afterwards:  
`\chrome\config\`  
`\chrome\css\`  
`\chrome\image\`  
`\chrome\userChrome.css`  
`\chrome\userContent.css`  

(Optional) Profile folders location on drive:  
**Windows**  
`C:\Users\ USERNAME \AppData\Roaming\Mozilla\Firefox\Profiles\ PROFILE FOLDER NAME \`  
Hidden files must be visible to see `AppData` folder. Alternatively open `%APPDATA%\Mozilla\Firefox\Profiles\` from explorers location bar.  
**Linux**  
`/home/ username /.mozilla/firefox/ profile folder name /`  
Hidden files must be visible to see `.mozilla` folder.  
**Mac OS X**  
`~\Library\Mozilla\Firefox\Profiles\ PROFILE FOLDER NAME \` or  
`~\Library\Application Support\Mozilla\Firefox\Profiles\ PROFILE FOLDER NAME \`  
`\Users\ USERNAME \Library\Application\Support\Firefox\Profiles\`  

## How to use custom user styles?

The _userChrome.css_ and _userContent.css_ files works like an options\configurations file. All main "features" can be enabled and disabled there.  
Edit _userChrome.css_ and _userContent.css_ with any text editor (**[Notepad++](https://notepad-plus-plus.org/download/)** recommended on Windows) and enable or disable any feature you like by modifying, removing or outcommenting available `@import` strings.  
Restart Firefox after every modification for changes to take effect.  

**Example**  
If "classic button appearance for navigation toolbar buttons" should be <u>enabled</u>, the corresponding line has to look like this:  
`@import "./css/noiaui_light.css";`  

If "classic button appearance for navigation toolbar buttons" should be <u>disabled</u>, the corresponding line has to look like this:  
`/* @import "./css/noiaui_light.css"; */`  

Note  
Code between `/*` and `*/` won't be used by Firefox unless there are other `/*` or `*/` inbetween.  

## How to find item ids and attributes?

Firefox 57-60  

Enable once:  
1\. Tools > WebDeveloper > Toggle Tools > Toolbox Options > Enable browser chrome and add-on debugging toolboxes  
2\. Tools > WebDeveloper > Toggle Tools > Toolbox Options > Enable remote debugging  

Hit `Ctrl+Alt+Shift+I` or open 'Tools > WebDeveloper > Browser Toolbox'.  

Inspect ui or web content.  

Force popups to stay open for inspection:  
Click on 'disable popup auto hide' button (= button with four squares) on developer toolbars end.  

Firefox 61+  

Enable once:  
1\. Tools > WebDeveloper > Toggle Tools > 'Customize Tools and get help button' (= button with three dots) > Settings > Enable browser chrome and add-on debugging toolboxes  
2\. Tools > WebDeveloper > Toggle Tools > 'Customize Tools and get help button' (= button with three dots) > Settings > Enable remote debugging  

Hit `Ctrl+Alt+Shift+I` or open 'Tools > WebDeveloper > Browser Toolbox'.  

Inspect ui or web content.  

Force popups to stay open for inspection: 
Click on 'Customize Tools and get help button' (= button with three dots) and select 'Disable popup auto-hide'.  

## How to modify custom user styles?

Open CSS files with a text editor. Look through the code and change values the way you need.  
Some files contain additional instructions about how to tweak the ui for individual cases.  
Restart Firefox for changes to take effect.  

_Example_  
Open `./css/noiaui_light.css` file  
Look for `/* unloaded/pending tabs color *//*`  
Remove `/*` at lines end to make that part of the code active. Save the file and restart Firefox.  


## Available options

[Buttons]  
- Noia button icons for toolbars (default)  
- Firefox 1 button icons for toolbars  
- Firefox 2 button icons for toolbars  
- Firefox 3 button icons for toolbars  
- Firefox 4 button icons for toolbars  
  
- shrink button icons on hover (default)  
  
- autosize for button icons on nav-bar (default) [compact=24/normal=30/touch=36]  
- 18x18px (tiny) size for button icons on nav-bar  
- 24x24px (small) size for button icons on nav-bar  
- 30x30px (normal) size for button icons on nav-bar  
- 36x36px (large) size for button icons on nav-bar  
  
[Location Bar]  
- location bar icons for go button and autocomplete dropmarker
  
[Themes for toolbars and tabs known from 'Noia4' and 'NoiaFox' themes *]  
- Noia theme (light)  
- Noia theme (light) + tabs below navigation toolbar  
- Noia theme (light) + tabs below navigation toolbar (Fx65+)  
- Noia theme (dark)  
- Noia theme (dark) + tabs below navigation toolbar  
- Noia theme (dark) + tabs below navigation toolbar (Fx65+)  
  
[Additional theme settings]  
- Noia theme (light): alternative tab colors  
- Noia theme (dark): alternative tab colors  
- Noia theme (light): separator between navigation toolbar and bookmarks toolbar  
- Noia theme (dark): separator between navigation toolbar and bookmarks toolbar  



