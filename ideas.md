# NetArchive — direction artistique

## Trois pistes

### Piste 01 — Terminal éditorial
Une archive technique sombre qui emprunte au journal de laboratoire et au terminal, avec une composition structurée par une ligne de commande verticale et des fiches comme des feuillets indexés.

**Probability:** 0.06

### Piste 02 — Blueprint nocturne
Un univers de plan réseau, bleu nuit et cyan, où les topologies deviennent le langage graphique principal et où la navigation s’organise comme une table de routage.

**Probability:** 0.03

### Piste 03 — Atelier monolithique
Une interface austère et tactile inspirée des consoles de supervision industrielles, avec des blocs denses, des repères de statut et une lecture presque opératoire.

**Probability:** 0.08

## Approche choisie — Terminal éditorial

### Design Movement
Swiss International Style appliqué à un terminal de laboratoire : grille typographique précise, hiérarchie éditoriale nette et contrepoint de signaux d’état issus des systèmes réseau.

### Core Principles
- Faire sentir l’archive : chaque section possède un identifiant, une date ou un état, comme un document de laboratoire consultable.
- Préférer la preuve à la promesse : topologies, commandes, résultats et difficultés sont mis en avant avant les ornements.
- Donner une tension calme : surfaces graphite, filets fins, cyan froid et lime signalétique, sans glow excessif ni dégradé décoratif.
- Construire une navigation opératoire : filtrer, ouvrir, copier et fermer doivent être immédiats, lisibles au clavier et toujours réversibles.

### Color Philosophy
Le graphite profond sert de papier de travail et réduit la fatigue visuelle. Le cyan signale les liaisons, la télémétrie et l’information navigable. Le lime est réservé aux états de réussite et aux points de contrôle. L’ambre indique une friction ou une zone d’attention. Les couleurs ne décorent pas : elles décrivent l’état d’un système.

### Layout Paradigm
Une colonne latérale fine joue le rôle d’index d’archive. Le contenu est volontairement asymétrique : hero en deux temps, chiffres de repérage à gauche, fiches techniques en grille irrégulière et détail projet en panneau latéral large. Les sections sont reliées par des filets et des repères, pas par des cartes uniformément arrondies.

### Signature Elements
- Un rail vertical d’archive avec points de repère, labels de section et mini curseur de terminal.
- Des micro-labels monospace du type `INDEX / 04`, `STATUS / ONLINE`, `CMD / COPY`.
- Des miniatures de topologies avec grille blueprint, nœuds, liens et points de statut.

### Interaction Philosophy
Les interactions doivent ressembler à des opérations de diagnostic : le bouton de filtre commute proprement, l’ouverture d’un projet expose sa fiche comme un dossier technique, la copie de commande donne un retour bref et explicite. Les états actifs utilisent une variation de contraste et un signal lime, jamais un mouvement gratuit.

### Animation
Entrées discrètes en fondu avec translation de 6 à 10 px, échelonnées de 40 ms par item. Les cartes montent de 2 px au survol avec transition de 180 ms ; les filets restent stables. Le drawer projet entre depuis la droite avec `transform` et `opacity`, 260 ms, et la topologie zoomée utilise une transition douce. Respecter `prefers-reduced-motion`.

### Typography System
Titres et affichage : Space Grotesk, poids 500 à 700, pour une présence technique mais humaine. Corps : IBM Plex Sans, 400 à 500, pour la lisibilité éditoriale. Labels, commandes et identifiants : IBM Plex Mono, 400 à 600. Les titres sont serrés, les métadonnées en capitales espacées, les blocs CLI jamais en italique.

### Brand Essence
**NetArchive est une bibliothèque de preuves techniques pour les étudiants et recruteurs qui veulent comprendre comment un système a été construit, testé et corrigé — pas seulement voir son résultat.**

Personnalité : méthodique, lucide, curieuse.

### Brand Voice
Les titres sont courts et factuels, les CTA décrivent une action réelle, les microcopies parlent comme un journal d’exploitation sans jargon gratuit.

- « Ouvrir le dossier technique »
- « Chaque panne laisse une méthode. »

### Wordmark & Logo
Le symbole est une constellation de trois nœuds connectés qui forme une silhouette de bouclier ouverte, traversée par un curseur `>` implicite. Le mot-symbole `NET/ARCHIVE` est composé en IBM Plex Mono avec une barre oblique lime comme séparateur, jamais en texte décoratif par défaut.

### Signature Brand Color
**Signal Lime — `#B8F05A`**. Une couleur de repérage vive, utilisée uniquement pour les états positifs, les points actifs et les actions de confirmation ; elle devient identifiable précisément parce qu’elle reste rare.

## Notes de contenu

Le catalogue s’appuie sur une collection TypeScript exportée depuis un fichier de données dédié, avec un objet par TP. Le schéma réutilisable couvre `title`, `category`, `tools`, `topologyImage`, `steps[]`, `commands[]`, `screenshots[]` et `results`, et ajoute des champs éditoriaux utiles (`id`, `summary`, `objective`, `difficulty`, `date`, `challenges`, `solutions`). Pour ajouter un nouveau travail, il suffit de dupliquer un objet et de fournir ses visuels.
