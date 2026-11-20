# Polymath pour Windows

[English](README.en.md) | [Русский](README.ru.md) | [Українська](README.uk.md) | [Deutsch](README.de.md) | [Español](README.es.md) | [Français](README.fr.md) | [Türkçe](README.tr.md) | [中文](README.zh.md)

Une petite barre d'aide pour les conversations et les réunions. Elle écoute votre interlocuteur et traduit ses propos dans votre langue, propose une réponse dans la langue de la conversation, résout une tâche affichée à l'écran et répond à toute question dans le chat.

**Vous seul voyez la barre.** Elle n'apparaît pas lorsque vous partagez l'écran dans Zoom, Teams, Meet, Discord ou OBS, ni sur les captures d'écran et les enregistrements d'écran.

## Fonctionnalités

- **Écouter**. Écoute le son de l'ordinateur (la voix de l'interlocuteur pendant un appel), reconnaît les phrases, affiche une traduction dans votre langue maternelle et, lorsque l'on s'adresse à vous, une réponse prête dans la langue de la conversation, avec sa traduction. Cliquez sur une réponse pour la copier. Le mode « Seulement quand une réponse est nécessaire » n'affiche que les répliques auxquelles il faut répondre.
- **Écran**. Une capture d'écran est envoyée au modèle : résolution d'une tâche, réponse à une question de test, relecture de code.
- **Observer**. Surveille l'écran et répond lorsqu'une nouvelle question ou tâche apparaît. Se désactive automatiquement après 10 minutes.
- **Chat**. Questions ordinaires. Un chiffre au début choisit une commande : `1` Rapide (réponse courte, modèle rapide), `3` Réponse (réponse à la dernière question entendue, en tenant compte de la conversation), `5` Traduction.
- Le modèle voit les dernières phrases de la conversation, vous pouvez donc demander dans le chat : « comment répondre à leur dernière question ? ».
- **Base de connaissances**. Vos propres fichiers `.txt` et `.md` contenant des réponses toutes prêtes aux questions fréquentes. Une réponse correspondante est trouvée sur l'ordinateur, sans Internet, et affichée immédiatement pendant que le modèle répond encore.
- **Commandes personnelles**. Ajoutez vos propres commandes à chiffres, avec vos instructions, votre modèle et vos réglages d'écran ou de son.
- **Historique et export**. Enregistrement facultatif des conversations, chiffré, et export vers un fichier texte.

## Installation

Chaque version publie deux fichiers prêts à l'emploi :

- `Polymath-Setup-<version>.exe` - l'installeur, selon la langue de Windows, avec 22 langues prises en charge. Vous pouvez choisir le dossier, aucun droit d'administrateur n'est nécessaire, les raccourcis sont placés sur le bureau et dans le menu Démarrer, et le programme se lance à la fin de l'installation.

Windows SmartScreen peut signaler un éditeur inconnu, car le fichier n'est pas encore signé. Cliquez sur « Informations complémentaires », puis sur « Exécuter quand même ».

Configuration requise : Windows 10 version 2004 (mai 2020) ou plus récente, ou Windows 11. Sur les systèmes plus anciens, le masquage face au partage d'écran ne fonctionne pas.

Mises à jour : une copie installée vérifie cette page à la recherche de nouvelles versions quelques secondes après son lancement. Lorsqu'une version plus récente apparaît, le programme affiche une carte et ne télécharge la mise à jour qu'avec votre accord. La mise à jour s'installe dans le même dossier, puis le programme redémarre.

## Premier lancement

1. Ouvrez les paramètres (l'icône en forme d'engrenage sur la barre).
2. Choisissez un fournisseur de modèle, collez la clé API et cliquez sur « Enregistrer la clé ». Le lien « Obtenir une clé » ouvre la page du fournisseur.
3. Cliquez sur « Tester la connexion ». La liste des modèles disponibles apparaît, et un clic sur un modèle le place dans le champ.
4. Indiquez votre langue maternelle. Dans la section « Base de connaissances », décrivez-vous brièvement dans le champ « À propos de vous » (poste, expérience). Le modèle s'en sert dans ses réponses.
5. Cliquez sur « Enregistrer » (ou appuyez sur Ctrl+S).

### Fournisseurs

