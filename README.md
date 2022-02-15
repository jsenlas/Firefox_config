## My Firefox

I use Firefox with certain modifications, here are some of them.

## Hiding tab bar

I use [Tree Style Tab](https://addons.mozilla.org/en-US/firefox/addon/tree-style-tab/) extension to organise tabs vertically on the left/right side of the browser window. The issue with this is that then I am stuck with original tab bar and the Tree Style Tab in the sidebar... 

So how to hide the tab bar:
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
 
