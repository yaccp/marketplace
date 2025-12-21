Met à jour marketplace.json avec les dernières versions des plugins depuis GitHub, commit, tag et push.

## Instructions

1. Lire le fichier `.claude-plugin/marketplace.json`

2. Pour chaque plugin dans le tableau `plugins`:
   - Extraire le repo depuis `source.repo` (ex: "yaccp/claude-plugin-aws-docusaurus")
   - Récupérer le plugin.json distant via curl (pour éviter le cache):
     `curl -s "https://raw.githubusercontent.com/{repo}/main/.claude-plugin/plugin.json"`
   - Parser le JSON retourné

3. Comparer les champs suivants et mettre à jour dans marketplace.json si différent:
   - `version`
   - `description`
   - `keywords`
   - `author`

4. Si aucune modification, afficher "Aucune mise à jour nécessaire" et terminer

5. Écrire le marketplace.json mis à jour (conserver le formatage avec 2 espaces d'indentation)

6. Afficher un résumé clair:
   - Nombre de plugins vérifiés
   - Pour chaque plugin mis à jour: nom et version (ancienne → nouvelle)
   - Plugins inchangés

7. Git commit:
   - Message: "chore: Update {plugin-name} to v{version}" (si un seul plugin mis à jour)
   - Message: "chore: Update {n} plugins" (si plusieurs plugins mis à jour)

8. Git tag:
   - Format: `v{marketplace.version}.{YYYYMMDD}` (ex: v1.0.0.20251221)
   - Utiliser la date du jour

9. Git push avec tags:
   - `git push origin main --tags`
