# <img src="/img/icon48.png" align="absmiddle"> Spaces

### Jake's maintained fork of the Spaces Chrome/Brave extension

This repo is a personal fork of Spaces, a Chrome extension for window-based
workspace management. The fork exists to keep the extension usable on modern
Chrome/Brave after Manifest V3, to preserve tab group metadata, and to fix
regressions found while using named Spaces heavily.

The most important local fix is for named spaces that contain Chrome/Brave tab
groups. During window teardown, the browser emits tab-group events while tabs are
disappearing. Older fork code handled those events by saving the whole tab list
from the transient closing window, which could overwrite a saved space with an
empty or partial tab list. This fork keeps tab-group persistence separate from
canonical tab-list persistence so closing and reopening a grouped named space
does not clobber its tabs.

### Original project summary

Spaces is a workspace manager for chrome.
It treats each chrome window like a different workspace and lets you name and save each space.
You can close a window full of tabs at any time then reopen it later and continue exactly
where you left off.

Spaces keeps track of new tabs opened in each workspace and also tabs that you close.
It also allows you to quickly move a tab that you are currently viewing into any
other space- whether it's open or closed.
Great for when you find yourself opening a tab out of context with what you are currently
working on and want to come back to it later.

Spaces was developed to help users that tend to have way too many tabs open in a chrome window.
It encourages you to move tabs that are not immediately relevant into a different,
more appropriate space - thus removing it from your current window.
This keeps your chrome session manageable - both visually and from a memory perspective.

Isn't this essentially just bookmarks with folders? Yeah, pretty much - but who uses bookmarks?

### Chrome Web Store

~~Spaces is also [available via the official Chrome Web Store](https://chrome.google.com/webstore/detail/spaces/cenkmofngpohdnkbjdpilgpmbiiljjim).~~

Please note that the webstore version may be behind the latest version here.

### Manifest V3

This extension has been migrated to manifest v3 in order to be compatible with modern Chrome versions.

### Tab groups support

Along with manifest v3 migration, [Tab groups](https://blog.google/products/chrome/manage-tabs-with-google-chrome/) support has been added.

### Install as an extension from source

1. Download the **[latest available version](https://github.com/JakeSc/spaces/archive/refs/heads/master.zip)**
2. Unarchive to your preferred location (e.g., `Downloads`).
2. In **Google Chrome**, navigate to [chrome://extensions/](chrome://extensions/) and enable <kbd>Developer mode</kbd> in the upper right corner.
3. Click on the <kbd>LOAD UNPACKED</kbd> button.
4. Browse to the _root directory_ of the unarchived download, and click <kbd>OPEN</kbd>.

> **TODO** &mdash; add more sections
> - [ ] Build from github
> - [ ] License (currently unspecified)
