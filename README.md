# Nouveaux styles CSL pour Zotero
## iso690-note-fr
**Description** :

Style compatible avec la norme ISO 690, permettant des citations en notes, avec une bibliographie finale, basé sur la version ISO 690 "author-date" écrite par Mellifluo, Grolimund, Hardegger et Giraud.
Ne gère pas les "op.cit" et "ibid" (les références sont répétées)

**Choix dans l'interprétation de la norme** :

Les références sont **structurées de manière identique dans les notes et la bibliographie**, à deux exceptions près :

- tous les auteurs principaux sont donnés dans la bibliographie, seulement les trois premiers (suivis de "et al.") dans les notes

- la collection n'est donnée que dans la bibliographie

**Ponctuation** :

Les élements constituant les références sont en général séparés par un point (.), sauf quelques exceptions. Les titres des ressources "hôtes" ne sont pas introduites par des guillemets. Les éléments ne figurant pas sur la ressources sont encadrés par des crochets carrés (\[\]). Les fonctions des créateurs principaux sont entre parenthèses.

**Typographie**

Le nom des créateurs principaux est en majuscules. Les titres sont en italique sauf si la ressource citée est incluse dans une ressource hôte (dans ce cas, celle-ci est en italique)

**Ordre général** :

Les éléments obligatoires selon la norme sont en **gras**.

Ressource non incluse dans une ressource hôte:

