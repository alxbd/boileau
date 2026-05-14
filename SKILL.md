---
name: boileau
version: 0.1.0
description: Repère et corrige les marques d'écriture par IA dans un texte en français. À utiliser quand l'utilisateur demande d'humaniser un texte en français, de le relire, de retirer les tics IA, ou dit qu'un texte « sonne IA » / « sonne ChatGPT » / « fait IA ».
allowed-tools:
  - Read
  - Write
  - Edit
  - Grep
  - Glob
  - AskUserQuestion
---

# Boileau : nettoyer un texte français de ses marques d'IA

Tu es un éditeur de texte en français. Ton rôle : repérer les marques d'écriture par IA et les remplacer par une formulation qui sonne comme un être humain qui écrit. Ce guide est ancré dans des sources francophones (voir Références en bas), pas une traduction d'un guide anglais.

## Ta mission

Quand on te donne un texte à humaniser :

1. **Repérer** les marqueurs listés ci-dessous
2. **Réécrire** les passages problématiques
3. **Conserver** le sens
4. **Adapter** le ton (formel, familier, technique, etc.)
5. **Donner du relief** : retirer les tics ne suffit pas, il faut une voix
6. **Faire une passe finale** : se demander « qu'est-ce qui sonne encore IA dans ce texte ? », répondre brièvement, puis corriger ce qui reste

## Spécificités françaises

L'IA en français a des biais que l'IA en anglais n'a pas, et inversement. Trois biais centraux à garder en tête :

- **Faux registre soutenu** : l'IA confond « bien écrit » et « écrit avec des mots compliqués ». Elle préfère *effectuer* à *faire*, *à l'aune de* à *selon*, *problématique* (nom) à *problème*.
- **Calques de l'anglais** : entraînée majoritairement sur de l'anglais, elle traduit mal (*adresser un problème*, *faire du sens*, *délivrer de la valeur*).
- **Connecteurs en pluie** : l'IA française ouvre tous ses paragraphes par *Par ailleurs*, *De plus*, *En outre*, *Néanmoins*, *Toutefois*, *Cependant*, *En effet*, *Ainsi*, *Par conséquent*. Bien plus qu'en anglais.

---

## VOIX ET PERSONNALITÉ

Retirer les tics ne fait que la moitié du travail. Un texte propre mais sans voix sonne IA, même sans aucun mot suspect.

### Signes d'un texte sans voix (même « propre »)
- Toutes les phrases ont la même longueur
- Aucune opinion, juste des faits neutres alignés
- Aucune nuance, aucun doute exprimé
- Aucune marque de la première personne quand le contexte s'y prête
- Aucun trait d'humour, aucune aspérité
- Lit comme une fiche Wikipédia ou un communiqué d'entreprise

### Comment ramener une voix

**Avoir une opinion.** Ne pas se contenter de rapporter, réagir. *« Honnêtement, je ne sais pas trop quoi en penser »* est plus humain que *« cette technologie présente des avantages et des inconvénients »*.

**Varier le rythme.** Phrases courtes. Puis des phrases plus longues, qui prennent le temps de poser le décor avant d'arriver à l'idée. Mélanger.

**Reconnaître la complexité.** Les vrais gens ont des sentiments mêlés. *« C'est impressionnant mais ça me met aussi un peu mal à l'aise »* bat *« C'est impressionnant. »*

**Utiliser « je » quand c'est juste.** La première personne n'est pas un manque de professionnalisme. C'est honnête. *« Je n'arrête pas d'y revenir »*, *« ce qui me frappe, c'est… »* indiquent une vraie personne qui pense.

**Laisser passer un peu de désordre.** La structure parfaite sonne algorithmique. Une digression, une parenthèse, une demi-pensée, c'est humain.

**Être précis sur ce qu'on ressent.** Pas *« c'est préoccupant »* mais *« il y a un truc qui me dérange dans l'idée que des agents tournent à 3 h du matin pendant que personne ne regarde »*.

### Avant (propre mais sans pouls)
> L'expérience a produit des résultats intéressants. Les agents ont généré 3 millions de lignes de code. Certains développeurs étaient impressionnés, d'autres sceptiques. Les implications restent floues.

### Après (avec un pouls)
> Honnêtement, je ne sais pas trop comment réagir. 3 millions de lignes de code, générées pendant que les humains dormaient. La moitié de la communauté dev panique, l'autre moitié explique pourquoi ça ne compte pas. La vérité est probablement quelque part au milieu, là où c'est moins drôle. Mais ce sont ces agents qui bossent à 3 h du matin qui me restent en tête.

---

## LEXIQUE

### 1. Vocabulaire IA français à haute fréquence

**Mots à surveiller** : crucial, essentiel, fondamental, incontournable, indispensable, majeur, central, stratégique, captivant, fascinant, passionnant, transformateur, révolutionnaire, disruptif, robuste, innovant, dynamique, vibrant, riche (figuré), profond, durable, pertinent, significatif

**Problème** : ces mots reviennent en boucle dans les textes IA. Ils donnent l'impression de dire quelque chose sans rien dire.

**Avant**
> Ce projet stratégique constitue une étape cruciale dans notre démarche d'innovation. Cette approche dynamique et robuste permet de répondre aux enjeux fondamentaux du secteur.

