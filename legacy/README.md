# Sauvegarde du code initial

Ce dossier conserve la version d'origine de l'application, telle qu'elle
existait avant la refonte complète de l'interface.

| Fichier | Description |
| --- | --- |
| `releve-toiture-v5-original.html` | Application d'origine (v5), copie exacte de l'ancien `index.html` (commit `b131e9f`). |

Le fichier est autonome : il s'ouvre directement dans un navigateur, sans
installation ni dépendance. Les données restent stockées en local
(`localStorage`, clé `releve-toiture-projet`) — la nouvelle version utilise la
**même clé et le même format**, les relevés existants sont donc conservés et
les deux versions restent interchangeables.

Pour revenir à l'ancienne interface :

```bash
cp legacy/releve-toiture-v5-original.html index.html
```