**NOM, Prénom des créateurs principaux (fonction)**. ***Titre*** : Type de rapport n° Numéro de rapport. Volume \[Medium\]. Genre. Fonction des créateurs secondaires Prénom NOM des créateurs secondaires. **Edition**. **Lieu** : **Editeur**. Numéro (brevets uniquement). **Date**. **\[Consulté le Date d'accès\]**. Collection. **ISBN**. **URL ou DOI**. Archive : localisation ou cote. Notes
Ressource incluse dans une ressource hôte

**NOM, Prénom des créateurs principaux (fonction)**. **Titre**. Dans : **CREATEURS DE LA RESSOURCE HÔTE**. ***Titre***. Volume \[Medium\]. Genre. Fonction des créateurs secondaires Prénom NOM des créateurs secondaires. **Edition**. **Lieu** : **Editeur**. **Date**. **\[Consulté le Date d'accès\]**. Collection. **ISBN**. **URL ou DOI**. Archive : localisation ou cote. Notes

FIXME : clarifier genre et medium dans le code

**Créateurs principaux** :

Les noms sont en majuscules, et précèdent les prénoms, avec une virgule en séparateur. Les différents auteurs sont séparés par des virgules, sauf le dernier, introduit par "et". Deux types de créateurs sont gérés : "auteur" et "éditeur". S'il existe au moins un "auteur", seuls les auteurs seront mentionnés. Sinon, s'il existe au moins un éditeur, seuls les "éditeurs" seront mentionnés. Les autres types d'auteurs sont traités en créateurs secondaires.
Dans les notes, seuls 3 créateurs sont mentionnés. Dans la bibliographie, tous les auteurs le sont.

Le nom des "éditeurs" est suivi de la mention (dir.)

Exceptions : pour les brevets, l'"auteur" au sens de Zotero est en fait un inventeur, qui doit figurer en Créateur secondaire.

Ex:

NOM, Prénom

NOM1, Prénom, NOM2, Prénom et NOM3, Prénom

NOM, Prénom (dir.)

NOM1, Prénom, NOM2, Prénom, NOM3, Prénom, NOM4, Prénom (dir.)

**Créateurs secondaires** :

Les créateurs secondaires sont introduits par leur fonction (ex: "Trad. par"). Les noms sont en majuscules, et suivent les prénoms, avec un espace en séparateur. Les différents auteurs sont séparés par des virgules, sauf le dernier, introduit par "et". Deux types de créateurs sont gérés : "traducteur" et "auteur" (dans le cas d'un inventeur de brevet).
Dans les notes, seuls 3 créateurs sont mentionnés. Dans la bibliographie, tous les auteurs le sont.

Ex:

Inventeur : Prénom NOM

Inventeurs : Prénom NOM1 et Prénom NOM2

Trad. par Prénom NOM1, Prénom NOM2 et Prénom NOM3

**Volumes** :

Si la ressource citée est un volume d'un ouvrage publié en plusieurs volumes, le volume est donné après le titre. Si le champ volume contient un chiffre, le chiffre sera précédé de "Vol. ". S'il contient une expression plus complexe comme "Tome 3, vol. 2", l'expression sera reprise telle quelle

Ex : 

*Titre*. Vol. 2

**Types et numéro de rapport**:

Si la ressource est un rapport, et qu'un numéro et un type de rapports sont présents dans Zotero, le numéro sera cité, précédé du type et de "n°". Si un numéro est présent mais pas de type, le type générique "Rapport" sera utilisé. Si le type est présent mais pas le numéro, seul le type est affiché.

Ex : 

GOURAULT, Jacqueline et KALTENBACH, Philippe. **Les premiers enseignements du quinzième plan de lutte contre la précarité dans la fonction publique** : Rapport d’information n°772 (2013-2014) \[en ligne\]. Paris : Sénat, 23 juillet 2014. \[Consulté le 30 juillet 2014\].

**Dates** :

la plus complète possible, en fonction des données présentes dans Zotero : "Mois année" pour les articles et "jour mois année" pour les autre ressources, sur le modèle "30 juillet 2014".

En cas de date inconnue: \[s.d.\]

FIXME : Pas de gestion des dates incertaines ni des tranches de dates. Vérifier ce que donnent les dates entre crochets

**Lieux** et **Editeurs**:

Pour les types de documents book map thesis report chapter entry entry-dictionary entry-encyclopedia, en cas de lieu inconnu: \[s.l.\]. En cas d'éditeur inconnu: \[s.n.\]. En cas de lieu et d'éditeur inconnu : \[s.l. : s.n.\]

**Contributions dans des monographies et périodiques**

"Dans" est utilisé à la place de "In". Il n'est pas utilisé pour introduire les titres de périodiques (option de la norme).

Si la ressource citée appartient à un type qui suppose normalment la mention d'une ressource hôte, mais que l'information n'est pas saisie (cas fréquent avec le type webpage, pour lequel le titre du site est rarement saisi), la référence est traitée comme une référence à un ressource ne faisant pas partie d'une hôte : pas de "In:", et titre de la ressource citée en italique.

**URL et DOI**

Si un DOI est fourni, il doit être suffisant pour obtenir le document. Donc si l'URL est fournie également, elle n'est pas affichée.

**Pagination d'un livre**

Si la pagination complète d'un livre est présente dans Zotero dans le champ pages, elle n'est pas affichée, ni dans la bibliographie, ni dans les notes.

**Collection et numéro dans la collection**

La collection et la numérotation sont affichés dans la bibliographie finale, pas dans les notes.

**Archives, localisation dans l'archive, cote**

Si ces champs sont saisis, ils sont affichés en fin de référence.

**Notes

Si le champ Extra de Zotero contient des informations, elles sont affichées en tant que notes, en toute fin de référence.

**Passage précis cité en note**

Si un passage précis de la ressource est cité en note (page, section, chapitre, etc), la localisation du passage (le "locator") est affichée après la date, ou à la place de la pagination "normale" de la ressource (cas des articles et des chapitres).
Le passage précis n'est pas indiqué dans la bibliographie.

Ex 1: (citation de la page 226)

note : SELMI, Adel et JOLY, Pierre-Benoit. Les régimes de production des connaissances de la sélection animale. Ontologies, mesures, formes de régulation. ''Sociologie du Travail''. Avril 2014, Vol. 56, no 2, p. 226. DOI 10.1016/j.soctra.2014.03.020.


bibliographie : SELMI, Adel et JOLY, Pierre-Benoit. Les régimes de production des connaissances de la sélection animale. Ontologies, mesures, formes de régulation. ''Sociologie du Travail''. Avril 2014, Vol. 56, no 2, p. 225‑244. DOI 10.1016/j.soctra.2014.03.020.

Ex 2: (citation du chapitre 2)

note : ROCHE, Florence et SABY, Frédéric (dir.). L’avenir des bibliothèques: l’exemple des bibliothèques universitaires. Villeurbanne : Presses de l’Enssib, 2013, chap. 2. ISBN 979-10-91281-13-3.

bibliographie : ROCHE, Florence et SABY, Frédéric (dir.). L’avenir des bibliothèques: l’exemple des bibliothèques universitaires. Villeurbanne : Presses de l’Enssib, 2013. ISBN 979-10-91281-13-3.

Ex 3: (citation de la figure 3)

note : BENTON, Arthur et ANDERSON, Steven W. Aphasia: Historical Perspectives. Dans : SARNO, Martha Taylor (dir.), ''Acquired Aphasia''. 3e édition \[en ligne\]. San Diego : Academic Press, 1998, fig. 4. \[Consulté le 27 juillet 2014\]. ISBN 978-0-12-619322-0.

bibliographie : BENTON, Arthur et ANDERSON, Steven W. Aphasia: Historical Perspectives. Dans : SARNO, Martha Taylor (dir.), ''Acquired Aphasia''. 3e édition \[en ligne\]. San Diego : Academic Press, 1998, p. 1‑24. \[Consulté le 27 juillet 2014\]. ISBN 978-0-12-619322-0.

**Tri de la bibliographie**

Le tri se fait par auteurs, puis par titres.
