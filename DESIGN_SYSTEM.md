# Design System & Art Direction

Ce document régit toute décision visuelle sur ce site (couleurs, typographie, espacement, composition, animation). Avant tout changement de CSS ou de mise en page, s'y référer — il prime sur l'intuition ponctuelle.

> **Révision (version définitive, validée visuellement)** : le site est structuré en **trois zones de fond plates** qui se succèdent du haut vers le bas de la page — blanc, crème, puis kaki juste avant le footer noir — plutôt qu'un kaki dominant sur l'ensemble du site comme une version antérieure de ce document l'avait décrit. Le reste de la palette reste **noir** (texte, footer) et **bronze** (accent, rare et volontaire). Voir §2-3 et §11. Tout le reste (espacement, composition, typographie, animations) reste valable et n'a pas changé de logique.

## 1. Identité générale

Identité visuelle **naturelle, méditerranéenne, sobre et professionnelle**, inspirée des couleurs du maquis corse (kaki, olive profond, vert très sombre) — sans jamais devenir le sujet du site.

Positionnement à la rencontre de :

**Financial · Editorial · Luxury · Mediterranean** — avec une priorité claire donnée à **Financial + Editorial**. La touche méditerranéenne vient en dernier, comme une nuance de caractère, pas comme un thème.

Combiner simultanément :
- finance, rigueur ;
- élégance, sobriété ;
- personnalité ;
- origine méditerranéenne / maquis corse — discrète.

Le site doit ressembler davantage à un **site éditorial financier premium** (type rapport annuel haut de gamme, magazine économique) qu'à un site institutionnel classique ou à un site vitrine. Il doit pouvoir être montré à un professionnel du M&A, Private Equity, conseil financier ou corporate finance sans donner une impression amateur, touristique ou excessivement créative.

**Mots-clés** : Natural — Mediterranean — Institutional — Editorial — Premium — Calm — Serious — Refined

**Éviter absolument** :
- effet militaire / camouflage ;
- effet randonnée / outdoor ;
- tourisme corse, site de voyage ;
- vert trop vif ou trop saturé ;
- design trop rustique ou artisanal ;
- trop startup, trop technologique ;
- trop coloré, trop "corporate générique" ;
- trop luxueux/ostentatoire ;
- trop minimaliste au point de devenir froid.

## 2. Palette de couleurs — trois bandeaux plein écran (blanc / crème / kaki), noir et bronze en complément

**Règle centrale : le fond de page change par bandeaux successifs, chacun plein écran (edge-to-edge, comme le bandeau noir du footer) — pas un kaki dominant partout, et pas un panneau clair posé au milieu d'un fond coloré.** Trois teintes, dans l'ordre où elles apparaissent en descendant la page :

| Bandeau | Couleur | Sections |
|---|---|---|
| **Blanc** (chaud, jamais blanc pur) | `--zone-white` | Intro, Télécharger mon CV, Parcours, Recommandations |
| **Crème** | `--zone-cream` | Analyses, Calculateur (Analyse financière) |
| **Kaki / olive profond** | `--paper` | En dehors des chiffres (juste avant le footer noir) |

| Rôle | Couleur | Usage |
|---|---|---|
| **Texte / éléments sombres** | Noir (quasi pur) | Texte principal, titres, nav, fond du footer |
| **Accent** | Bronze / doré discret | Boutons et éléments interactifs (survol inclus), icônes, petites touches d'accent — jamais une grande surface |

**Principe pratique de mise en page** : chaque bandeau couvre toute la largeur de l'écran, pas seulement la largeur du contenu (960px) — c'est le même traitement que le footer noir, qui a toujours été plein écran. À l'intérieur d'un bandeau, les cartes existantes (`.card`, `.calc-shell`, `.cv-card`, `.edc-card`, `.reco-card`, toutes sur `--ivory`) continuent de flotter par-dessus, un ton plus clair que le crème et légèrement plus chaud que le blanc, ce qui suffit à les détacher sans dégradé ni bordure appuyée. Sur le bandeau kaki (`#personal`), les trois `.edc-card` de "En dehors des chiffres" poussent ce principe plus loin qu'ailleurs : ombre large et diffuse dès le repos (pas seulement au survol) pour un vrai effet de flottement, volontairement plus marqué que sur `.card`/`.cv-card` puisque le contraste ivoire/kaki est plus fort que ivoire/blanc ou ivoire/crème.

