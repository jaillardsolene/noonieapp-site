# noonieapp.com

Site vitrine du portefeuille NoonieApp. HTML/CSS statique, aucun framework,
aucun JS. Servi par GitHub Pages sur le domaine `noonieapp.com`.

## Pages

| Chemin | Fichier |
|---|---|
| `/` | `index.html` |
| `/danio` | `danio/index.html` |
| `/danio/privacy` | `danio/privacy/index.html` |
| `/danio/support` | `danio/support/index.html` |
| `/mentions-legales` | `mentions-legales/index.html` |

## Tokens visuels

Repris tels quels de Danio (`apps/aquarium/ux.md` §3, monorepo séparé) :
encre `#3B3B4F` · fond clair `linear-gradient(180deg, #EAF6FA, #CFE2E9)` ·
fond sombre `#29293A → #0E0E15` · accent action
`linear-gradient(135deg, #25C6DB, #39A6EA)` · lien `#62629F` / `#9E9ED4` ·
Plus Jakarta Sans. Thème sombre par `prefers-color-scheme`, sans JS.

Une app 2 (terrarium, ruche…) ne change que ces tokens : la structure du site
ne bouge pas.

## À compléter avant publication

- `mentions-legales/` : SIRET, nom, adresse, hébergeur — page marquée
  incomplète en clair.
- `danio/privacy/` : date de « Last updated ».
- `danio/` et `/` : lien App Store réel, et captures d'écran.
