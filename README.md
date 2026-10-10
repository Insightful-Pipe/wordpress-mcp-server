# WordPress MCP Server by Insightful Pipe

[![MCP Compatible](https://img.shields.io/badge/MCP-Compatible-blue)](https://insightfulpipe.com/mcp-servers/wordpress)
[![Insightful Pipe](https://img.shields.io/badge/Insightful_Pipe-MCP_Servers-purple)](https://insightfulpipe.com/mcp-servers)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

> **Connect WordPress to AI assistants: posts, pages, media and comments via the WordPress REST API.**

Part of the [Insightful Pipe MCP Server Collection](https://insightfulpipe.com/mcp-servers) — use WordPress from Claude, ChatGPT, Cursor, and other AI assistants through the Model Context Protocol (MCP).

<img src="images/wordpress-icon.svg" alt="WordPress MCP Server" width="64" height="64">

## MCP Server URL

```
https://wordpress.insightfulmcp.com/
```

## What is WordPress MCP?

WordPress MCP is a **remote Model Context Protocol server** hosted by InsightfulPipe. Access posts, pages, media, users, comments, and site settings from your WordPress site via the REST API.

## Installation

### Claude

1. Copy the MCP Server URL: `https://wordpress.insightfulmcp.com/`
2. Open [Claude Connectors Settings](https://claude.ai/settings/connectors)
3. Scroll to the bottom and click **Add custom connector**
4. Paste the URL and click **Add**
5. Click **Connect** and sign in to InsightfulPipe if asked. Claude then lists the connector as connected.

### ChatGPT

Custom MCP servers are added through ChatGPT's **Developer mode**. Availability depends on your ChatGPT plan, and workspace admins may need to allow it.

1. Turn on **Developer mode** in ChatGPT settings
2. Create a new app for a remote MCP server and paste the URL: `https://wordpress.insightfulmcp.com/`
3. Sign in to InsightfulPipe if asked. The connection finishes as soon as you are signed in.

See OpenAI's guide: [Developer mode and MCP apps in ChatGPT](https://help.openai.com/en/articles/12584461-developer-mode-and-mcp-apps-in-chatgpt)

### Claude Code

```bash
claude mcp add --transport http wordpress https://wordpress.insightfulmcp.com/
```

### Cursor

Add the server to `~/.cursor/mcp.json` (all projects) or `.cursor/mcp.json` (one project):

```json
{
  "mcpServers": {
    "wordpress": {
      "url": "https://wordpress.insightfulmcp.com/"
    }
  }
}
```

When Cursor shows **Needs authentication**, click **Connect** and sign in to InsightfulPipe if asked.

## Available Actions

34 actions: 18 read, 16 write.

### Read Actions (18)

| Action | Description |
|--------|-------------|
| `get_categories` | List all categories |
| `get_category` | Get a specific category by ID |
| `get_comment` | Get a specific comment by ID |
| `get_comments` | List all comments |
| `get_current_user` | Get the currently authenticated user |
| `get_media` | List all media items |
| `get_media_item` | Get a specific media item by ID |
| `get_page` | Get a specific page by ID |
| `get_page_revisions` | List all revisions for a page |
| `get_pages` | List all pages |
| `get_post` | Get a specific post by ID |
| `get_post_revisions` | List all revisions for a post |
| `get_posts` | List all posts |
| `get_tag` | Get a specific tag by ID |
| `get_tags` | List all tags |
| `get_taxonomies` | List all registered taxonomies |
| `get_types` | List all registered post types |
| `search` | Search across posts, pages, and other content types |

### Write Actions (16)

| Action | Description |
|--------|-------------|
| `create_category` | Create a new category |
| `create_comment` | Create a new comment |
| `create_media` | Upload a new media item (metadata only; file upload requires multipart form) |
| `create_page` | Create a new page |
| `create_post` | Create a new post |
| `create_tag` | Create a new tag |
| `delete_category` | Delete a category (requires force=true) |
| `delete_comment` | Delete a comment (moves to trash, or permanently deletes if force=true) |
| `delete_media` | Delete a media item (requires force=true for permanent deletion) |
| `delete_tag` | Delete a tag (requires force=true) |
| `update_category` | Update an existing category |
| `update_comment` | Update an existing comment |
| `update_media` | Update a media item's metadata |
| `update_page` | Update an existing page |
| `update_post` | Update an existing post |
| `update_tag` | Update an existing tag |

## Control What Your AI Can Do

You decide what AI agents can do with each connected account:

- **Turn individual actions on or off** for every connected account, so agents only see the actions you allow.
- **Connect as Read-only or Read & Write.** A read-only connection can only enable read actions.
- **Destructive actions stay off by default.** Actions such as deletes are disabled until an admin enables them.
- **Team access per account.** Restricted team members only use the accounts they are granted, with the read actions enabled on them.

## Usage Examples

```
"List my 10 most recent posts"
```

```
"Create a draft post titled "5 Ways to Improve Your Ad Reporting""
```

```
"Show comments waiting for moderation"
```

## Pricing

The WordPress MCP server is included in every InsightfulPipe plan, together with all other MCP servers and the CLI. Plans start at $29.99/month, and you can try it for 7 days. See [insightfulpipe.com/pricing](https://insightfulpipe.com/pricing) for current plans.

## Explore More MCP Servers by Insightful Pipe

Visit **[insightfulpipe.com/mcp-servers](https://insightfulpipe.com/mcp-servers)** to discover our full collection of MCP servers.

- [WooCommerce MCP](https://insightfulpipe.com/mcp-servers/woocommerce)
- [Google Search Console MCP](https://insightfulpipe.com/mcp-servers/google-search-console)

**[View All MCP Servers →](https://insightfulpipe.com/mcp-servers)**

## Resources

- [Documentation](https://insightfulpipe.com/docs/connectors-wordpress)
- [Video Tutorial](https://www.youtube.com/playlist?list=PLJNzvjxzI5Xwe__BJJLAelSF0ewO3mEFk)
- [InsightfulPipe Blog](https://insightfulpipe.com/blog)

## Support

- **Documentation**: [insightfulpipe.com/docs](https://insightfulpipe.com/docs)
- **All MCP Servers**: [insightfulpipe.com/mcp-servers](https://insightfulpipe.com/mcp-servers)
- **Email**: support@insightfulpipe.com

---

**[Insightful Pipe](https://insightfulpipe.com)** — AI-powered marketing analytics through MCP servers. [Explore all integrations →](https://insightfulpipe.com/mcp-servers)

## License

MIT License - see [LICENSE](LICENSE) for details.
