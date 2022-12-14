---
aliases: 
- 
tags:
- seedling
publish: true
---

# How to release a new version of your plugin?

This guide assumes that you have [[How to get started developing plugins|created your plugin using the sample plugin template]].
From the [obsidian sample plugin readme](https://github.com/obsidianmd/obsidian-sample-plugin):

1.   Update your `manifest.json` with your new version number, such as `1.0.1`, and the minimum Obsidian version required for your latest release.
2.   Update your `versions.json` file with `"new-plugin-version": "minimum-obsidian-version"` so older versions of Obsidian can download an older version of your plugin that's compatible.
3.   Create new GitHub release using your new version number as the "Tag version". Use the exact version number, don't include a prefix `v`. See here for an example: [https://github.com/obsidianmd/obsidian-sample-plugin/releases](https://github.com/obsidianmd/obsidian-sample-plugin/releases)
4.   Upload the files `manifest.json`, `main.js`, `styles.css` as binary attachments.
5.   Publish the release.


If you want to automate this, see [[Using GitHub actions to create releases for plugins]].