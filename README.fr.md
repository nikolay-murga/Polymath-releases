# Polymath pour Windows

[English](README.en.md) | [Русский](README.ru.md) | [Українська](README.uk.md) | [Deutsch](README.de.md) | [Español](README.es.md) | [Français](README.fr.md) | [Polski](README.pl.md) | [Türkçe](README.tr.md) | [中文](README.zh.md)

**Your quiet AI partner, in every conversation**
(Votre partenaire IA discret, dans chaque conversation)

Polymath s'assoit à côté de vous et vous aide quand les mots ou les connaissances viennent à manquer. Il entend ce que dit votre interlocuteur, voit ce qui est sur votre écran et vous suggère quoi faire ensuite. Personne d'autre ne le voit, et il ne parle jamais à votre place.

### À quoi il sert

- **Parler avec des gens dont vous ne connaissez pas la langue.** Polymath écoute votre interlocuteur et montre ce qu'il a dit. Puis il vous suggère quoi répondre dans sa langue et dans la vôtre (pour que vous compreniez toujours ce que vous lui dites exactement). Vous restez vous-même dans la conversation, au lieu de vous cacher derrière un traducteur.
- **Rencontres en ligne.** Polymath peut surveiller votre écran et vous suggérer comment répondre dans la langue de votre interlocuteur et dans la vôtre (pour que vous compreniez toujours ce que vous écrivez exactement). Vous écrivez un message qui vous ressemble, en mieux.
- **Séduction.** Recevez une idée de réponse, une blague ou un compliment juste au moment où vous en avez besoin.
- **Tâches du quotidien.** Posez une question, faites une capture d'écran avec l'application et obtenez une réponse adaptée à votre situation.
- **Choses difficiles et incompréhensibles.** Vous ne savez pas où cliquer ou pourquoi quelque chose ne marche pas ? Montrez votre écran à Polymath, il indique l'erreur et explique comment la corriger.

### Ce qui faisait peur est désormais à votre portée avec Polymath

- Passer un entretien d'embauche en ligne et savoir quoi dire.
- Configurer des publicités sur Google ou Meta sans gaspiller votre budget.
- Créer votre premier site web et le mettre en ligne chez n'importe quel hébergeur.
- Comprendre un bail ou un contrat de crédit sans manquer les petites lignes.
- Remplir une déclaration d'impôts ou monter un dossier de visa sans erreur dans les documents.
- Rédiger un CV et une lettre de motivation qui se remarquent, y compris dans une langue étrangère.
- Négocier un prix ou une remise, discuter des conditions avec un propriétaire, un artisan ou un client.
- Comprendre un courrier de la banque, des impôts ou de l'assurance et savoir ce qu'on attend vraiment de vous.
- Configurer une box Wi-Fi, une imprimante ou un téléphone quand rien ne marche et que le technicien est cher ou indisponible.
- Rédiger une réclamation convaincante à un magasin, une compagnie aérienne ou un syndic.
- Préparer une conversation difficile avec un patron, un partenaire ou des parents et trouver les bons mots.

Avant, il fallait un spécialiste à vos côtés ou un coup de fil à un ami. Aujourd'hui, vous avez Polymath, qui s'y connaît dans tous les domaines et reste toujours à portée de main.

---

Une petite barre d’aide pour les conversations et les réunions. Elle écoute votre interlocuteur et traduit ses paroles dans votre langue, suggère une réponse dans la langue de la conversation, résout une tâche depuis l’écran et répond à toutes vos questions dans le chat.

**Vous seul voyez la barre.** Elle n’apparaît pas quand vous partagez l’écran dans Zoom, Teams, Meet, Discord ou OBS, ni dans les captures d’écran et les enregistrements.

## Fonctions