| Fournisseur                          | Modèle par défaut        | Images (Écran/Observer) | Son direct |
| ------------------------------------ | ------------------------ | ----------------------- | ---------- |
| Google Gemini                        | gemini-flash-lite-latest | oui                     | oui        |
| OpenAI                               | gpt-5-mini               | oui                     | non        |
| Anthropic Claude                     | claude-sonnet-5-5        | oui                     | non        |
| OpenRouter                           | openrouter/auto          | oui                     | non        |
| Groq                                 | openai/gpt-oss-120b      | non                     | non        |
| Mistral                              | mistral-medium-latest    | oui                     | non        |
| Ollama (local)                       | llama3.2                 | non                     | non        |
| Personnalisé (compatible OpenAI)     | au choix                 | selon le modèle         | non        |

Les fournisseurs renomment parfois leurs modèles. Si un modèle est introuvable, cliquez sur « Tester la connexion » et choisissez-en un dans la liste.

Le « Modèle rapide » est utilisé par les commandes « Rapide » et « Traduction ». Le champ peut rester vide, dans ce cas c'est le modèle principal qui est utilisé.

Lorsqu'un modèle répond 503 (surchargé) ou 429 (quota épuisé), le programme interroge aussitôt le second modèle de la paire.

### Modèle de secours

La section « Modèle de secours » des paramètres définit un autre fournisseur, interrogé lorsque les deux modèles principaux répondent 503 ou 429. Par exemple, Anthropic Claude (`claude-haiku-5-5` par défaut, un modèle rapide). La clé de secours est enregistrée séparément. Si elle n'est pas renseignée, la clé du même fournisseur de la section « Modèle » est utilisée. Le secours est ignoré lorsqu'il ne peut pas lire ce qui est envoyé, comme une image de l'écran (Écran/Observer) ou le son.

## Reconnaissance vocale (pour « Écouter »)

Les paramètres « Reconnaissance vocale » proposent quatre moteurs :

