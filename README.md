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
**CREATEURS PRINCIPAUX**. ***Titre***. Type de rapport n° Numéro de rapport. Volume \[Medium\]. Genre. Créateurs secondaires. **Edition**. **Lieu** : **Editeur**. Numéro (brevets uniquement). **Date**. **\[Consulté le Date d'accès\]**. Collection. **ISBN**. **URL ou DOI**. Archive : localisation ou cote. Notes
Ressource incluse dans une ressource hôte
**CREATEURS PRINCIPAUX**. **Titre**. Dans : **CREATEURS DE LA RESSOURCE HÔTE**. ***Titre***. Volume \[Medium\]. Genre. Créateurs secondaires. **Edition**. **Lieu** : **Editeur**. **Date**. **\[Consulté le Date d'accès\]**. Collection. **ISBN**. **URL ou DOI**. Archive : localisation ou cote. Notes

FIXME : clarifier genre et medium dans le code

**Créateurs principaux** :
Les noms précèdent les prénoms, avec une virgule en séparateur. Les différents auteurs sont séparés par des virgules, sauf le dernier, introduit par "et". Deux types de créateurs sont gérés : "auteur" et "éditeur". S'il existe au moins un "auteur", seuls les auteurs seront mentionnés. Sinon, s'il existe au moins un éditeur, seuls les "éditeurs" seront mentionnés. LEs autres types d'auteurs sont traités en créateurs secondaires.
Dans les notes, seuls 3 créateurs sont mentionnés. Dans la bibliographie, tous les auteurs le sont.
Le nom des "éditeurs" est suivi de la mention (dir.)
Exceptions : pour les brevets, l'"auteur" au sens de Zotero est en fait un inventeur, qui doit figurer en Créateur secondaire.
Ex:
NOM, Prénom
NOM1, Prénom, NOM2, Prénom et NOM3, Prénom
NOM, Prénom (dir.)
NOM1, Prénom, NOM2, Prénom, NOM3, Prénom, NOM4, Prénom (dir.)


**Dates** :
la plus complète possible, en fonction des données présentes dans Zotero, sur le modèle "30 juillet 2014".
En cas de date inconnue: \[s.d.\]
Pas de gestion des dates incertaines ni des tranches de dates


A traduire et markdowniser :

- if the cited ressource is a volume of a multivolume book or monograph, the volume is given after the title
- if report genre and number are present, they are given after the title. If a report number exists but no report genre, the generic term 'rapport' is used
- no mention of subsidiary creators after the title, except for patent inventors, with prefix "Inventeur(s)"
- if missing, publisher place and publisher are replaced with \[s.l.\] and \[s.n.\], only for some types (book, thesis, map, chapter...)
- if a precise passage is cited in the note, the "locator" is given after the date. It can replace the pagination of a chapter or article
- if the complete pagination of a book or monograph is present in Zotero, it is NOT displayed
- if present, series name and number are given, but only in the final bibliography
- 'Dans:' is used instead of "In:"
- 'Dans' is used before the title of host ressources (in a book, website...), except before serials title
- if the bibliographic data for a contribution does not include the title of the host ressource, the contribution title is in italic, and 'Dans:' is not displayed
- if a doi and an URL are given, only the doi is displayed
- if present, archive, archive location and call number are given after the doi/URL
- if present, the note is given at the end of the reference
