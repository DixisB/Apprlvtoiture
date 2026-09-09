# Relevé toiture

Application web d'un seul fichier pour réaliser un **relevé de toiture** sur le
terrain : on importe le plan, on pose un repère numéroté à chaque désordre, on
lui associe des photos et une description, puis on génère une **planche de
synthèse** (PNG) ou un **rapport A4** (impression / PDF).

Aucune installation, aucun compte, aucun serveur : tout tient dans
`index.html` et les données restent dans le navigateur de l'appareil
(`localStorage`).

## Utilisation

Ouvrir `index.html` dans un navigateur, ou publier le dépôt sur GitHub Pages et
ajouter la page à l'écran d'accueil du téléphone.

| Onglet | Rôle |
| --- | --- |
| **Plan** | Import du plan (fichier, glisser-déposer ou collage), zoom/pince, pose et déplacement des repères. Le plan tient toujours dans un cadre de hauteur fixe : les actions restent atteignables sans défiler, et le doigt fait défiler la page tant que le plan n'est pas agrandi. |
| **Repères** | Une fiche par désordre : description, photos (appareil ou galerie), repositionnement, suppression. |
| **Planche** | Plan au centre, vignettes photo en périphérie reliées par des flèches à leur repère. Aperçu ajusté à l'écran par défaut (bascule « Taille réelle »), export PNG et impression toujours en pleine résolution. Une vignette sans description n'affiche que sa photo. |

Le menu `⋮` donne accès à l'impression / PDF, au remplacement du plan, à
l'export et l'import d'une sauvegarde `.json`, au thème (auto / clair / sombre)
et à la réinitialisation du relevé.

## Parti pris graphique

Interface d'outil technique : **aplats uniquement**, aucun dégradé, aucune
ombre portée, aucune animation décorative. La hiérarchie repose sur des filets
d'un pixel, des angles à 4 px et une échelle typographique courte. La palette
tient en trois valeurs — marine `#0E2338` pour la structure, orange `#C9531D`
réservé aux repères et aux actions, gris neutres pour le reste — et la même
couleur de repère est utilisée à l'écran, dans la planche exportée et dans le
rapport imprimé.

L'ergonomie a été revue en même temps : navigation par onglets, thème clair et
sombre, en-tête avec nom et adresse du chantier, indicateur d'occupation du
stockage, feuilles d'actions et boîtes de dialogue à la place des `alert()`,
visionneuse photo, sauvegarde `.json` exportable, repères repositionnables et
rapport d'impression dédié.

Le moteur métier d'origine est conservé : même clé de stockage
(`releve-toiture-projet`), même format de données, même algorithme de
répartition des vignettes et de tracé des flèches. Les deux versions lisent donc
les mêmes relevés.

## Code d'origine

La version initiale est conservée telle quelle dans
[`legacy/releve-toiture-v5-original.html`](legacy/releve-toiture-v5-original.html)
— voir [`legacy/README.md`](legacy/README.md) pour y revenir.