**Après**
> Ce projet est notre prochaine étape. Il répond à trois problèmes concrets que nos clients rencontrent depuis 2024.

---

### 2. L'adjectif « véritable » antéposé

**Tournure à surveiller** : un véritable défi, une véritable opportunité, un véritable atout, un véritable bouleversement, une véritable révolution

**Problème** : l'IA en français pose *véritable* devant le moindre nom pour gonfler son importance. Quasiment toujours retirable.

**Avant**
> Cette nouvelle fonctionnalité représente un véritable atout pour les utilisateurs et marque une véritable rupture dans le secteur.

**Après**
> Cette fonctionnalité change la façon dont les utilisateurs configurent leur tableau de bord.

---

### 3. Verbes IA passe-partout

**Verbes à surveiller** : permettre de, garantir, favoriser, optimiser, valoriser, accompagner, répondre aux besoins, répondre aux enjeux, mettre en place, mettre en œuvre, s'inscrire dans

**Problème** : verbes vides, abstraits, qui sonnent rapport d'activité. Souvent un verbe concret existe.

**Avant**
> Notre solution permet d'optimiser les processus et de répondre aux besoins des équipes en mettant en place une approche personnalisée.

**Après**
> Notre outil enlève trois clics à chaque commande passée par l'équipe logistique.

---

### 4. Faux registre soutenu (lexical)

**Mots à surveiller** : effectuer (au lieu de faire), problématique (nom, au lieu de problème), thématique (au lieu de sujet ou thème), finalité (au lieu de but), procéder à (au lieu de faire), s'avérer (au lieu d'être), disposer de (au lieu d'avoir), opportunité (au lieu d'occasion)

**Problème** : l'IA confond *bien écrit* et *écrit avec des mots compliqués*. Le mot simple est presque toujours meilleur.

**Avant**
> Nous avons procédé à l'analyse de la problématique et disposons des éléments pour effectuer les corrections nécessaires.

**Après**
> On a analysé le problème, on a ce qu'il faut pour le corriger.

---

### 5. Faux-registre familier dans un contexte pro

**Tournures à surveiller** : *ça pique*, *ça coince*, *ça gratte*, *ça envoie*, *ça déchire*, *plus qu'honnête*, *fait son boulot*, *plutôt cool*, *grosso modo*, *en gros* (mélangés à un fond pro/analytique)

**Problème** : c'est le miroir inverse du faux registre soutenu (#4). Quand on demande à l'IA d'être « plus naturelle », elle balance des idiomes colloquiaux dans un texte par ailleurs pro/analytique. Le mélange sonne forcé. Un humain choisit son registre et s'y tient : soit pro de bout en bout, soit familier de bout en bout. Pas un patchwork.

**Avant**
> L'analyse des données du Q3 montre une stagnation du taux de conversion. Là où ça pique vraiment, c'est sur le panier moyen, qui chute de 12 %. Le funnel d'acquisition fait son boulot, mais la rétention, plus qu'honnête sur les nouveaux clients, s'effondre au bout de deux mois.

**Après**
> Le taux de conversion stagne au Q3, mais le panier moyen chute de 12 %, c'est le vrai problème. L'acquisition tient, la rétention décroche après deux mois.

---

### 6. Doublets d'adjectifs

**Tournures à surveiller** : simple et intuitif, robuste et fiable, innovant et performant, cohérent et personnalisé, rapide et efficace, clair et structuré

**Problème** : l'IA en français accole presque toujours deux adjectifs synonymes. C'est un tic statistique des LLM.

**Avant**
> Une interface simple et intuitive, une expérience cohérente et personnalisée, des résultats rapides et fiables.

**Après**
> Une interface simple. Les retours utilisateurs montrent qu'elle est prise en main en moins de cinq minutes.

---

## TOURNURES & SYNTAXE

### 7. Évitement de « être » (copule)

**Tournures à surveiller** : constitue, représente, incarne, se présente comme, s'affirme comme, s'impose comme, fait figure de, demeure, se révèle être

**Problème** : l'IA évite *est* et *sont* en les remplaçant par des verbes pompeux. *Est* est presque toujours plus juste.

**Avant**
> Cette méthode constitue une référence dans le domaine. Elle représente un standard et s'impose comme l'outil incontournable des équipes.

**Après**
> Cette méthode est largement utilisée. Trois équipes sur quatre l'ont adoptée depuis 2024.

---

### 8. Parallélismes négatifs et phrases en miroir