**Éviter l'effet "template/Canva"** — piège déjà rencontré une fois sur ce site : des rectangles blanc pur posés sur un aplat de couleur uniforme lisent immédiatement comme un gabarit générique. Garde-fou : les cartes ne sont jamais en blanc pur (`#FFFFFF`) — toujours `--ivory`, une teinte crème chaude — et le bandeau "blanc" lui-même reste légèrement teinté plutôt que `#FFFFFF` pur.

Toutes les teintes restent **désaturées et élégantes** — jamais de vert lumineux ou saturé. Le kaki ne doit jamais virer militaire/camouflage : le choisir suffisamment riche et sourd (jamais terne ni criard).

**Ne pas** : utiliser un bleu corporate classique · utiliser des gradients flashy entre bandeaux · multiplier les nuances de vert (on reste sur le trio blanc/crème/kaki + noir/bronze, pas une palette de beiges/verts/terracotta comme dans une version antérieure de ce document).

## 3. Utilisation des couleurs

**Le kaki sert à :**
- le bandeau "En dehors des chiffres", juste avant le footer noir ;
- un panneau interne différencié (ex. le bloc "marché en direct" dans une carte d'analyse), pour créer de la profondeur sans sortir de la famille de couleur.

**Le blanc et le crème servent à :**
- les bandeaux de fond des autres sections (voir §2) — le blanc pour Intro/CV/Parcours/Recommandations, le crème pour Analyses/Calculateur ;
- en `--ivory` (une nuance de crème plus claire que le bandeau crème), les cartes et panneaux qui portent du texte dense (CV, timeline, analyse, calculateur).

**Le noir sert à :**
- tout le texte courant, les titres, la navigation (menu, liens) sur les bandeaux blanc et crème ;
- les fonds volontairement sombres (footer, "signature" de fin de page).
- Sur le bandeau kaki, le texte passe en clair (`--ivory` / `--muted-light`) plutôt qu'en noir, pour rester lisible.

**Le bronze sert à :**
- un déclencheur d'attention ponctuel : bouton au survol, icône, séparateur d'accent — jamais une surface large.

## 4. Inspiration financière

Malgré l'identité corse, conserver les codes visuels du monde financier : M&A, Private Equity, investment banking, stratégie, analyse financière, conseil, sérieux professionnel.

Référence : un **rapport financier haut de gamme** ou un **magazine économique premium**, pas un site vitrine classique. Typographie élégante et très lisible. Hiérarchie immédiatement compréhensible entre titre, sous-titre, texte, chiffres, informations secondaires.

## 5. Esthétique Finance / M&A — sections sensibles

Les parties suivantes doivent avoir une esthétique particulièrement sobre et analytique, plus proche d'une interface financière/éditoriale haut de gamme que d'un site perso :

- **Analyse**
- **Calculateur**
- **Bandeau LVMH / Hermès**

Le bandeau LVMH/Hermès en particulier doit rester très lisible et professionnel — jamais l'impression d'un site de trading amateur. Priorité à la clarté des chiffres, à l'alignement, à la typographie mono pour les données — pas à la décoration.

## 6. Typographie

Professionnelle, élégante, très lisible, contemporaine, cohérente avec le monde financier.

- Une **sans-serif moderne et très lisible** pour les informations courantes, les données, l'interface.
- Une **police éditoriale** (avec plus de personnalité) est acceptable pour les grands titres, si elle reste cohérente avec le reste — c'est déjà l'esprit de la paire actuelle (serif éditoriale pour les titres, sans-serif pour le corps de texte, mono pour les chiffres).
- Les chiffres, données financières et informations de marché doivent être **particulièrement lisibles** (idéalement une police mono/tabulaire dédiée aux données).

**Éviter** : typographies manuscrites, trop "vintage", artisanales, touristiques, trop futuristes, trop arrondies, trop ludiques, décoratives.

## 7. Maquis corse — une inspiration, pas un thème

Le lien avec la Corse doit être **subtile et progressif** : quelqu'un qui découvre le site doit le percevoir peu à peu (par les couleurs, une texture, une lumière) plutôt que de le voir affiché explicitement.

**Ne pas multiplier** les références visuelles à la Corse : pas de photos de plages, pas de motifs corses caricaturaux, pas de drapeaux décoratifs, pas de paysages omniprésents, pas de clichés touristiques.

Le maquis peut inspirer : les couleurs, quelques textures très légères, les photographies utilisées, certains arrière-plans, quelques éléments graphiques discrets — jamais plus.

**Si des photographies sont utilisées** : naturelles, élégantes, peu saturées, avec de la profondeur, éventuellement légèrement assombries/désaturées pour rester sobres. Jamais de cliché touristique évident (plage, calanques cartes-postales, etc.).

Résultat recherché : **"un site financier avec une identité méditerranéenne discrète"** — jamais "un site corse consacré à la finance".

## 8. Menu (hamburger)

Le bouton hamburger (haut gauche) doit être **discret et élégant** — un détail d'interface, pas un élément décoratif. Le menu ouvert doit utiliser la palette définie ci-dessus (fond ivoire/beige, texte vert très sombre, accents kaki pour les séparateurs ou l'état actif) et garder une excellente lisibilité.

