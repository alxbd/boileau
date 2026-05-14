<h1 align="center">Boileau</h1>

<p align="center">
  <b>Un skill pour repérer et corriger les marques d'écriture par IA dans un texte en français.</b>
</p>

<p align="center">
  <i>« Ce que l'on conçoit bien s'énonce clairement,<br>
  et les mots pour le dire arrivent aisément. »<br>
  — Nicolas Boileau, <i>L'Art poétique</i> (1674)</i>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/couverture-38_marqueurs_%C2%B7_6_familles-brightgreen" alt="38 marqueurs · 6 familles">
  <img src="https://img.shields.io/badge/langue-fran%C3%A7ais_uniquement-blue" alt="Français uniquement">
  <a href="https://github.com/alxbd/boileau/blob/main/LICENSE"><img src="https://img.shields.io/github/license/alxbd/boileau?style=flat&color=blue" alt="License"></a>
</p>

<br />

---

## Pourquoi

Les guides « Signs of AI writing » existants (Wikipedia EN, plugins de détection, listes de tics) sont presque tous en anglais. Traduits littéralement, ils ratent les biais propres à l'IA générative en français :

- **Faux registre soutenu** (*effectuer*, *à l'aune de*, *problématique* nominalisé)
- **Calques de l'anglais** (*adresser un problème*, *faire du sens*, *délivrer de la valeur*)
- **Connecteurs académiques en pluie** (*Par ailleurs*, *De plus*, *En outre*, *Néanmoins*…)
- **Typographie française cassée** (guillemets droits au lieu de « », espaces insécables manquantes, accents oubliés sur les majuscules : *Etat*, *Apres*, *A propos*)
- **Registre pseudo-littéraire mièvre** (*promesse murmurée*, *instant suspendu*, *comme si le temps s'était figé*)
- **L'adjectif *véritable* posé devant tout et rien**

Boileau couvre ces marqueurs à partir de sources francophones (voir ci-dessous), pas d'une traduction.

## Ce que fait le skill

À partir d'un texte donné, Claude :

1. Repère les marqueurs IA présents (38 marqueurs documentés, regroupés en 6 familles)
2. Réécrit chaque passage problématique
3. Présente une première version humanisée
4. Fait une passe d'audit : « qu'est-ce qui sonne encore IA ? »
5. Présente une version finale après correction de l'audit
6. Liste les changements faits (optionnel)

## Couverture

Le skill couvre 6 grandes familles, 38 marqueurs :

| Famille | Marqueurs |
|---|---|
| Lexique | Vocabulaire IA, *véritable* antéposé, verbes passe-partout, faux soutenu lexical, faux familier dans contexte pro, doublets d'adjectifs |
| Tournures & syntaxe | Évitement de *être*, parallélismes négatifs et phrases en miroir, triades, anaphores rythmées, variation élégante, fausses gammes, connecteurs en pluie, tournures pseudo-soutenues, transitions pseudo-journalistiques |
| Calques de l'anglais | Anglicismes IA, calques syntaxiques |
| Contenu | Inflation d'importance, inflation de notoriété, analyses en participes présents, langage promotionnel, attributions floues, sections « Défis et perspectives » |
| Style & mise en forme | Tirets cadratins, gras mécanique, listes à en-tête en gras, émojis, typographie française cassée |
| Communication & délayage | Artefacts conversationnels, avis de coupure de connaissance, ton flatteur, auto-validation rhétorique, méta-annonces, posture didactique, phrases creuses, sur-qualification, conclusions vides, registre mièvre |

Le skill s'inspire de la structure du guide [Wikipedia:Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing) mais redéfinit chaque section avec un lexique et des exemples natifs en français. Certaines sections de l'original anglais ont été retirées (Title Case dans les titres, qui n'existe pas en français), d'autres ajoutées (calques de l'anglais, typographie française, registre mièvre).

## Installation

Boileau suit le format SKILL.md, désormais reconnu par plusieurs agents IA (Claude Code, OpenAI Codex CLI, GitHub Copilot CLI, Google Gemini CLI, Cursor…). Voir la section correspondant au client utilisé. Pour une installation portable entre plusieurs clients, voir [Installation inter-clients](#installation-inter-clients) plus bas.

### Pour Claude Code (utilisateur courant)

Cloner le repo dans le dossier des skills personnels :

```bash
mkdir -p ~/.claude/skills
cd ~/.claude/skills
git clone git@github.com:alxbd/boileau.git
```

Le skill sera disponible dans toutes les sessions Claude Code.

### Pour un projet Claude Code spécifique

Cloner dans `.claude/skills/` à la racine du projet :

```bash
mkdir -p .claude/skills
cd .claude/skills
git clone git@github.com:alxbd/boileau.git
```

### Pour OpenAI Codex CLI

Codex lit les skills depuis `~/.agents/skills/` (utilisateur) et `.agents/skills/` (racine de repo) :

```bash
mkdir -p ~/.agents/skills
cd ~/.agents/skills
git clone git@github.com:alxbd/boileau.git
```

Pour un projet Codex spécifique, cloner plutôt dans `.agents/skills/` à la racine du repo.

### Pour GitHub Copilot CLI

Copilot CLI accepte `~/.copilot/skills/` ou `~/.agents/skills/` côté utilisateur, et `.github/skills/`, `.claude/skills/` ou `.agents/skills/` côté projet :

```bash
mkdir -p ~/.copilot/skills
cd ~/.copilot/skills
git clone git@github.com:alxbd/boileau.git
```

### Pour Google Gemini CLI

Gemini CLI lit `~/.gemini/skills/` ou `~/.agents/skills/` (utilisateur), et `.gemini/skills/` ou `.agents/skills/` (projet) :

```bash
mkdir -p ~/.gemini/skills
cd ~/.gemini/skills
git clone git@github.com:alxbd/boileau.git
```

### Pour Cursor

Cursor lit `~/.cursor/skills/` ou `~/.agents/skills/` (utilisateur), et `.cursor/skills/` ou `.agents/skills/` (projet) :

```bash
mkdir -p ~/.cursor/skills
cd ~/.cursor/skills
git clone git@github.com:alxbd/boileau.git
```

### Installation inter-clients

Codex CLI, Copilot CLI, Gemini CLI et Cursor reconnaissent tous le chemin standard `~/.agents/skills/` (utilisateur) et `.agents/skills/` (projet). C'est l'emplacement le plus portable pour qui jongle entre plusieurs clients :

```bash
mkdir -p ~/.agents/skills
cd ~/.agents/skills
git clone git@github.com:alxbd/boileau.git
```

Note : Claude Code n'utilise pas `~/.agents/skills/`. Pour rendre Boileau aussi disponible dans Claude Code, ajouter en plus l'installation Claude Code ci-dessus (ou créer un lien symbolique entre les deux dossiers).

## Utilisation

Trois façons de l'invoquer :

**1. Demande directe**
> Humanise ce texte : « Notre solution incontournable constitue une véritable révolution… »

**2. Via la mention du skill**
> Utilise le skill boileau pour relire ce post LinkedIn.

**3. Sur un fichier**
> Passe ce fichier `draft.md` dans boileau.

Claude répond avec :
- Une première réécriture
- Une passe d'audit (ce qui sonne encore IA)
- Une version finale corrigée
- Un récap des changements (sur demande)

## Quand l'utiliser

- Relecture d'un texte écrit par une IA (article, post, mail, document)
- Vérification d'un texte qu'on a soi-même écrit mais qui sent l'IA
- Édition d'un communiqué, d'une page web, d'un brief
- Nettoyage de notes ou de plans générés en brainstorm

## Quand ne pas l'utiliser

- Pour de la traduction : ce n'est pas son rôle
- Pour des textes très techniques où le vocabulaire identifié comme « IA » est en fait précis et nécessaire (par exemple, *crucial* peut être pertinent dans un papier de recherche médicale)
- Pour des fictions ou des textes créatifs où certains tics (mièvres, lyriques) sont assumés stylistiquement

## Sources

Le skill est ancré dans des références francophones :

- [Aide:Identifier l'usage d'une IA générative — Wikipédia FR](https://fr.wikipedia.org/wiki/Aide:Identifier_l%27usage_d%27une_IA_g%C3%A9n%C3%A9rative)
- [Projet:Observatoire des IA — Wikipédia FR](https://fr.wikipedia.org/wiki/Projet:Observatoire_des_IA/Documentation)
- [Wikipédia:Sondage/IA générative](https://fr.wikipedia.org/wiki/Wikip%C3%A9dia:Sondage/Intelligence_artificielle_g%C3%A9n%C3%A9rative)
- [40 marqueurs linguistiques qui trahissent (Isma)](https://redigeretvendreavecia.substack.com/p/40-marqueurs-linguistiques-qui-trahissent)
- [Les tics de langage de ChatGPT (Daria décrypte l'IA)](https://dariadecrypteia.substack.com/p/les-tics-de-langage-de-chatgpt)
- [Reconnaître un texte d'IA (Loumina)](https://www.loumina.fr/blog-reconnaitre-un-texte-d-ia-les-tics-de-chatgpt)
- [Comment savoir si un texte a été généré par ChatGPT (Digitad)](https://digitad.ca/comment-savoir-texte-genere-par-chatgpt/)
- [La réception de ChatGPT au sein de Wikipédia (UQAM)](https://collimateur.uqam.ca/collimateur/la-reception-de-chatgpt-au-sein-de-wikipedia/)
- [Wikipedia:Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing) (anglais, pour la structure générale)

## Crédits et remerciements

Boileau est un dérivé du skill [humanizer](https://github.com/blader/humanizer) de **Siqi Chen** ([@blader](https://github.com/blader)), publié sous licence MIT en 2025. Merci à lui pour le travail initial : la structure du skill, le format des sections (avant/après, mots à surveiller, problème), la passe d'audit finale et l'ancrage sur le guide *Signs of AI writing* de Wikipédia EN viennent directement de son skill.

À partir de cette base, Boileau a été progressivement étendu et adapté au français, à mesure que des biais spécifiques à l'IA générative en français étaient observés dans des textes réels :

- Lexique et exemples entièrement réécrits à partir de sources francophones (Wikipédia FR, catalogues de tics IA en français, observations terrain).
- Sections retirées car non pertinentes en français (Title Case dans les titres, guillemets courbes EN).
- Sections étendues ou ajoutées pour des biais propres au FR : calques de l'anglais, typographie française cassée, registre pseudo-littéraire mièvre, faux-registre familier mélangé au pro, anaphores rythmées (« Pour celles qui… »), connecteurs académiques en pluie, posture didactique, méta-annonces, transitions pseudo-journalistiques, et plusieurs autres.
- Le skill est itératif : chaque nouveau pattern observé dans un texte FR généré par IA est ajouté avec sa formulation, ses exemples avant/après, et son explication.

Le skill anglais reste plus large et plus polyvalent. Boileau est plus étroit (français uniquement) mais plus précis sur les tics français.

## Licence

MIT. Voir [LICENSE](LICENSE) pour le texte complet, qui inclut les notices de copyright de Boileau et de humanizer (le skill original dont Boileau dérive).
