# River skills for Claude

Claude skills for working with River models (Excel add-in).

| Skill | What it does |
|-------|--------------|
| `river-model-structure` | Reviews, plans and applies a documentation group structure for a River flow, through the River MCP server. |
| `river-documentation` | Turns a River documentation export into a user-facing documentation draft (`documentation_draft.md`). |

`river-model-structure` needs the **River MCP server** to be connected in Claude.

## Claude Desktop

Skills are loaded through plugins distributed by the River Solutions Marketplace.

1. In Claude Desktop, open **Customize** and select **Plugins**
2. Click the **Add** button → **Add marketplace**
3. Select **Add from a repository**
4. Paste `https://github.com/river-solutions/river-claude-plugin.git` then select it
5. Make sure **Sync automatically** is toggled on
6. The list of plugin will now show a new plugin called **River**. Click on the **+** icon on the plugin card to enable it. It will now show with a green tick mark.
7. If you want to check the list of skills, click the plugin card.

From this point, the skills are available both in Claude Chat and Code. They will update automatically when a new version is published.

Note that some skills require the River MCP Connector, which is a separate installation.

## Claude Code

Add this repository as a plugin marketplace, then install the `river` plugin:

```
/plugin marketplace add river-solutions/river-claude-plugin
/plugin install river@river-solutions
```

Restart Claude Code (or run `/reload-plugins`) and check that the skills are listed with `/skills`.

To update later:

```
/plugin marketplace update river-solutions
```

## Using the skills

Just ask, e.g. *"Is my River model well structured?"* or *"Write the documentation for this River model."* Claude picks the matching skill automatically. You can also use a slash command by typing `/river-` and select the skill you want to use.