1. **Via le modèle** (par défaut). La phrase est envoyée directement au modèle de chat. Fonctionne avec Google Gemini, avec la même clé.
2. **API Whisper dans le cloud**. OpenAI (`whisper-1`, `gpt-4o-mini-transcribe`), Groq (`whisper-large-v3-turbo`, rapide et économique) ou votre propre serveur compatible OpenAI. La clé de reconnaissance est enregistrée à part de la clé du modèle.
3. **Local (whisper.cpp)**. Le son ne quitte jamais l'ordinateur. L'installation se fait par une seule commande, les fichiers vont dans `%APPDATA%\Polymath\whisper`. Choisissez ensuite « Local » et cliquez sur « Tester la reconnaissance ». Le petit modèle est utilisé par défaut (466 Mo). D'autres tailles et l'accélération sur les cartes graphiques NVIDIA sont disponibles comme options du script d'installation.
4. **Local (NVIDIA Parakeet)**. Également sur cet ordinateur, plus rapide que whisper.cpp sur le processeur et généralement plus précis. Le modèle connaît 25 langues européennes (anglais, russe, ukrainien, allemand, français, espagnol et d'autres), mais pas le turc ni le chinois. Le bouton « Télécharger Parakeet » des paramètres l'installe. Au total, cela représente environ 520 Mo. Choisissez ensuite « Local (NVIDIA Parakeet) » et cliquez sur « Tester la reconnaissance ». La première phrase après une pause attend 7 à 10 secondes le chargement du modèle, les suivantes prennent moins d'une seconde. Après 10 minutes sans parole, le serveur s'arrête et libère la mémoire.

Au premier lancement sur un nouvel ordinateur, la barre demande une fois comment reconnaître la parole : via Gemini (rien à télécharger) ou avec Parakeet sur cet ordinateur (le programme télécharge environ 520 Mo, avec une progression et un bouton d'annulation). Le choix peut être modifié plus tard dans les paramètres.

Le bouton « Tester la reconnaissance » fonctionne pour les quatre moteurs.

## Utilisation

| Action                              | Raccourci                      |
| ----------------------------------- | ------------------------------ |
| Afficher / masquer la barre         | `Ctrl` + `Alt` + `P`           |
| Résoudre une tâche affichée         | `Ctrl` + `Alt` + `2`           |
| Observer l'écran (activer/désactiver) | `Ctrl` + `Alt` + `4`         |
| Écouter l'appel (activer/désactiver)  | `Ctrl` + `Alt` + `7`         |
| Clic à travers la barre (activer/désactiver) | `Ctrl` + `Alt` + `T` |
| Envoyer                             | `Entrée`                       |
| Nouvelle ligne                      | `Maj` + `Entrée`               |
| Arrêter la réponse                  | `Ctrl` + `.` ou le bouton `■`  |
| Nouvelle conversation               | `Ctrl` + `N` ou le bouton `+`  |
| Requête précédente                  | `↑` / `↓` dans un champ vide   |
| Masquer la barre                    | `Échap`                        |

Les raccourcis se modifient dans les paramètres : cliquez sur le champ et appuyez sur la combinaison voulue. Si un autre programme utilise déjà ce raccourci, la barre le signale.

La barre se déplace en la faisant glisser par son titre, et sa position est mémorisée. La largeur, l'opacité et la taille de police sont réglables.

### Apparence et souris

La section « Interface » des paramètres :

- **Thème** : sombre (graphite, par défaut) ou clair (ivoire).
- **Opacité de la barre** : toute la barre avec son texte (30-100 %).
- **Opacité du fond** : seulement le fond de la barre, le texte reste net (20-100 %).
- **Clic à travers la barre** : les clics traversent la barre d'aide et atteignent la fenêtre située dessous. La barre ne peut alors plus être déplacée ni cliquée à la souris, mais le clavier et les raccourcis fonctionnent. Activez ou désactivez avec `Ctrl` + `Alt` + `T`, et un repère « clic à travers » apparaît alors dans le titre de la barre. La fenêtre des paramètres reste toujours une fenêtre normale.
- **Appuyer sur les boutons au survol** : posez le curseur sur un bouton de la barre (3 secondes par défaut, de 1,5 à 5 possibles) et il s'appuie tout seul. Une bande se remplit sous le bouton. Fonctionne aussi en mode clic à travers.

« Écouter » capte le son de tout le système. Utilisez un casque : seul l'interlocuteur est alors enregistré, et non votre propre voix.

## Commandes personnelles

Les commandes à chiffres se trouvent dans `%APPDATA%\Polymath\commands.json` (bouton « Ouvrir commands.json » des paramètres). Le fichier est relu à chaque appel, aucun redémarrage n'est nécessaire. Exemple :

```json
{
  "1": {
    "name": "Entretien",
    "instructions": "Réponds comme un développeur Java senior lors d'un entretien d'embauche. Réponds en {conversation_language}, puis donne une courte traduction en {native}.",
    "model": "main"
  }
}
```

Champs : `name`, `instructions` (obligatoire), `model` (`main` ou `small`), `screen: true` (joindre une capture d'écran), `watch: true` (observer l'écran), `listen: true` (activer « Écouter »). Variables : `{native}` est votre langue, `{conversation_language}` est la langue de la conversation.

## Masquage face au partage d'écran

Les fenêtres sont créées avec le mécanisme de Windows qui les exclut de la capture (`WDA_EXCLUDEFROMCAPTURE`). Lors d'une capture de l'écran, on voit à la place ce qui se trouve sous la fenêtre. Zoom, Teams, Google Meet dans le navigateur, Discord, OBS, l'Outil Capture, Impr écran et la Xbox Game Bar respectent ce mécanisme.

Également :

- aucun bouton dans la barre des tâches et aucune entrée dans Alt+Tab ;
- l'icône de la zone de notification est désactivée par défaut (la zone de notification est visible quand tout l'écran est partagé) ;
- aucune fenêtre système : les infobulles, listes et menus sont dessinés dans la barre, et le menu contextuel est désactivé.

Limites :

- Le masquage ne protège pas contre une caméra pointée sur l'écran ni contre une capture HDMI matérielle.
- Si vous partagez une **fenêtre** d'un programme (et non l'écran entier) et que la barre se trouve par-dessus, l'autre partie voit ce qui se trouve sous la barre. C'est normal.
- Sur Windows antérieur à la version 2004 de Windows 10, un rectangle noir apparaît dans la capture à la place de la barre.
- Les liens et fichiers ouverts (commands.json, dossier de données) s'ouvrent dans des programmes ordinaires et sont visibles lors du partage d'écran.

## Base de connaissances

La section « Base de connaissances » des paramètres :

- **À propos de vous** : informations générales vous concernant. Le modèle les utilise dans chaque réponse.
- **Fichiers** : le bouton « Ajouter des fichiers », ou le glisser-déposer de fichiers `.txt` et `.md` dans la section. Les fichiers sont copiés dans `%APPDATA%\Polymath\knowledge` (bouton « Ouvrir le dossier »). Vous pouvez les modifier directement là-bas, le programme prend les changements en compte tout seul. Un fichier portant le même nom est remplacé. La limite est de 2 Mo par fichier, en UTF-8, UTF-16 ou Windows-1251.
- **Utiliser la base dans les réponses** : s'active dès que la base contient un fichier.
- **Afficher tout de suite une correspondance de la base, avant la réponse du modèle** : pareil.

