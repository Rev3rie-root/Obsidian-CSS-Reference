Obsidian CSS Reference

A community reference for Obsidian’s interface selectors.

This repository is meant to help theme creators and CSS snippet authors understand what a selector targets and why it works. Many snippets online solve a problem without explaining how the interface is structured. The goal here is to document the pieces of Obsidian’s UI so they’re easier to customize.

**Supported Version(s)**

* Obsidian 1.12.7
* Community contributions for newer versions are welcome.

**Repository Structure**
```

Obsidian-CSS-Reference/
│
├── README.md
├── Ribbon/
├── Sidebars/
├── Tabs/
├── Editor/
├── File Explorer/
├── Status Bar/
├── Properties/
├── Modals/
└── Images/
```

### Entry Format

Each page follows the same format.

Problem

Describe what someone wants to change.

Selector
```CSS
/* CSS goes here */
```

**Explanation**
Explain what the selector targets and why it works.

**Notes**
Mention anything version-specific or any known limitations.

### Example

Left Ribbon Background When Sidebar Is Collapsed

**Problem**
The left ribbon becomes a darker color after collapsing the left sidebar.

Selector

```CSS
.workspace-ribbon.side-dock-ribbon.mod-left.is-collapsed::before {
 background-color: var(--background-primary);
}
```

**Explanation**

When the left sidebar is collapsed, Obsidian adds the .is-collapsed class to the left ribbon. The visible background is not the ribbon itself—it is drawn by the ribbon’s ::before pseudo-element. Styling that pseudo-element changes the background color shown in the collapsed state.

