# Ari Plugin Registry

This repository serves as the official source for community plugins for the Ari application. It hosts the static `registry.json` file used by the application to browse and install plugins.

## Registry Schema (`registry.json`)

The `registry.json` file contains a list of all approved plugins.

```json
{
  "version": 1,
  "plugins": [
    {
      "id": "gift-plugin",
      "name": "Gift Management",
      "description": "Manage gift ideas and wishlists for your contacts",
      "author": "Ari Team",
      "repo": "ari-project/ari-plugin-gifts",
      "icon": "gift",
      "tags": ["contacts", "gifts"],
      "minCoreVersion": "0.1.0"
    }
  ]
}
```

### Fields

| Field | Description |
|-------|-------------|
| `id` | Unique identifier, must match `plugin.json` → `name` in the plugin archive. |
| `name` | Human-readable display name. |
| `description` | Short description (1-2 sentences). |
| `author` | Author name. |
| `repo` | GitHub `owner/repo` — used to fetch releases and README. |
| `icon` | Optional icon identifier (Lucide icon name). |
| `tags` | Array of categorization tags. |
| `minCoreVersion` | Minimum required Ari core version. |

## Submitting a Plugin

To submit a new plugin:

1.  Host your plugin on GitHub.
2.  Create a release with a `plugin.zip` asset.
3.  Fork this repository.
4.  Add your plugin entry to `registry.json`.
5.  Submit a Pull Request.

Your plugin must comply with the [Ari Plugin Guidelines](https://github.com/ari-project/ari).
