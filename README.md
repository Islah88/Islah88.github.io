# Portfolio — El Islah Mhoma

Portfolio personnel d'**El Islah Mhoma**, Ingénieur IA / LLMOps : agents autonomes,
RAG souverain et sécurisation des LLM.

En ligne : **<https://islah88.github.io>**

## Contenu

| Page | Rôle |
|---|---|
| `index.html` | Accueil : positionnement, preuves chiffrées, compétences, parcours, références, contact |
| `projets.html` | Réalisations : étude de cas approfondie (SCALPEL) puis fiches projets courtes |
| `success.html` | Page de confirmation après envoi du formulaire de contact |

## Stack

Site statique, sans build ni dépendance à installer.

- HTML5 / CSS3, thème **Stellar** (HTML5 UP) personnalisé
- jQuery, Scrollex, Scrolly, Font Awesome — tous embarqués dans `assets/`
- Formulaire de contact : [Formspree](https://formspree.io) en AJAX, avec redirection
  vers `success.html`
- Hébergement : GitHub Pages, servi à la racine du domaine utilisateur

## Développement local

Aucune compilation n'est nécessaire. Pour prévisualiser le site, il faut simplement le
servir en HTTP (l'ouvrir en `file://` casse les chemins absolus des ressources) :

```bash
python -m http.server 8000
```

Puis ouvrir <http://127.0.0.1:8000>.

## Déploiement

Tout commit poussé sur la branche `main` est publié automatiquement par GitHub Pages.

Après une modification de `assets/css/main.css`, incrémenter le numéro de version dans
les liens `main.css?v=N` des pages HTML, afin de forcer les navigateurs à recharger la
feuille de style au lieu de servir leur copie en cache.

## Formulaire de contact — pré-remplissage par URL

Un lien de la forme `index.html?subject=<clé>#contact` personnalise automatiquement le
titre, la description et le message du formulaire. Les clés disponibles sont définies
dans l'objet `SUJETS` en bas de `index.html` : ajouter une entrée à cet objet suffit à
brancher un nouveau bouton « En savoir plus » depuis une fiche projet.

## Structure

```
.
├── assets/          # CSS, JS et polices du thème (ne pas modifier main.css sans besoin)
├── documents/       # CV et sources LaTeX
├── images/          # Photos, captures de projets, image de partage Open Graph
├── index.html
├── projets.html
├── success.html
├── robots.txt
└── sitemap.xml
```

## Crédits

Thème **Stellar** par [HTML5 UP](https://html5up.net) (@ajlkn), utilisé sous licence
[Creative Commons Attribution 3.0](https://html5up.net/license). Icônes :
[Font Awesome](https://fontawesome.com). Voir `LICENSE.txt`.