Fonctionnement. Pour une question dans le chat et pour chaque phrase de l'interlocuteur dans « Écouter », le programme cherche d'abord une réponse dans vos fichiers, sans Internet et sans modèle. Une correspondance apparaît immédiatement sous forme de bloc bleu « Depuis la base de connaissances » au-dessus de la réponse du modèle, avec un bouton « Copier » à côté. En même temps, le modèle reçoit ces données (toute la base si elle est petite, sinon les passages trouvés) et répond en s'appuyant dessus. La recherche reconnaît les différentes formes des mots. La recherche locale ne trouve pas une question écrite dans une autre langue, mais le modèle répond quand même à partir de la base.

Trois façons d'écrire les fichiers :

```markdown
# Quel salaire attendez-vous ?
À partir de 5 000 USD nets, ouvert à la discussion.

# Pourquoi quittez-vous votre poste actuel ?
Je veux davantage d'architecture.
```

```text
Q: Quel est votre préavis ?
A: Deux semaines.
```

Ou simplement des paragraphes séparés par une ligne vide. La première ligne courte d'un paragraphe en est le sujet.

## Historique et export

La section « Historique » des paramètres :

- **Enregistrer l'historique sur le disque**. Désactivé par défaut : l'historique reste alors en mémoire jusqu'à la fermeture du programme. Activé, chaque question et réponse est ajoutée au fichier du jour dans `%APPDATA%\Polymath\history`, et chaque ligne est chiffrée avec DPAPI de Windows, donc seul votre compte Windows peut la lire.
- **Nom dans l'historique**. Signe vos questions dans les exports. Vide signifie le nom d'utilisateur Windows.
- **Conserver, jours**. Les jours plus anciens sont supprimés au démarrage. 0 signifie tout conserver.
- **Exporter** cette session, aujourd'hui, 7 jours, 30 jours ou tout. « Exporter en .txt » enregistre un fichier dans `Documents\Polymath`, « Copier comme texte » place le même texte dans le presse-papiers.
- **Effacer l'historique** supprime les fichiers d'historique et les entrées de cette session (il faut appuyer deux fois sur le bouton).

Ce qui est enregistré :

- chat : la question (avec la commande et le repère de capture d'écran) et la réponse du modèle ;
- Écouter : la phrase de l'interlocuteur et sa traduction, ainsi que la réponse suggérée et sa traduction lorsqu'une réponse était nécessaire ;
- Observer : les réponses aux tâches affichées à l'écran. Les exécutions vides ne sont pas enregistrées.

Le fichier d'export n'est pas chiffré. L'Explorateur et le Bloc-notes, ouverts avec le bouton « Afficher le fichier », sont visibles lors du partage d'écran.

## Confidentialité

- Les clés API sont stockées chiffrées par Windows (DPAPI) dans `%APPDATA%\Polymath\settings.json`.
- Par défaut, l'historique est seulement en mémoire et disparaît à la fermeture du programme. L'enregistrement sur le disque s'active dans les paramètres, et les fichiers d'historique sont alors chiffrés avec DPAPI.
- Les fichiers de la base de connaissances sont stockés sans chiffrement dans `%APPDATA%\Polymath\knowledge` et sont recherchés sur l'ordinateur. Ils ne partent vers le modèle qu'avec une question : toute la base si elle est petite, sinon les passages correspondants.
- Le son et les captures d'écran ne sont envoyés qu'au fournisseur choisi (ou au fournisseur de secours), et seulement tant que « Écouter », « Écran » ou « Observer » est activé. Avec whisper.cpp ou Parakeet en local, le son ne quitte jamais l'ordinateur.
- Le journal des erreurs se trouve dans `%APPDATA%\Polymath\logs\app.log`. Il ne contient aucun texte de conversation.

## Démarrage en arrière-plan

La case « Démarrer à l'ouverture de session Windows » lance Polymath masqué. Affichez la barre avec `Ctrl` + `Alt` + `P`.

## Configuration requise et limites

- Windows 10 version 2004 ou plus récente, ou Windows 11.
- Une connexion Internet est nécessaire pour les modèles dans le cloud. La reconnaissance vocale locale fonctionne hors ligne après l'installation.
- Une clé d'au moins un fournisseur de modèle. Les clés vous appartiennent, c'est le fournisseur qui les facture.
