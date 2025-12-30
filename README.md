# marketplace

Plugin marketplace

## Installation

```bash
claude plugin add yaccp/marketplace
```

## Usage

Ce plugin est **auto-découvert**. Décrivez simplement votre besoin :

```
"Je veux configurer marketplace"
```

Claude activera automatiquement le plugin et vous guidera via des menus interactifs.

## Configuration

Toute la configuration est stockée dans :

```
.claude/yaccp/marketplace/config.json
```

## Structure

```
marketplace/
├── .claude-plugin/
│   └── plugin.json       # Métadonnées
├── skills/
│   └── marketplace/
│       └── SKILL.md      # Workflow complet
└── CLAUDE.md             # Guide Claude
```

## License

Apache-2.0
