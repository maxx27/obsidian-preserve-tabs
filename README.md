# Obsidian Preserve Tabs

If file is already opened then jump to its tab. Otherwise default behavior.

## Original idea and credits

Thanks to Zhihao Nan and his [open-in-new-tab-and-preserve-tabs](https://github.com/Nanzhxxx/open-in-new-tab-and-preserve-tabs) plugin.

## Behavior

- If the current tab contains file A and you open file B, file B opens in a existing tab and becomes active.
- If file B is already open in another tab, Obsidian switches to that existing tab instead of opening a duplicate.
- If the current tab is empty, Obsidian reuses the empty tab.
- If you open the same file that is already active, Obsidian keeps the current tab.

This applies to file opens that use Obsidian's normal `openFile` flow, including the file explorer, search results, recent files, and calendar daily notes.

## Installation

### From Obsidian Community Plugins

After the plugin is accepted into the community directory:

1. Open Obsidian Settings.
2. Go to Community plugins.
3. Search for `Preserve Tabs`.
4. Install and enable the plugin.

### Manual installation

1. Download `manifest.json` and `main.js` from a release.
2. Place them in:

   ```text
   <vault>/.obsidian/plugins/obsidian-preserve-tabs/
   ```

3. Reload Obsidian.
4. Enable the plugin in Community plugins.

## Notes

The plugin wraps Obsidian's `WorkspaceLeaf.openFile` method and restores the original method when unloaded.

## License

MIT