Il doit donner l'impression de faire **partie intégrante** du site depuis le début — pas d'un composant ajouté après coup. Pas d'ombre excessive, pas d'effet flashy à l'ouverture : une transition sobre suffit (voir §13 Animations).

## 9. Espacement et respiration (règle fondamentale)

Ne jamais coller des éléments simplement parce qu'il reste de la place. Chaque élément doit disposer d'un espace visuel suffisant. Utiliser généreusement : padding, margin, espaces verticaux/horizontaux, largeur de contenu contrôlée.

Le site ne doit jamais donner l'impression que les éléments ont été posés à la suite les uns des autres avec quelques pixels entre eux — chaque section doit avoir son propre rythme et sa propre respiration.

## 10. Composition proportionnelle

Répartir les éléments de façon proportionnelle et équilibrée. Éviter : blocs trop petits noyés dans des espaces énormes, blocs trop larges sans raison, colonnes de largeur identique quand ça ne sert pas le contenu, sections surchargées, éléments regroupés dans une seule zone de l'écran.

Les proportions doivent suivre le contenu : un élément principal peut occuper plus d'espace, les informations secondaires peuvent être plus compactes, une donnée importante peut bénéficier de plus d'espace. La hiérarchie visuelle doit être évidente sans lire le contenu.

## 11. Déroulement naturel du site

Le scroll doit donner une impression de progression naturelle, jamais de passage brutal d'un bloc indépendant à un autre. Chaque section a une relation logique avec la précédente — un parcours qui ressemble à une histoire :

`Introduction → Présentation → Expertise/contenu → Informations importantes → Détails → Conclusion/contact`

Éviter les changements brutaux de couleur, taille, style, densité, alignement entre sections adjacentes. Rythme visuel continu.