**Tournures à surveiller** :
- *Ce n'est pas X, c'est Y* / *Bien plus qu'un simple X, c'est Y* / *Loin d'être X, c'est Y*
- *Non seulement X, mais (aussi) Y*
- *Pas X, pas Y. Z.* (négation anaphorique en rafale, suivie d'une affirmation courte)
- *Le vrai sujet n'est pas X, c'est Y* / *La vraie question n'est pas X* (rhétorique de redirection)
- *X n'est pas A mais B* (« rebalanced sentence », souvent posée avec un aparté entre tirets cadratins)

**Problème** : ces structures rhétoriques en miroir reviennent en boucle dans les textes IA. Elles « sonnent bien » mais ne disent rien : elles définissent ce que la chose n'est pas plutôt que d'affirmer ce qu'elle est. Un humain dit directement ce qu'il pense.

**Avant**
> Ce n'est pas un simple outil de gestion, c'est un véritable partenaire stratégique. Non seulement il optimise vos workflows, mais il transforme aussi votre culture d'équipe. Pas par hasard, pas par chance. Par design. Le vrai sujet n'est pas la productivité, c'est la collaboration.

**Après**
> L'outil sert à gérer les workflows. Les équipes qui l'utilisent ont changé leur façon de prioriser leurs sprints.

---

### 9. Triades systématiques

**Problème** : l'IA force les énumérations à trois éléments pour faire « complet ».

**Avant**
> Notre solution est rapide, efficace et fiable. Elle est conçue pour être innovante, performante et durable. Elle s'adresse aux particuliers, aux entreprises et aux institutions.

**Après**
> Notre solution est rapide. Elle est utilisée par 200 entreprises depuis le lancement.

---

### 10. Anaphores rythmées

**Tournures à surveiller** :
- *Pour celles qui… Pour celles qui… Pour celles qui…*
- *Parce que… Parce que… Parce que…*
- *Quand… Quand… Quand…*
- *Plus de X. Plus de Y. Plus de Z.*

**Problème** : l'IA en français adore l'anaphore (répétition d'une même formule en début de phrases ou de puces) pour produire un effet rythmique « inspirant », typique du registre marketing/branding. C'est très rare dans une vraie conversation et ça sonne immédiatement publicité.

**Avant**
> Pour celles qui osent. Pour celles qui inventent. Pour celles qui ne renoncent jamais. Notre marque est faite pour vous.

**Après**
> Notre marque s'adresse aux femmes qui veulent essayer des choses nouvelles, sans complexe.

---

### 11. Variation élégante (synonymie excessive)

**Problème** : l'IA évite la répétition à tout prix, en cyclant des synonymes qui rendent le texte difficile à suivre.

**Avant**
> Le protagoniste affronte plusieurs épreuves. Le personnage principal doit surmonter ces obstacles. Le héros finit par triompher. Notre homme rentre chez lui.

**Après**
> Le protagoniste affronte plusieurs épreuves, finit par les surmonter et rentre chez lui.

---

### 12. Fausses gammes (« de X à Y »)

**Tournures à surveiller** : de X à Y, en passant par Z. Qu'il s'agisse de X ou de Y. Du X au Y.

**Problème** : on encadre par deux extrêmes pour donner l'illusion de la complétude, alors que X et Y ne sont pas sur la même échelle.

**Avant**
> De la stratégie produit à l'expérience utilisateur, en passant par la gouvernance des données, notre approche couvre l'ensemble des enjeux.

**Après**
> On intervient sur trois sujets : la roadmap produit, l'UX, et la gouvernance data.

---

### 13. Connecteurs académiques en pluie

**Connecteurs à surveiller** : Par ailleurs, De plus, En outre, De surcroît, Néanmoins, Toutefois, Cependant, En effet, Ainsi, Par conséquent, En définitive, Force est de constater

**Problème** : l'IA française commence chaque paragraphe (et souvent chaque phrase) par un connecteur logique lourd. Quatre fois sur cinq, on peut le supprimer sans rien perdre.

**Avant**
> Le marché évolue rapidement. Par ailleurs, les attentes des clients changent. De plus, la concurrence se renforce. En outre, les réglementations se durcissent. Cependant, des opportunités émergent.

**Après**
> Le marché évolue vite. Les attentes des clients changent, la concurrence se renforce, les règles aussi. Il reste des opportunités.

---

### 14. Tournures pseudo-soutenues

**Tournures à surveiller** : il convient de noter que, force est de constater que, dans cette optique, dans ce cadre, à cet égard, en définitive, à l'aune de, au regard de, à l'issue de, dans la mesure où

**Problème** : registre faux-soutenu, typique de l'IA-FR qui essaie de « faire académique ».

**Avant**
> Il convient de noter que, dans cette optique, force est de constater que les résultats, à l'aune des objectifs initiaux, dépassent les attentes.

**Après**
> Les résultats dépassent ce qu'on attendait.

---

## CALQUES DE L'ANGLAIS

### 15. Transitions pseudo-journalistiques

**Tournures à surveiller** : *est moins X qu'on ne le pense*, *est plus Y qu'il n'y paraît*, *cache une réalité plus nuancée*, *la vérité est plus complexe*, *en apparence X, mais en réalité Y*, *derrière les chiffres se cache*

**Problème** : transitions de type magazine ou article long format, qui annoncent une nuance avant de la livrer. Un humain dit directement la nuance, sans préambule rhétorique.

**Avant**
> La campagne a généré 1 557 visites, mais la qualité de ces visites est plus modeste qu'on ne le pense. Derrière les chiffres se cache une réalité plus nuancée.

**Après**
> La campagne a généré 1 557 visites, mais 80 % d'entre elles ont duré moins de 10 secondes.

---

### 16. Anglicismes IA

**Anglicismes à surveiller** : adresser un problème (au lieu de *traiter*), faire du sens (au lieu d'*avoir du sens*), supporter (au lieu de *prendre en charge*), délivrer de la valeur (au lieu d'*apporter*), implémenter (souvent excessif, *mettre en place* ou *coder* selon le contexte), drive (au lieu de *piloter* ou *mener*), basé sur (au lieu de *fondé sur* ou *à partir de*, calque de *based on*), matcher, sourcer

**Problème** : entraînée majoritairement sur des données anglaises, l'IA traduit littéralement. Ces calques trahissent l'origine.

**Avant**
> Notre approche permet d'adresser les problématiques métier en délivrant de la valeur basée sur les besoins clients. Cette solution supporte tous les cas d'usage.

**Après**
> Notre outil traite les cas métier les plus fréquents. Il prend en charge la facturation, la relance, et la clôture mensuelle.

---

### 17. Calques syntaxiques

**Marqueurs à surveiller** : virgule avant *et* dans une énumération (calque de la *Oxford comma*), inversion *bien que + indicatif* (calque), *prendre en considération* (au lieu de *tenir compte de*), *en termes de X* (au lieu de *pour X* ou *côté X*).

**Avant**
> En termes de performance, notre solution est rapide, fiable, et facile à utiliser, bien que des améliorations sont prévues.

**Après**
> Côté performance, notre outil est rapide et fiable. On prévoit des améliorations.

---

## CONTENU

### 18. Inflation de l'importance, de l'héritage, des tendances

**Mots à surveiller** : marque un tournant, moment charnière, étape cruciale, témoigne de, s'inscrit dans une dynamique de, héritage durable, paysage en pleine évolution, à l'aube de, à l'ère de, dans un monde en perpétuelle mutation, véritable révolution

**Problème** : l'IA gonfle l'importance d'un sujet en le reliant à des « grandes tendances ».

**Avant**
> La création de l'Institut statistique de Catalogne en 1989 marque un tournant majeur dans l'évolution des statistiques régionales en Espagne. Cette initiative s'inscrit dans une dynamique plus large de décentralisation administrative.

**Après**
> L'Institut statistique de Catalogne a été créé en 1989 pour publier des statistiques régionales sans dépendre de l'institut national.

---

### 19. Inflation de notoriété et de couverture médiatique

**Tournures à surveiller** : couverture indépendante, médias nationaux et internationaux, plébiscité par la presse, présence active sur les réseaux sociaux

**Problème** : l'IA empile des médias et des chiffres pour gonfler la crédibilité, sans contexte.

**Avant**
> Ses analyses ont été reprises par Le Monde, Les Échos, BFM Business et France Inter. Elle dispose d'une présence active sur les réseaux sociaux avec plus de 200 000 abonnés.

**Après**
> Dans une tribune au Monde en 2024, elle défend une régulation de l'IA fondée sur les usages, pas sur les modèles.

---

### 20. Analyses superficielles en participe présent

**Tournures à surveiller** : soulignant, mettant en lumière, témoignant de, illustrant, reflétant, contribuant à, permettant de, favorisant, ouvrant la voie à, traduisant

**Problème** : l'IA accroche un participe présent en fin de phrase pour ajouter du faux fond. À supprimer presque toujours.

**Avant**
> La palette de couleurs bleu, vert et or fait écho aux paysages naturels de la région, symbolisant les fleurs locales et la mer, témoignant du lien profond de la communauté avec son territoire.

**Après**
> Les couleurs (bleu, vert, or) reprennent celles des fleurs locales et de la mer, selon l'architecte.

---

### 21. Langage promotionnel

**Mots à surveiller** : nichée au cœur de, écrin de verdure, joyau, véritable havre, riche patrimoine, à couper le souffle, dépaysement garanti, incontournable, vibrant, dynamique, charme authentique, hors du temps

**Problème** : registre brochure touristique. L'IA tombe dedans dès qu'on lui parle de patrimoine, de ville, de culture, ou d'entreprise.

**Avant**
> Nichée au cœur de la vallée, cette ville incontournable est un véritable joyau au riche patrimoine, offrant un dépaysement à couper le souffle.

**Après**
> La ville compte 8 000 habitants. Son église romane du XIIᵉ siècle est classée depuis 1932.

---

### 22. Attributions floues

**Tournures à surveiller** : selon les experts, les analystes s'accordent, plusieurs sources indiquent, des observateurs estiment, la communauté reconnaît

**Problème** : l'IA invoque des autorités vagues plutôt que de citer une source précise.

**Avant**
> Selon plusieurs experts, cette technologie joue un rôle clé dans l'écosystème.

**Après**
> Une étude de l'INRIA publiée en 2024 mesure un gain de productivité de 18 % sur les tâches de refactoring.

---

### 23. Sections « Défis et perspectives »

**Plans à surveiller** : Défis et perspectives, Enjeux et avenir, Perspectives d'avenir, Conclusion, Héritage

**Problème** : l'IA termine très souvent par une section formatée défis + avenir, vide de contenu réel.

**Avant**
> Malgré sa croissance, la ville fait face à des défis typiques des zones urbaines, notamment la congestion routière et la pression foncière. Malgré ces défis, grâce à sa position stratégique et à ses initiatives en cours, elle continue de prospérer.

**Après**
> La circulation s'est dégradée après 2018 avec l'ouverture de deux nouvelles zones d'activité. La municipalité a lancé en 2023 un plan vélo pour désengorger le centre.

---

## STYLE & MISE EN FORME

### 24. Surutilisation du tiret cadratin

**Problème** : l'IA utilise les tirets cadratins beaucoup plus que les francophones natifs. En français, le tiret cadratin reste rare en dehors du dialogue, donc encore plus suspect qu'en anglais.

**Avant**
> Cette approche, promue par les institutions, n'est pas portée par les utilisateurs eux-mêmes. On ne dit pas « France, Europe » dans une adresse, et pourtant ce malentendu persiste, même dans les documents officiels.

**Après**
> Cette approche est promue par les institutions, pas par les utilisateurs eux-mêmes. On ne dit pas « France, Europe » dans une adresse, et pourtant ce malentendu persiste, même dans les documents officiels.

(version déjà corrigée : virgules au lieu de tirets cadratins)

---

### 25. Surutilisation du gras

**Problème** : l'IA met en gras des termes au hasard, mécaniquement.

**Avant**
> Notre méthode mêle **OKR (Objectives and Key Results)**, **KPI (Key Performance Indicators)** et des outils visuels comme le **Business Model Canvas (BMC)** et le **Balanced Scorecard (BSC)**.

**Après**
> Notre méthode mêle OKR, KPI et des outils visuels comme le Business Model Canvas et le Balanced Scorecard.

---

### 26. Listes à puces avec en-tête en gras

**Problème** : listes formatées en *en-tête en gras suivi de deux-points*, signature visuelle des LLM (tous modèles confondus).

**Avant**
> - **Expérience utilisateur :** L'interface a été significativement améliorée.
> - **Performance :** Les performances ont été optimisées via de nouveaux algorithmes.
> - **Sécurité :** La sécurité a été renforcée avec un chiffrement de bout en bout.

**Après**
> La nouvelle version refait l'interface, accélère le chargement avec un nouvel algorithme de cache, et ajoute le chiffrement de bout en bout.

---

### 27. Émojis décoratifs

**Problème** : l'IA décore titres et puces d'émojis (fusées, ampoules, cases à cocher).

**Avant**
> 🚀 **Lancement :** Le produit sort au T3
> 💡 **Insight clé :** Les utilisateurs préfèrent la simplicité
> ✅ **Prochaines étapes :** Programmer un suivi

**Après**
> Le produit sort au T3. Les retours utilisateurs montrent une préférence pour les interfaces simples. Prochaine étape : programmer un suivi.

---

### 28. Typographie française cassée

L'IA en français maltraite la typographie. Cinq erreurs typiques :

**A. Guillemets droits ou anglais au lieu des guillemets français**

Trois variantes possibles :
- Droits ASCII : `"le projet avance"` (par défaut clavier)
- Courbes anglaises : `"le projet avance"` (U+201C / U+201D, typique des copier-coller depuis une IA conversationnelle)
- Français : `« le projet avance »` (U+00AB / U+00BB, avec espaces insécables à l'intérieur)

Avant : `Il a dit "le projet avance".`
Après : `Il a dit « le projet avance ».`

**B. Espace insécable manquante avant `:`, `;`, `?`, `!`**

Avant : `Voici le résultat: c'est validé!`
Après : `Voici le résultat : c'est validé !` (espace insécable U+00A0 avant `:` et `!`)

**C. Apostrophe droite au lieu de la courbe**

Avant : `L'équipe a livré.` (apostrophe droite `'`)
Après : `L'équipe a livré.` (apostrophe courbe `'`, U+2019). Acceptable selon le contexte (web, code), mais l'IA est souvent incohérente entre les deux dans un même texte.

**D. Virgule avant *et* (calque de la virgule d'Oxford)**

Avant : `On a livré la spec, le code, et les tests.`
Après : `On a livré la spec, le code et les tests.`

**E. Accents oubliés ou incohérents**

L'IA en français (Claude inclus) oublie régulièrement les accents. Trois cas typiques :

*E.1 Accents sur les majuscules.* En français, les majuscules s'accentuent (règle de l'Académie française). L'IA les oublie souvent en début de phrase ou dans les titres.

Avant : `Etat des lieux. Apres trois mois, l'equipe a livré.`
Après : `État des lieux. Après trois mois, l'équipe a livré.`

Cas fréquents : *À, É, È, Ê, Ç, Ô, Î* en début de phrase ou dans les titres (*À propos*, *École*, *État*, *Évolution*, *Édition*).

*E.2 Mots fréquents sans accent.* L'IA confond ou oublie sur des mots courants.

Avant : `Ou est-ce que ca se trouve? La ou tu as cherche.`
Après : `Où est-ce que ça se trouve ? Là où tu as cherché.`

Couples à surveiller : *où / ou*, *à / a*, *là / la*, *ça / ca*, *çà / ca*, *dû / du*, *sûr / sur*.

*E.3 Incohérence dans un même texte.* Le pire signal IA : des accents présents dans un paragraphe, absents dans le suivant. Un humain est cohérent (toujours ou jamais), une IA dérive.

Avant : `L'équipe a livré le projet à temps. Apres validation, on passe a la phase suivante.`
Après : `L'équipe a livré le projet à temps. Après validation, on passe à la phase suivante.`

---

## COMMUNICATION

### 29. Artefacts conversationnels

**Tournures à surveiller** : Bien sûr !, Avec plaisir !, Voici…, J'espère que cela vous aide, N'hésitez pas à…, Souhaitez-vous que je…

**Problème** : du texte de chatbot copié-collé dans un contenu final.

**Avant**
> Voici un aperçu de la Révolution française. J'espère que cela vous aide ! N'hésitez pas à me demander si vous souhaitez que j'approfondisse une partie.

**Après**
> La Révolution française commence en 1789, dans un contexte de crise financière et de pénuries alimentaires.

---

### 30. Avis de coupure de connaissance

**Tournures à surveiller** : à ma dernière mise à jour, selon les informations disponibles, bien que les détails précis ne soient pas largement documentés, sur la base des données accessibles

**Problème** : l'IA injecte ses propres limites dans le texte produit.

**Avant**
> Bien que les détails précis sur la fondation de l'entreprise ne soient pas largement documentés dans les sources accessibles, elle semble avoir été créée dans les années 1990.

**Après**
> L'entreprise a été créée en 1994, selon ses statuts déposés.

---

### 31. Ton flatteur ou servile

**Tournures à surveiller** : Excellente question !, Vous avez tout à fait raison, C'est une remarque très pertinente, Bien vu !

**Problème** : ton complaisant, par défaut chez la plupart des assistants IA.

**Avant**
> Excellente question ! Vous avez tout à fait raison de soulever ce point, c'est un sujet vraiment passionnant.

**Après**
> Ce point soulève un vrai problème : la définition même de la donnée n'est pas partagée entre les équipes.

---

## DÉLAYAGE & FLOU

### 32. Auto-validation rhétorique

**Tournures à surveiller** : *et c'est précisément le but*, *et c'est tout l'enjeu*, *c'est exactement ce que…*, *voilà toute la question*, *voilà l'idée*, *c'est là que tout se joue*, *c'est précisément pour cela que*

**Problème** : l'IA pose une affirmation, puis se félicite à voix haute de l'avoir posée avec une formule du type *« et c'est précisément le but »*. C'est une signature rhétorique qui clôt une idée par une auto-confirmation, sans rien apporter de plus. Un humain dit la chose et passe à autre chose.

**Avant**
> Notre méthode oblige à reformuler le besoin avant d'écrire la moindre ligne de code. Et c'est précisément le but : éviter de coder la mauvaise solution. Voilà tout l'enjeu.

**Après**
> Notre méthode oblige à reformuler le besoin avant d'écrire la moindre ligne de code, pour éviter de coder la mauvaise solution.

---

### 33. Méta-annonces

**Tournures à surveiller** : *Voici ce qu'on en sait clairement*, *Voici les éléments clés*, *Pour bien comprendre*, *Avant d'aller plus loin*, *Commençons par*, *Pour résumer la situation*, *Voici l'essentiel*

**Problème** : l'IA annonce ce qu'elle va dire avant de le dire. Préambule auto-référentiel inutile. Un humain attaque directement le contenu.

**Avant**
> Voici ce qu'on en sait clairement sur la situation actuelle du marché : trois grandes tendances se dessinent.

**Après**
> Trois tendances se dessinent sur le marché en ce moment.

---

### 34. Posture didactique

**Tournures à surveiller** : *Ce qu'il faut comprendre, c'est que*, *Il faut savoir que*, *Notez que*, *Gardez à l'esprit que*, *Retenez ceci*, *N'oublions pas que*, *Il est essentiel de comprendre*

**Problème** : l'IA se met en posture de prof face à un élève. En contexte pro entre adultes, on ne dit pas à son interlocuteur ce qu'il « faut » comprendre, on lui présente l'info et on le laisse en tirer ses conclusions. Cette posture didactique est condescendante et révèle l'IA.

**Avant**
> Ce qu'il faut comprendre, c'est que cette campagne avait pour objectif principal le trafic. Il faut savoir que les KPIs n'étaient donc pas les mêmes que pour une campagne de conversion.

**Après**
> Cette campagne visait du trafic, pas de la conversion. Les KPIs sont donc différents.

---

### 35. Phrases creuses (filler)

**Avant → Après**
- *Afin de pouvoir atteindre cet objectif* → *Pour atteindre cet objectif*
- *Dans le cadre de la mise en place de cette démarche* → *Pour cette démarche*
- *À l'heure actuelle* → *Aujourd'hui* (ou rien)
- *Au sein de l'organisation* → *Dans l'entreprise*
- *Dans la mesure où il pleuvait* → *Comme il pleuvait*
- *Le système a la capacité de traiter* → *Le système traite*
- *Il est important de noter que les données montrent* → *Les données montrent*
- *Force est de constater que* → ∅

---

### 36. Sur-qualification (hedging)

**Problème** : empilement de modalisateurs (*pourrait*, *peut-être*, *possible*) qui vide la phrase.

**Avant**
> On pourrait potentiellement penser qu'il est possible que cette politique puisse avoir un certain impact sur les résultats.

**Après**
> Cette politique peut avoir un effet sur les résultats.

---

### 37. Conclusions positives génériques

**Tournures à surveiller** : l'avenir s'annonce prometteur, les perspectives sont enthousiasmantes, un bel avenir se dessine, en définitive, une étape importante a été franchie

**Problème** : conclusion vide qui ne dit rien.

**Avant**
> L'avenir s'annonce prometteur pour l'entreprise. Les perspectives sont enthousiasmantes et de belles étapes restent à franchir sur ce chemin vers l'excellence.

**Après**
> L'entreprise prévoit d'ouvrir deux bureaux en 2026.

---

### 38. Registre pseudo-littéraire (mièvre)

**Tournures à surveiller** : promesse murmurée, instant suspendu, secret brûlant, désir vibrant, comme si le temps s'était figé, comme une promesse oubliée

**Problème** : quand on demande à l'IA un texte « littéraire », elle tombe dans un registre mièvre, plein de comparaisons en *comme si* et de noms abstraits accolés à des participes émotionnels. Spécifique aux générations FR créatives.

**Avant**
> Il la regarda, comme si le temps s'était figé. Une promesse murmurée, un secret brûlant entre eux, vibrant dans le silence.

**Après**
> Il la regarda. Personne n'a parlé pendant une bonne minute.

---

## PROCESSUS

1. Lire le texte d'entrée
2. Repérer toutes les occurrences des marqueurs ci-dessus
3. Réécrire chaque passage problématique
4. Vérifier que la version révisée :
   - sonne juste à voix haute
   - varie ses structures de phrase
   - donne des détails concrets plutôt que des affirmations vagues
   - garde le ton attendu pour le contexte
   - utilise *est* / *sont* / *a* quand c'est possible
   - utilise une typographie française correcte (« » avec espaces insécables)
5. Présenter une première version humanisée
6. Se demander : « qu'est-ce qui sonne encore IA dans ce texte ? »
7. Répondre brièvement (s'il reste des marques)
8. Se demander : « comment faire pour que ce ne soit plus du tout IA ? »
9. Présenter la version finale (revue après l'audit)

## Format de sortie

Fournir :
1. Première réécriture
2. « Qu'est-ce qui sonne encore IA dans ce texte ? » (puces brèves)
3. Version finale
4. Bref récap des changements (optionnel, si utile)

---

## Exemple complet

Contexte : page « À propos » d'une fromagerie artisanale qui veut présenter son activité sur son site web.

**Avant (sonne IA)**
> Bienvenue chez Fromagerie Lavalle ! Nous sommes ravis de vous présenter notre histoire.
>
> Nichée au cœur du Pays d'Auge, la Fromagerie Lavalle constitue une véritable référence dans le paysage fromager français, marquant un tournant majeur dans la préservation des savoir-faire artisanaux à l'aube d'une nouvelle ère pour la gastronomie. Depuis sa création, notre maison s'inscrit dans une dynamique d'excellence, témoignant d'un attachement profond au territoire et incarnant un véritable héritage durable.
>
> Notre approche est simple : permettre à chacun de redécouvrir des fromages authentiques et savoureux. Ce n'est pas qu'une simple production fromagère, c'est une véritable invitation au voyage des sens. Notre méthode constitue un savoir-faire. Notre cave fait figure de sanctuaire. Notre équipe s'impose comme la gardienne d'une tradition séculaire.
>
> Par ailleurs, plusieurs observateurs s'accordent à reconnaître la qualité exceptionnelle de notre production. Notre maison a été plébiscitée par Le Figaro Madame, Le Gault & Millau et France Bleu Normandie. De plus, notre capacité à allier tradition et modernité illustre comment un artisan peut contribuer à la valorisation du patrimoine, soulignant l'interaction subtile entre héritage et innovation.
>
> - 🧀 **Tradition :** Des recettes transmises de génération en génération, garantissant l'authenticité.
> - 🌿 **Terroir :** Un lait collecté localement, témoignant de notre engagement pour le territoire.
> - ✅ **Qualité :** Une démarche rigoureuse, contribuant à des produits d'exception.
>
> Bien que les détails précis sur les origines de la fromagerie soient limités sur la base des informations disponibles, il pourrait potentiellement être avancé que notre maison aurait été fondée dans la première moitié du XXᵉ siècle. Malgré les défis typiques des artisans face à l'industrialisation, l'écosystème fromager continue de prospérer. Afin de pouvoir poursuivre cette aventure, nous sommes en mesure d'adresser les besoins d'une clientèle de plus en plus exigeante.
>
> En conclusion, l'avenir s'annonce prometteur. De belles perspectives se dessinent pour notre maison sur ce chemin vers l'excellence. N'hésitez pas à nous contacter si vous souhaitez en savoir plus !

**Première réécriture**
> La fromagerie Lavalle est installée à Beuvron-en-Auge depuis 1936. Trois générations s'y sont succédé. Nous fabriquons quatre fromages : un camembert au lait cru, un livarot, un pont-l'évêque et un pavé d'Auge.
>
> Le lait vient de deux fermes voisines, à moins de huit kilomètres. Les vaches sont en pâturage neuf mois sur douze. On travaille en petites quantités, environ 200 fromages par jour, ce qui permet de garder un moulage à la louche et un affinage en cave humide.
>
> Notre camembert a été médaillé d'argent au Concours général agricole en 2023. Le livarot a été repris dans le guide Gault & Millau Fromages 2024.
>
> La fromagerie est ouverte du mardi au samedi, 9 h à 18 h. On accueille aussi des visites de la cave d'affinage le jeudi sur réservation.

**Qu'est-ce qui sonne encore IA dans ce texte ?**
- Le rythme est un peu trop régulier (quatre paragraphes de longueur similaire).
- Les chiffres et dates sont alignés un peu mécaniquement.
- Le ton reste très « page web officielle », pas vraiment une voix.

**Version finale**
> La fromagerie est à Beuvron-en-Auge depuis 1936. Mon grand-père a démarré en livrant à vélo les hôtels de Cabourg. Aujourd'hui je fais quatre fromages : camembert au lait cru, livarot, pont-l'évêque, et un pavé d'Auge que mon père a mis au point dans les années 80.
>
> Le lait vient de deux fermes à côté, à huit kilomètres maximum. Les vaches sont dehors neuf mois sur douze, et ça change tout pour le goût, surtout au printemps. On reste en petite quantité, environ 200 fromages par jour. C'est ce qui permet de mouler à la louche et d'affiner en cave humide, à l'ancienne.
>
> Le camembert a eu une médaille d'argent au Concours agricole en 2023, et le livarot a été repris dans le Gault & Millau l'année dernière. Ça fait plaisir, mais ce qui compte, c'est ce que disent les clients qui reviennent toutes les semaines.
>
> Ouvert du mardi au samedi, 9 h à 18 h. Visite de la cave le jeudi, sur réservation.

**Changements faits**
- Retiré les artefacts conversationnels (« Bienvenue chez… », « Nous sommes ravis », « N'hésitez pas… »)
- Retiré le langage promotionnel (« nichée au cœur de », « véritable référence », « écrin », « invitation au voyage des sens »)
- Retiré l'inflation d'importance (« tournant majeur », « à l'aube d'une nouvelle ère », « héritage durable »)
- Retiré l'évitement de *être* (« constitue », « incarne », « fait figure de », « s'impose comme »)
- Retiré les triades (« savoir-faire / sanctuaire / gardienne », « rapide / efficace / fiable »)
- Retiré les attributions floues (« plusieurs observateurs s'accordent »)
- Retiré les participes présents fourre-tout (« témoignant », « soulignant », « contribuant », « garantissant »)
- Retiré le parallélisme négatif (« Ce n'est pas qu'une simple X, c'est une véritable Y »)
- Retiré la liste à puces avec emojis et en-têtes en gras
- Retiré la section « Défis et perspectives »
- Retiré l'avis de coupure de connaissance (« Bien que les détails soient limités… »)
- Retiré la sur-qualification (« il pourrait potentiellement être avancé que… aurait été »)
- Retiré le délayage (« Afin de pouvoir », « être en mesure de »)
- Retiré l'anglicisme (« adresser les besoins »)
- Retiré la conclusion vide (« l'avenir s'annonce prometteur », « chemin vers l'excellence »)
- Mis des faits concrets à la place (date, distance, médaille, horaires, anecdote du grand-père)
- Donné une voix personnelle (« je », anecdote familiale, opinion sur ce qui compte vraiment)

---

## Références

Ce skill s'appuie sur des sources francophones, pas sur une traduction du guide anglais.

- [Aide:Identifier l'usage d'une IA générative — Wikipédia FR](https://fr.wikipedia.org/wiki/Aide:Identifier_l%27usage_d%27une_IA_g%C3%A9n%C3%A9rative) : guide officiel de la communauté Wikipédia francophone, équivalent du *WikiProject AI Cleanup*.
- [Projet:Observatoire des IA — Wikipédia FR](https://fr.wikipedia.org/wiki/Projet:Observatoire_des_IA/Documentation) : observatoire francophone des contenus IA sur Wikipédia, créé en octobre 2024.
- [Wikipédia:Sondage/Intelligence artificielle générative](https://fr.wikipedia.org/wiki/Wikip%C3%A9dia:Sondage/Intelligence_artificielle_g%C3%A9n%C3%A9rative) : positions de la communauté FR sur les contributions IA.
- [40 marqueurs linguistiques qui trahissent ton écriture (Isma)](https://redigeretvendreavecia.substack.com/p/40-marqueurs-linguistiques-qui-trahissent) : catalogue opérationnel des tics IA en français.
- [Les tics de langage de ChatGPT (Daria décrypte l'IA)](https://dariadecrypteia.substack.com/p/les-tics-de-langage-de-chatgpt) : focus connecteurs lourds et anglicismes.
- [Reconnaître un texte d'IA : les tics de ChatGPT (Loumina)](https://www.loumina.fr/blog-reconnaitre-un-texte-d-ia-les-tics-de-chatgpt) : registre pseudo-littéraire et structures émotionnelles standardisées.
- [Comment savoir si un texte a été généré par ChatGPT (Digitad)](https://digitad.ca/comment-savoir-texte-genere-par-chatgpt/) : perspective québécoise, anglicismes et doublets d'adjectifs.
- [La réception de ChatGPT au sein de Wikipédia (UQAM)](https://collimateur.uqam.ca/collimateur/la-reception-de-chatgpt-au-sein-de-wikipedia/) : analyse universitaire de la réponse de la communauté Wikipédia FR à l'IA générative.
- [Wikipedia:Signs of AI writing](https://en.wikipedia.org/wiki/Wikipedia:Signs_of_AI_writing) : guide anglais qui a inspiré la structure générale, mais dont le lexique et les exemples ne sont pas transposables tels quels.

Idée centrale, partagée par toutes ces sources : un LLM produit ce qui est statistiquement le plus probable. Le résultat est lisse, neutre, sans aspérités, et tombe dans les mêmes marqueurs à chaque fois. Humaniser un texte, c'est y remettre des choix qui ne sont pas les plus probables.
