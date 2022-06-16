## Firefox

I made few changes and features to make Firefox more efficient that might be of interest to someone. I found some of them by myself some are from my colleagues that caught my eye and I really liked. Here are they... 

## Having tabs on the side rather than on top

I use [Tree Style Tab](https://addons.mozilla.org/en-US/firefox/addon/tree-style-tab/) extension to organise tabs vertically on the right/*left* side of the browser window. The issue is that now I have both tab bars - the original and one on the side.

### Hiding tab bar

How to hide the tab bar:
1. go to ```about:config```
2. set ```toolkit.legacyUserProfileCustomizations.stylesheets``` to ```true```
3. go to Firefox directory ```/home/user/.mozilla/firefox/##hash##.profile_name/``` 
4. create folder with name ```chrome```
5. in the ```chrome``` folder create file ```userChrome.css``` 

```
#main-window[tabsintitlebar="true"]:not([extradragspace="true"]) #TabsToolbar > .toolbar-items {
  opacity: 0;
  pointer-events: none;
}
#main-window:not([tabsintitlebar="true"]) #TabsToolbar {
    visibility: collapse !important;
}
````

For more information on how to change more things in Firefox you can find it [www.userchrome.org](https://www.userchrome.org/firefox-89-styling-proton-ui.html)

## Using profiles in Firefox

I am a mess when it comes to tab management in the browser. The moment I learned that I can start browser where I left my work, I started hoarding tabs. I mean it is pretty bad hah. 100+ is no problem for me and when I am working on multiple projects at the same time, school stuff, stuff I want to read... I started attacking 200. It is neatly organized but it is not healthy and my brain is subconciously overloaded.

https://support.mozilla.org/en-US/kb/back-and-restore-information-firefox-profiles

...

## Accessing HTTP sites (taken from [here](https://support.mozilla.org/en-US/questions/959914))

	1. In a new tab, type or paste about:config in the address bar and press Enter. Click the button promising to be careful.
	2. In the filter box, type or paste autofill and pause while the list is filtered
	3. Double-click browser.urlbar.autoFill to toggle it from true to false. 