**Référence concrète** : le site [Rothschild & Co](https://www.rothschildandco.com/fr-fr/) illustre bien ce principe — quasiment aucune ligne de séparation visible entre les sections ; les transitions se font par un espace généreux ou un dégradé très doux, jamais une coupure nette. C'est le contre-exemple de l'effet "blocs empilés" (voir aussi §13).

**Règle technique** : ne jamais mettre de `border-bottom` sur la règle générique `section` — ça matérialise une couture visible à chaque changement de section, qui est précisément ce qu'on cherche à éviter. La continuité entre sections voisines vient plutôt du fait qu'elles partagent la même couleur de zone (voir ci-dessous) : deux sections adjacentes de même zone sont visuellement indissociables, sans qu'aucune ligne ni ombre ne marque la frontière.

**Trois zones de fond plates** : le fond de page change par blocs de sections, du haut vers le bas du site, en trois couleurs pleines (pas de dégradé) :

- **Zone blanc** (`--zone-white`) — Intro, Télécharger mon CV, Parcours, Recommandations.
- **Zone crème** (`--zone-cream`) — Analyses, Calculateur (Analyse financière).
- **Zone kaki** (`--paper`) — En dehors des chiffres, qui précède directement le footer noir.

Chaque section pose sa couleur de zone en fond plein (`background` sur l'`id` de la section, pas de dégradé interne) ; des sections voisines de même zone (ex. Intro/CV/Parcours) s'enchaînent donc sans aucune coupure visible. Les cartes existantes (`.card`, `.calc-shell`, `.cv-card`, `.edc-card`, `.reco-card`, toutes sur `--ivory`) continuent de flotter par-dessus leur zone — plus claires que le crème, légèrement plus chaudes que le blanc — ce qui suffit à les détacher du fond sans dégradé.

Sur la zone kaki (`#personal`), le texte passe en clair (`--ivory` pour les titres et le texte courant, `--muted-light` pour le texte secondaire) plutôt qu'en noir, pour rester lisible — voir §2.

**Piège technique important : le bandeau doit être plein écran, pas seulement large comme le contenu.** Une `<section>` qui porte `class="wrap"` directement voit sa propre boîte limitée à 960px et centrée (`.wrap{max-width:960px;margin:0 auto;...}`) — tout `background` posé sur cette section ne peint alors que ce bloc central de 960px, avec la zone précédente visible sur les côtés (c'est le bug qui s'est produit une fois : un panneau clair flottant au milieu d'un fond kaki, au lieu d'un vrai bandeau plein écran). Le motif correct, déjà utilisé par `#cv` et par `<footer>`, est de **ne jamais mettre `class="wrap"` sur la `<section>` elle-même** mais de nicher une `<div class="wrap">` juste à l'intérieur pour contraindre le contenu — la section garde alors sa largeur 100% et son `background` couvre tout l'écran. Les six sections concernées (`#intro`, `#cv`, `#parcours`, `#analyses`, `#calculateur`, `#personal`) suivent toutes ce motif.

## 12. Sections

Chaque section doit avoir une **raison d'exister** — ne pas en créer une juste pour remplir la page. Son format (large et immersif, compact et informatif, éditorial, grille, centré sur un chiffre, centré sur un texte) doit être choisi en fonction de son contenu.

**Règle** : le contenu détermine la composition, pas l'inverse.

## 13. Cartes et effets visuels — sobriété avant tout

Un site financier sérieux ne doit pas ressembler à un dashboard de dizaines de petits rectangles. Réserver les cartes aux cas où elles apportent une réelle valeur : comparaison, regroupement d'informations, indicateur, contenu indépendant. Pour le reste, privilégier : espaces, lignes, typographie, variations de taille, alignements, séparateurs discrets.

**Éviter systématiquement** : ombres excessives, dégradés trop visibles, effets 3D, éléments décoratifs qui n'apportent rien au contenu.

## 14. Animations

Subtiles et lentes. Le site doit sembler vivant, jamais animé pour attirer artificiellement l'attention.

**Privilégier** : apparition progressive, léger déplacement, transitions douces, hover discret, changement subtil d'opacité.

**Éviter** : animations rapides, effets flashy, parallaxes excessives, éléments qui sautent, rotations, animations permanentes.

**Principe** : l'animation accompagne la navigation, elle ne devient jamais le contenu.

## 15. Responsive design

Pensé dès le départ pour desktop, tablette et mobile — pas une simple réduction de la version desktop. Sur mobile : conserver les espaces, conserver la hiérarchie, simplifier les grilles, éviter les blocs compressés, conserver une lecture naturelle. Le contraste et la lisibilité (notamment pour les données financières et le menu) doivent rester excellents sur petit écran.

## 16. Checklist avant d'ajouter un élément

Avant d'ajouter quoi que ce soit, vérifier :
1. Est-il réellement nécessaire ?
2. Quelle est sa hiérarchie par rapport aux autres éléments ?
3. Dispose-t-il de suffisamment d'espace ?
4. Est-il cohérent avec la palette (kaki en fond, noir/blanc/bronze pour le reste — pas de nouvelle couleur ajoutée) ?
5. Est-il cohérent avec l'identité financière du site ?
6. Le regard comprend-il naturellement où aller ensuite ?

Si la réponse est non à l'une de ces questions : revoir la composition plutôt que d'ajouter du CSS.

## 17. Principe général

> Un environnement financier premium et éditorial : kaki en fond, noir pour le texte, blanc pour la lecture, bronze en signature discrète.

Assez professionnel pour être présenté à des professionnels du M&A, Private Equity, Investment Banking ou Corporate Finance — mais avec une identité assez personnelle pour ne pas ressembler à un template financier générique, et suffisamment différente des sites bleu marine/blanc habituels du secteur.

### Règle absolue

Sobriété avant décoration.
Blanc pour lire, kaki pour respirer, bronze pour ponctuer.
Espacement avant densité.
Hiérarchie avant accumulation.
Cohérence avant variété.
Naturel avant spectaculaire.