- **Listen** (`7` / `Ctrl` + `Alt` + `7`). Écoute le son de l’ordinateur (la voix de l’interlocuteur pendant un appel), reconnaît les phrases, affiche une traduction dans votre langue maternelle et, quand on s’adresse à vous, une réponse prête dans la langue de la conversation avec sa traduction. Un clic sur une réponse la copie. Le mode « Seulement quand une réponse est nécessaire » n’affiche que les répliques auxquelles vous devez répondre.
- **Screenshot** (`2` / `Ctrl` + `Alt` + `2`). Une capture d’écran part au modèle : résoudre une tâche, répondre à une question de test, relire du code.
- **Watch** (`4` / `Ctrl` + `Alt` + `4`). Surveille l’écran et répond quand une nouvelle question ou tâche y apparaît. S’arrête tout seul après 10 minutes.
- **Chat**. Questions ordinaires. Un chiffre au début choisit une commande : `1` Quick (court, modèle rapide), `3` Answer (une réponse à la dernière question entendue, en tenant compte de la conversation), `5` Translate.
- Le modèle voit les dernières phrases de la conversation, donc dans le chat vous pouvez demander « comment répondre à leur dernière question ? ».
- **Base de connaissances**. Vos propres fichiers `.txt` et `.md` avec des réponses toutes prêtes aux questions fréquentes. Une réponse adaptée est trouvée sur l’ordinateur, sans internet, et affichée tout de suite pendant que le modèle répond encore.

## Installation

Les fichiers prêts sont dans le dossier `dist` :

- `Polymath-Setup-<version>.exe` - le programme d’installation, il suit la langue de Windows et gère 22 langues : vous pouvez choisir le dossier, pas besoin de droits d’administrateur, raccourcis sur le bureau et dans le menu Démarrer, le programme se lance après l’installation ;

Windows SmartScreen peut signaler un éditeur inconnu (le fichier n’est pas signé). Cliquez sur « Informations complémentaires » puis « Exécuter quand même ».

Configuration requise : Windows 10 version 2004 (mai 2020) ou plus récent, Windows 11. Sur les systèmes plus anciens, le masquage de la capture d’écran ne fonctionne pas.

## Premier lancement

1. Ouvrez les paramètres (la roue dentée sur la barre).
2. Choisissez un fournisseur de modèle, collez la clé API et cliquez sur « Enregistrer la clé ». Le lien « Obtenir une clé » ouvre la page du fournisseur.
3. Cliquez sur « Tester la connexion ». Une liste de modèles disponibles apparaît, un clic sur un modèle le met dans le champ.
4. Indiquez votre langue maternelle. Dans la section « Base de connaissances », décrivez-vous brièvement dans « À propos de vous » (métier, expérience). Le modèle l’utilise dans ses réponses.
5. Cliquez sur « Enregistrer » (ou Ctrl+S).

### Fournisseurs

| Fournisseur                  | Modèle par défaut        | Images (Screenshot/Watch)   | Son direct     |
| ---------------------------- | ------------------------ | ----------------------- | -------------- |
| Google Gemini                | gemini-flash-lite-latest | oui                     | oui            |
| OpenAI                       | gpt-5-mini               | oui                     | non            |
| Anthropic Claude             | claude-sonnet-5-5        | oui                     | non            |
| OpenRouter                   | openrouter/auto          | oui                     | non            |
| Groq                         | openai/gpt-oss-120b      | non                     | non            |
| Mistral                      | mistral-medium-latest    | oui                     | non            |
| Ollama (local)               | llama3.2                 | non                     | non            |
| Personnalisé (compatible OpenAI) | au choix             | selon le modèle         | non            |

Les fournisseurs renomment leurs modèles. Si un modèle est introuvable, cliquez sur « Tester la connexion » et choisissez-en un dans la liste.

Le « Modèle rapide » est utilisé par les commandes Quick et Translate. Il peut rester vide, c’est alors le modèle principal qui est utilisé.

Quand un modèle répond 503 (surchargé) ou 429 (quota épuisé), le programme interroge aussitôt l’autre modèle de la paire.

### Modèle de secours

La section « Modèle de secours » des paramètres : un autre fournisseur que le programme interroge quand les deux modèles ci-dessus répondent 503 ou 429. Par exemple, Anthropic Claude (`claude-haiku-5-5` par défaut, un modèle rapide). La clé de secours est stockée séparément. Sans elle, la clé du même fournisseur de la section « Modèle » est utilisée. Le modèle de secours est ignoré quand il ne peut pas lire ce qui est envoyé : une image de l’écran (Screenshot/Watch) ou du son.

## Reconnaissance vocale (pour Listen)

Les paramètres « Reconnaissance vocale » proposent quatre moteurs :

