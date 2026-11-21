# Isaac Traducteur FR

Traducteur français pour **The Binding of Isaac: Repentance+**.
C'est un petit logiciel qui tourne en fond pendant que tu joues et affiche la
traduction des objets, cartes, pilules et babioles directement par-dessus le jeu,
sans le ralentir. Pas besoin de Python ni d'installation compliquée : un seul `.exe`.

---

## Démarrage rapide

1. **Télécharge** `IsaacTraducteurFR.exe`.
2. Mets-le dans un dossier à toi (Bureau, Documents ou Téléchargements). **Pas** dans
   `Program Files` (Windows y bloque les mises à jour automatiques).
3. **Double-clique** dessus. Une petite icône **« FR »** apparaît près de l'horloge
   (clique sur la flèche `^` si elle est cachée).
4. Lance le jeu. C'est tout : ramasse un objet, sa traduction s'affiche.

> **Premier lancement :** il faut une **connexion internet** quelques secondes, le
> temps de télécharger les traductions. Ensuite elles sont enregistrées et le logiciel
> marche sans internet (sauf la traduction du texte libre, voir plus bas).

> **Avertissement Windows :** l'exe n'est pas signé (logiciel perso). Au premier
> lancement, Windows peut afficher « Windows a protégé votre PC » →
> **Informations complémentaires → Exécuter quand même**. C'est normal et sans danger.

---

## Ce qu'il faut pour que ça marche

| | Version GRATUITE | Version COMPLÈTE (VIP) |
|---|---|---|
| **Le jeu** | Repentance+ | Repentance+ |
| **Internet** | Au 1er lancement (traductions) | Au 1er lancement |
| **Tesseract (lecture de texte)** | Pas nécessaire | **Recommandé** (bien meilleure lecture) |

La version **gratuite** fonctionne toute seule, sans rien installer de plus : elle lit
le journal du jeu et traduit les objets que tu ramasses.

La version **complète** utilise en plus la **lecture de l'écran (OCR)**. Pour qu'elle
soit précise, installe **Tesseract** (voir la section OCR).

---

## Comment ça marche

Le logiciel lit le **journal du jeu** (`log.txt`, généré automatiquement par Isaac).
Quand tu ramasses un objet, le jeu l'écrit dans ce journal ; le logiciel le repère et
affiche sa traduction. C'est pour ça que c'est léger et fluide : il ne « regarde » pas
l'écran en permanence, il lit juste un fichier texte.

La **lecture de l'écran (OCR)** ne sert que pour ce qui n'est pas dans le journal :
le texte affiché dans le jeu, les conditions de déblocage, les objets quand tu
t'en approches, etc. C'est la partie réservée à la version complète.

---

## Version gratuite vs version complète (VIP)

**GRATUIT, pour toujours :**
- Traduction des objets, cartes, pilules et babioles ramassés
- Bulle déplaçable où tu veux à l'écran
- Noms officiels de la version française
- **Choix de la langue** : français, anglais, espagnol, allemand, italien,
  portugais (BR), russe (clic droit → Langue de traduction)

**Version COMPLÈTE (soutien à 2 €) :**
- **Bulles au style du jeu** : panneau sombre aux bords déchirés et texte écrit à la
  main, comme les panneaux d'Isaac (la version gratuite garde la bulle parchemin)
- **Traduction à l'approche** : approche-toi d'un objet, sa traduction s'affiche
  (même les objets jamais débloqués, marqués « ??? »)
- **Suivi des transformations** : quand tu ramasses un objet qui compte pour une
  transformation (Guppy, Belzébuth, Léviathan, Séraphin…), la bulle montre
  l'avancement (`→ Belzébuth 2/3`), et t'annonce quand tu l'obtiens. Récap de la
  run à tout moment : clic droit sur l'icône → « Transformations de la run ».
- **Qualité cachée des objets** : chaque objet a une note de 0 à 4 que le jeu ne
  montre jamais (c'est elle que regardent les salles d'ange/de diable, le D4,
  etc.). La bulle l'affiche en tête : `Qualité 4/4 · objet surpuissant`.
- **Synergies avec ton build** : quand tu vois ou ramasses un objet, la bulle te dit
  s'il interagit avec un objet que tu as déjà, en bien ou en mal
  (« Effet annulé par Dr. Fetus », « Ipéca : le laser explose au contact… »).
  Fini les mauvaises surprises.
- **Astuces du wiki** (effets, synergies, notes) dans la recherche (F9)
- **Fenêtre F9 au style du jeu** : thème sombre, onglets et titres écrits à la main
- **Onglet Paramètres dans F9** : tous les réglages du clic droit au même endroit
  (cases à cocher, durée, taille, langue, mises à jour…)
- **Onglet Stats dans F9** : tableau de bord de tes runs, enregistrées
  automatiquement : run en cours avec son temps en direct, nombre de runs, temps de
  jeu, durée moyenne, record de profondeur, jusqu'où vont tes runs (Grottes,
  Profondeurs, Utérus…), persos les plus joués, objets les plus pris, dernières runs.
  (Le jeu n'écrit ni la mort ni la victoire dans son log : c'est l'étage le plus
  profond atteint qui compte.)
