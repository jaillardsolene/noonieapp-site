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

## Patron de page app — réutilisable

`/danio` est le **patron des pages app du portefeuille**. Sa structure :
hero (nom · accroche · description · CTA · maquette) → 3 rangées de
fonctionnalités → bloc gratuit/payant → FAQ en accordéon → CTA de fin.

- `assets/app-page.css` porte **toute** la mise en page et **aucune couleur** :
  il ne lit que les variables de `site.css`. Vérifiable — il ne contient pas
  une seule valeur hexadécimale.
- La **seule** partie propre à Danio est un bloc de neuf lignes en `<style>`
  dans `danio/index.html` : la couleur de courbe de ses neuf paramètres
  (`ux.md` §3.6).

Une app 2 (terrarium, ruche) copie la page, change les tokens et remplace ces
neuf lignes. **La mise en page ne bouge pas.**

Trois sections sont **hors périmètre par décision**, et ne doivent pas être
ajoutées : logos clients (pas de B2B), témoignages (zéro app publiée, zéro
avis — en inventer un serait un mensonge), formulaire d'inscription (aucun
service d'emailing décidé, et cela contredirait le « no account, no server »
écrit sur la page elle-même).

**Les illustrations de téléphone sont des maquettes, jamais des captures** :
tant qu'aucune app n'est publiée, aucune capture n'existe. Le cadre ne contient
que de la géométrie et porte le mot « Mockup » — même règle que
`chartLocked.sampleLabel` dans l'app (`copy.md` §13).

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
- `danio/` et `/` : lien App Store réel, et captures d'écran.
