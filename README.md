# YACCP Marketplace

**Yet Another Claude Code Plugin** - Marketplace communautaire de plugins pour Claude Code.

## Installation

```bash
# Ajouter la marketplace
/plugin marketplace add yaccp/marketplace
```

## Plugins disponibles

| Plugin | Description | Version | Catégorie |
|--------|-------------|---------|-----------|
| `yaccp-aws-docusaurus` | Deploy sites to AWS S3 + CloudFront + Route53 | 1.1.5 | deployment |

## Utilisation

```bash
# Installer un plugin
/plugin install yaccp-aws-docusaurus@yaccp

# Mettre à jour la marketplace
/plugin marketplace update yaccp

# Mettre à jour un plugin
/plugin update yaccp-aws-docusaurus@yaccp
```

## Structure

```
marketplace/
├── .claude-plugin/
│   └── marketplace.json    # Registry référençant les plugins externes
├── CLAUDE.md
└── README.md
```

Les plugins sont hébergés dans leurs propres repos GitHub et référencés via:
```json
{
  "source": "github:yaccp/claude-plugin-aws-docusaurus"
}
```

## Contribuer un plugin

1. Créer un repo GitHub avec `.claude-plugin/plugin.json`
2. Ajouter `commands/`, `skills/`, `agents/` selon besoin
3. Fork ce repo marketplace
4. Ajouter l'entrée dans `.claude-plugin/marketplace.json`:
   ```json
   {
     "name": "mon-plugin",
     "source": "github:user/mon-plugin",
     "description": "Description du plugin",
     "category": "category"
   }
   ```
5. Pull Request

## Licence

MIT