- **Scan de l'écran (F6)** : traduit n'importe quel texte affiché
- **Pilules et cartes** traduites automatiquement quand tu les utilises
- **Traduction du texte libre** du jeu
- **Mode streamer / OBS** : une page prête à ajouter dans OBS en « Source
  navigateur » (`http://localhost:17645`), qui affiche les traductions et les
  transformations en direct à ton audience (clic droit → Mode streamer / OBS)

**Donner ton avis :** clic droit → **« Donner mon avis / idée / signaler un bug »**.
Un petit formulaire envoie ton retour directement au créateur. N'hésite pas !

**Essai :** la version complète est débloquée gratuitement pendant tes **3 premières
parties**. Ensuite, elle se verrouille (la traduction des objets, elle, reste gratuite).

**Débloquer :** procure-toi une clé VIP, **copie-la** (Ctrl+C), puis **clic droit sur
l'icône FR → « Débloquer la version complète »**. C'est instantané.

---

## OCR : installer Tesseract (pour la version complète)

L'OCR, c'est la lecture du texte affiché à l'écran. Windows a un lecteur intégré, mais
il lit mal la police d'Isaac. **Tesseract** est gratuit, open source, et beaucoup plus
précis.

**Pour l'installer :** clic droit sur l'icône FR → **« Installer Tesseract »**. Une
fenêtre s'ouvre et l'installe toute seule (via `winget`, l'installeur de Windows).
Laisse-la finir, puis c'est bon.

Si tu préfères à la main : installe
[Tesseract OCR](https://github.com/UB-Mannheim/tesseract/wiki). Le logiciel le trouve
tout seul s'il est dans `C:\Program Files\Tesseract-OCR`.

> Sans Tesseract, la version complète marche quand même, mais la lecture de l'écran
> est moins fiable.

---

## Raccourcis clavier

| Touche | Action |
|---|---|
| **F6** | Scanner l'écran et traduire *(VIP)* |
| **F7** | Placer la bulle à la souris |
| **F8** | Réafficher le dernier objet |
| **F9** | Rechercher un objet / astuces du wiki, stats et paramètres *(VIP)* |
| **Maj + F6** | Scan avec image de diagnostic |
| **Ctrl + F8** | Quitter |

Tu peux changer ces touches dans `config.json` (clic droit → Ouvrir le dossier des réglages).

---

## Menu (clic droit sur l'icône FR)

- Scanner l'écran et traduire
- Rechercher un objet / carte / pilule
- Traduire à l'approche des objets *(VIP)*
- Voyant de fonctionnement (petite pastille dans un coin du jeu)
- Durée et taille de la bulle, placement
- Débloquer la version complète
- Vérifier les mises à jour du logiciel
- Installer Tesseract
- Lancer au démarrage de Windows
- Quitter

**Le voyant** (petite pastille dans un coin du jeu) montre que tout marche :
🟢 surveillance active · 🟡 lecture en cours · 🔵 objet reconnu · ⚪ à l'approche
désactivée · 🔴 lecture impossible (installe Tesseract).

---

## Mises à jour automatiques

Le logiciel vérifie tout seul au démarrage s'il existe une version plus récente et
l'installe en quelques secondes. Rien à retélécharger. Tu peux aussi forcer la
vérification : clic droit → **« Vérifier les mises à jour du logiciel »**.

---

## Problèmes courants

**Rien ne se traduit quand je ramasse un objet.**
Vérifie que le jeu est bien **Repentance+** et que le logiciel tourne (icône FR près de
l'horloge). Au premier lancement, laisse-lui quelques secondes avec internet.

**La lecture de l'écran marche mal (version complète).**
Installe **Tesseract** (clic droit → Installer Tesseract).

**Windows / l'antivirus affiche un avertissement.**
L'exe n'est pas signé (petit logiciel perso). Choisis « Exécuter quand même ». Si
l'antivirus le met en quarantaine, autorise-le.

**« Isaac Traducteur FR tourne déjà ».**
Il est déjà lancé : regarde l'icône FR près de l'horloge.

---

## Crédits et licences

- Traductions des objets : **External Item Descriptions (EID)** par *wofsauge* et les
  contributeurs — https://github.com/wofsauge/External-Item-Descriptions (aussi la liste des
  interactions entre objets)
- Qualité des objets : fichiers de données du jeu (*items_metadata.xml*)
- Noms officiels et astuces : **The Binding of Isaac: Rebirth Wiki (FR)**,
  sous licence **CC BY-SA 4.0** — https://bindingofisaacrebirth.wiki.gg/fr
- Traduction du texte libre : **MyMemory**
- Police des bulles (version complète) : **Permanent Marker** par *Font Diner*,
  sous licence **Apache 2.0** (voir `PermanentMarker-LICENSE.txt`)
- Police intégrée : **Cormorant Garamond** par *Christian Thalmann*, sous licence
  **SIL Open Font License 1.1** (voir `CormorantGaramond-OFL.txt`)
- *The Binding of Isaac* est une marque d'Edmund McMillen / Nicalis. Ce logiciel est un
  outil de fan non officiel, sans affiliation.