1. **Par le modèle** (par défaut). La phrase va directement au modèle du chat. Fonctionne avec Google Gemini, avec la même clé.
2. **API Whisper dans le cloud**. OpenAI (`whisper-1`, `gpt-4o-mini-transcribe`), Groq (`whisper-large-v3-turbo`, rapide et peu cher) ou votre propre serveur compatible OpenAI. La clé de reconnaissance est stockée à part de la clé du modèle.
3. **Local (whisper.cpp)**. Le son ne quitte jamais l’ordinateur. S’installe avec une commande :

```powershell
powershell -ExecutionPolicy Bypass -File scripts\install-whisper.ps1
```

Dans le programme installé, le script se trouve dans `<dossier du programme>\resources\scripts`. Options : `-Model tiny|base|small|medium|large-v3-turbo` (small par défaut, 466 Mo) et `-Cuda` pour les cartes graphiques NVIDIA. Les fichiers vont dans `%APPDATA%\Polymath\whisper`. Choisissez ensuite « Local » et cliquez sur « Tester la reconnaissance ».

4. **Local (NVIDIA Parakeet)**. Également sur cet ordinateur, plus rapide que whisper.cpp sur un processeur et généralement plus précis. Le modèle `parakeet-tdt-0.6b-v3` connaît 25 langues européennes (anglais, russe, ukrainien, allemand, français, espagnol et d’autres), mais pas le turc ni le chinois. Fonctionne via [sherpa-onnx](https://github.com/k2-fsa/sherpa-onnx). Le bouton « Télécharger Parakeet » des paramètres met tout en place, ou une seule commande :

```powershell
powershell -ExecutionPolicy Bypass -File scripts\install-parakeet.ps1
```

Environ 520 Mo au total. L’option `-Model v2` prend le modèle uniquement anglais, un peu plus précis en anglais. Les fichiers vont dans `%APPDATA%\Polymath\parakeet`. Choisissez ensuite « Local (NVIDIA Parakeet) » et cliquez sur « Tester la reconnaissance ». La première phrase après une pause attend 7 à 10 s pendant le chargement du modèle, les suivantes prennent moins d’une seconde. Après 10 minutes sans parole, le serveur s’arrête et libère la mémoire. Les deux téléchargements (le programme et le modèle) sont vérifiés avec le SHA-256 publié par GitHub. Un fichier qui ne correspond pas est supprimé et rien n’est installé. Sans hachage publié, pas d’installation.

Au premier lancement sur un nouvel ordinateur, la barre demande une fois comment reconnaître la voix : via Gemini (rien à télécharger) ou avec Parakeet sur cet ordinateur (l’application télécharge environ 520 Mo, avec progression et un bouton d’annulation). La réponse peut être changée plus tard dans les paramètres.

Le bouton « Tester la reconnaissance » fonctionne pour les quatre moteurs.

## Utilisation

| Action                             | Raccourci                      |
| ---------------------------------- | ------------------------------ |
| Afficher / masquer la barre        | `Ctrl` + `Alt` + `P`           |
| Réponse rapide (brève, modèle rapide) | `Ctrl` + `Alt` + `1` |
| Résoudre une tâche depuis l’écran  | `Ctrl` + `Alt` + `2`           |
| Réponse à la question qui vient d’être entendue | `Ctrl` + `Alt` + `3` |
| Surveiller l’écran (oui/non)       | `Ctrl` + `Alt` + `4`           |
| Traduire | `Ctrl` + `Alt` + `5` |
| Écouter l’appel (oui/non)          | `Ctrl` + `Alt` + `7`           |
| Cliquer à travers la barre (oui/non) | `Ctrl` + `Alt` + `T`         |
| Envoyer                            | `Entrée`                       |
| Nouvelle ligne                     | `Maj` + `Entrée`               |
| Arrêter la réponse                 | `Ctrl` + `.` ou le bouton `■`  |
| Nouvelle conversation              | `Ctrl` + `N` ou le bouton `+`  |
| Requête précédente                 | `↑` / `↓` dans un champ vide   |
| Masquer la barre                   | `Échap`                        |

### Commandes courtes et longues

Les commandes courtes fonctionnent dans la barre, les longues (avec `Ctrl` + `Alt`) depuis n’importe quelle fenêtre. Un chiffre dans un champ vide choisit une commande, `1 votre texte` fonctionne aussi.

| Action | Courte (dans la barre) | Longue (depuis n’importe quelle fenêtre) |
| --- | --- | --- |
| Réponse rapide (brève, modèle rapide) | `1` | `Ctrl` + `Alt` + `1` |
| Résoudre une tâche depuis l’écran | `2` | `Ctrl` + `Alt` + `2` |
| Réponse à la question qui vient d’être entendue | `3` | `Ctrl` + `Alt` + `3` |
| Surveiller l’écran (oui/non) | `4` | `Ctrl` + `Alt` + `4` |
| Traduire | `5` | `Ctrl` + `Alt` + `5` |
| Écouter l’appel (oui/non) | `7` | `Ctrl` + `Alt` + `7` |
| Afficher / masquer la barre | `Esc` | `Ctrl` + `Alt` + `P` |
| Cliquer à travers la barre (oui/non) | - | `Ctrl` + `Alt` + `T` |
| Paramètres | `Ctrl` + `,` | `Ctrl` + `,` |
| Nouvelle conversation | `Ctrl` + `N` | - |
| Arrêter la réponse | `Ctrl` + `.` | - |
| Afficher tous les raccourcis | `F1` | - |

**Barre masquée ?** Appuyez sur `Ctrl` + `Alt` + `P` (ou sur le raccourci défini dans les paramètres) ou relancez Polymath (raccourci du menu Démarrer), et la barre revient. L’icône de la zone de notification est désactivée par défaut. Le bouton `?` de la barre (à côté des paramètres, ou `F1`) affiche toutes les commandes et tous les raccourcis.

**Important :** les commandes courtes ne fonctionnent que lorsque le champ de saisie est actif, et pas en mode clic à travers. Les commandes longues (avec `Ctrl` + `Alt`) fonctionnent toujours.

Les raccourcis se changent dans les paramètres : cliquez sur le champ et appuyez sur la combinaison. Si un autre programme l’utilise déjà, la barre le signale.

Faites glisser la barre par son titre, sa position est mémorisée. La largeur, l’opacité et la taille de la police sont réglables.

### Apparence et souris

La section « Interface » des paramètres :

- **Thème** - sombre (graphite, par défaut) ou clair (ivoire) ;
- **Opacité de la barre** - toute la barre avec son texte (30-100 %) ;
- **Opacité du fond** - seulement le fond de la barre, le texte reste net (20-100 %) ;
- **Cliquer à travers la barre** - les clics traversent la barre d’aide jusqu’à la fenêtre en dessous. La barre ne peut être ni déplacée ni cliquée à la souris, le clavier et les raccourcis fonctionnent toujours. Se bascule avec `Ctrl` + `Alt` + `T`, le titre de la barre affiche alors une marque « clic traversant ». La fenêtre des paramètres est toujours une fenêtre normale ;
- **Appuyer sur les boutons par survol** - laissez le curseur sur un bouton de la barre (3 secondes par défaut, de 1,5 à 5 possible) et il s’enfonce tout seul. Une bande se remplit sous le bouton. Fonctionne aussi en mode clic traversant.

Listen capte le son de tout le système. Utilisez un casque : ainsi seul l’interlocuteur est enregistré, pas votre propre voix.

## Vos propres commandes

Les commandes numériques se trouvent dans `%APPDATA%\Polymath\commands.json` (le bouton « Ouvrir commands.json » des paramètres). Le fichier est relu à chaque appel, pas besoin de redémarrer. Exemple :

```json
{
  "1": {
    "name": "Interview",
    "instructions": "Answer as a senior Java developer at a job interview. Answer in {conversation_language}, then give a short translation into {native}.",
    "model": "main"
  }
}
```

Champs : `name`, `instructions` (obligatoires), `model` (`main` ou `small`), `screen: true` (joindre une capture d’écran), `watch: true` (surveiller l’écran), `listen: true` (activer Listen). Marqueurs : `{native}` - votre langue, `{conversation_language}` - la langue de la conversation.

## Fiabilité du masquage

Les fenêtres sont créées avec `SetWindowDisplayAffinity(WDA_EXCLUDEFROMCAPTURE)`. C’est un mécanisme de Windows : une capture d’écran montre à la place ce qui se trouve sous la fenêtre. Zoom, Teams, Google Meet dans un navigateur, Discord, OBS, l’Outil Capture, PrintScreen et la Xbox Game Bar le respectent.

Également :

- pas de bouton dans la barre des tâches ni d’entrée dans Alt+Tab ;
- l’icône de la zone de notification est désactivée par défaut (la zone est visible quand tout l’écran est partagé) ;
- pas de fenêtres contextuelles du système : les infobulles, listes et menus sont dessinés à l’intérieur de la barre, le menu contextuel est désactivé.

Limites :

- Le masquage ne protège pas d’une caméra pointée vers l’écran ni d’une capture HDMI matérielle.
- Si vous partagez une **fenêtre** d’un programme (pas tout l’écran) et que la barre est posée dessus, l’autre côté voit ce qui est sous la barre. C’est normal.
- Windows antérieur à 10 version 2004 affiche un rectangle noir dans la capture à la place de la barre.
- Les liens et fichiers ouverts (commands.json, le dossier de données) s’ouvrent dans des programmes ordinaires et sont visibles quand l’écran est partagé.

Vérifiez le masquage sur votre ordinateur :

```powershell
powershell -ExecutionPolicy Bypass -File scripts\verify-capture.ps1
```

Le script affiche deux fenêtres de test protégées et une normale, capture l’écran de deux façons et affiche le résultat. La ligne `RESULT: Polymath windows are hidden from screen capture` signifie que tout fonctionne.

## Base de connaissances

La section « Base de connaissances » des paramètres :

- **À propos de vous** - informations générales sur vous. Le modèle les utilise dans chaque réponse.
- **Fichiers** - le bouton « Ajouter des fichiers », ou déposez des fichiers `.txt` et `.md` sur la section. Les fichiers sont copiés dans `%APPDATA%\Polymath\knowledge` (le bouton « Ouvrir le dossier »). Vous pouvez les modifier là, le programme prend les changements en compte tout seul. Un fichier du même nom est remplacé, jusqu’à 2 Mo, en UTF-8, UTF-16 ou Windows-1251.
- **Utiliser la base de connaissances dans les réponses** - s’active dès que la base contient un fichier.
- **Afficher tout de suite une correspondance de la base, avant la réponse du modèle** - idem.

Fonctionnement. Pour une question du chat et pour chaque phrase de l’interlocuteur dans Listen, le programme cherche d’abord une réponse dans vos fichiers, sans internet et sans le modèle. Une correspondance apparaît aussitôt sous la forme d’un bloc bleu « De la base de connaissances » au-dessus de la réponse du modèle, avec un bouton « Copier » à côté. En même temps, le modèle reçoit ces données (toute la base quand elle est petite, sinon les parties correspondantes) et répond en s’appuyant dessus. La recherche comprend les différentes formes des mots. La recherche locale ne trouvera pas une question dans une autre langue, mais le modèle répond quand même à partir de la base.

L’une des trois façons d’écrire les fichiers :

```markdown
# What salary do you expect?
From 5,000 USD net, open to discussion.

# Why are you leaving your current job?
I want more architecture work.
```

```text
Q: What is your notice period?
A: Two weeks.
```

Ou simplement des paragraphes séparés par une ligne vide : la courte première ligne d’un paragraphe en est le sujet.

## Historique et export

La section « Historique » des paramètres :

- **Enregistrer l’historique sur le disque**. Désactivé par défaut : l’historique ne vit alors qu’en mémoire jusqu’à la fermeture du programme. Activé : chaque question et réponse est ajoutée à `%APPDATA%\Polymath\history\YYYY-MM-DD.jsonl`, chaque ligne chiffrée avec Windows DPAPI (seul votre compte Windows peut la lire).
- **Nom dans l’historique**. Signe vos questions dans les exports. Vide signifie le nom d’utilisateur Windows.
- **Conserver, jours**. Les jours plus anciens sont supprimés au démarrage. 0 conserve tout.
- **Exporter** cette session, aujourd’hui, 7 jours, 30 jours ou toute la période. « Exporter en .txt » enregistre un fichier dans `Documents\Polymath`, « Copier en texte » place le même texte dans le presse-papiers.
- **Effacer l’historique** supprime les fichiers d’historique et les entrées de cette session (appuyez deux fois sur le bouton).

Ce qui est enregistré :

- chat : Q - votre question (avec la commande et une marque de capture d’écran), A - la réponse du modèle ;
- Listen : Q - la phrase de l’interlocuteur et sa traduction, A - la réponse qui vous a été suggérée et sa traduction (quand une réponse était nécessaire) ;
- Watch : réponses aux tâches de l’écran, les exécutions vides ne sont pas enregistrées.

Le fichier d’export n’est pas chiffré. L’Explorateur et le Bloc-notes, ouverts avec le bouton « Afficher le fichier », sont visibles quand l’écran est partagé.

## Confidentialité

- Les clés API sont stockées chiffrées par Windows (DPAPI via Electron safeStorage) dans `%APPDATA%\Polymath\settings.json`.
- Par défaut, l’historique n’est qu’en mémoire et disparaît à la fermeture du programme. L’enregistrement sur le disque s’active dans les paramètres, les fichiers d’historique sont chiffrés avec DPAPI.
- Les fichiers de la base de connaissances sont stockés dans `%APPDATA%\Polymath\knowledge` sans chiffrement, la recherche s’y fait sur l’ordinateur. Ils ne vont au modèle qu’avec une question : toute la base quand elle est petite, sinon les parties correspondantes.
- Le son et les captures d’écran vont uniquement au fournisseur choisi (ou à celui de secours) et seulement tant que Listen, Screenshot ou Watch est activé. Avec whisper.cpp ou Parakeet en local, le son ne quitte jamais l’ordinateur.
- Journal des erreurs : `%APPDATA%\Polymath\logs\app.log` (sans texte des conversations).

## Fonctionnement en arrière-plan

La case « Démarrer à l’ouverture de session Windows » lance Polymath masqué. Appelez la barre avec Ctrl+Alt+P. À la main : `Polymath.exe --background`.

## Mises à jour

Polymath installé (depuis `Polymath-Setup`) cherche une nouvelle version quelques secondes après le démarrage. Rien n’est téléchargé sans votre accord : la barre affiche « Polymath X est disponible » avec les boutons « Mettre à jour » et « Plus tard », puis « Redémarrer et mettre à jour » une fois le téléchargement terminé. Polymath se ferme, s’installe par-dessus l’ancienne version et redémarre, les réglages, les clés et l’historique sont conservés. Si l’icône de la zone de notification est activée, son menu contient « Check for updates ». Une copie lancée depuis le dossier des sources et une copie portable ne se mettent pas à jour toutes seules.

Le téléchargement est vérifié avec le SHA-512 du `latest.yml` de la version. Une version sans ce hachage est refusée et un fichier qui ne correspond pas n’est pas installé. Chaque build vérifie que `latest.yml` contient le bon hachage. L’installateur n’est pas encore signé, Windows SmartScreen peut donc encore avertir.

## Pour les développeurs

Node.js 20 ou plus récent est nécessaire.

```powershell
npm install
```

```powershell
npm start
```

```powershell
npm test
```

```powershell
npm run dist
```

- `npm test` - tests unitaires (détecteur de phrases, WAV, analyse des réponses, SSE, commandes, paramètres, client du modèle, historique).
- `npm run dist` - l’installateur dans `dist`, puis une vérification que `latest.yml` contient le bon SHA-512.
- `python scripts/make-installer-art.py` - redessine les visuels du programme d’installation (`build/` : image latérale, en-tête, icône) à partir de `assets/icon.png`. Nécessite Python avec Pillow.
- `npm run capture-test` - la vérification de masquage intégrée (résultat en JSON).
- La variable `POLYMATH_VISIBLE=1` désactive le masquage en mode développement, pour faire des captures de l’interface. Elle n’a aucun effet dans le programme compilé.

Organisation :

- `src/main` - le processus principal : fenêtres, raccourcis, modèle, reconnaissance vocale, Listen, Watch ;
- `src/renderer` - la barre et la fenêtre des paramètres, capture du son système ;
- `src/shared` - code partagé : détecteur de phrases, WAV, analyse de texte, SSE, traductions de l’interface ;
- `scripts` - installation de whisper.cpp et Parakeet et vérification du masquage ;
- `tests` - tests.
