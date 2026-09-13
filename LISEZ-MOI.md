# Atelier BD — obtenir l'APK

L'app est entièrement contenue dans ce projet : une fois installée, elle ne dépend
d'aucun site web. Il reste à la compiler, et GitHub le fait gratuitement pour toi.
Tu n'installes rien sur ton PC, tout se passe dans le navigateur.

---

## 1. Créer le dépôt

Va sur **https://github.com**, crée un compte si besoin, puis clique sur
**New repository**. Donne-lui un nom (`atelier-bd`), coche **Private** si tu veux
le garder pour toi, et valide.

## 2. Envoyer les fichiers

Sur la page du dépôt vide, clique sur **uploading an existing file**.
Dézippe ce projet sur ton ordinateur, puis glisse **tout le contenu** du dossier
dans la zone d'envoi : `www`, `config.xml`, `.github` et ce fichier.

> Si le dossier `.github` n'apparaît pas chez toi, c'est qu'il est masqué.
> Sur Windows : onglet *Affichage* → coche *Éléments masqués*.
> Sur Mac : `Cmd + Maj + .` dans le Finder.

Clique sur **Commit changes** en bas.

## 3. Laisser GitHub compiler

La compilation démarre toute seule. Ouvre l'onglet **Actions** du dépôt : tu vois une
ligne « Construire l'APK » avec un rond orange qui tourne. Compte 5 à 10 minutes la
première fois.

Quand le rond devient vert, clique sur la ligne, descends tout en bas jusqu'à
**Artifacts**, et télécharge **atelier-bd-apk**. Tu obtiens un zip contenant
`atelier-bd.apk`.

> Rond rouge ? Clique dessus, ouvre l'étape en erreur et envoie-moi les dernières
> lignes du journal, je corrige.

## 4. Installer sur le téléphone

Envoie-toi l'APK (mail, câble, Drive), ouvre-le sur Android, accepte
« autoriser l'installation depuis cette source ».

L'app rejoint ta liste d'applications avec son icône. Tu peux supprimer le fichier
APK de tes téléchargements, ça ne change rien.

---

## Premier lancement

L'app demande une **clé API Anthropic**, à créer sur
**https://console.anthropic.com** → *API Keys*, avec quelques euros de crédit.
La facturation est à l'usage : une planche coûte quelques centimes.

La clé est enregistrée dans l'app, sur ton téléphone. Tu ne la ressaisis plus.

## Ce que fait l'app

- **Écrire la suite** — une série, un film, une BD : elle invente l'épisode suivant
- **Histoire perso** — un thème ou ton propre univers : elle crée l'histoire
- Chaque case est dessinée en ligne claire, avec cartouches et bulles
- **Chapitre suivant** enchaîne sur ce qui vient de se passer
- **Garder cette planche** l'enregistre dans le téléphone, relisible sans connexion

## Modifier l'app plus tard

Tout tient dans `www/index.html` : les textes, les couleurs, les consignes données
au modèle. Modifie le fichier sur GitHub, valide, et un nouvel APK se construit
automatiquement.

## Si ça coince

| Problème | Cause |
|---|---|
| « credit balance is too low » | Recharge le compte sur console.anthropic.com |
| « model not found » | Change le nom du modèle dans les réglages de l'app |
| Une case reste vide | Le dessin a échoué, relance la planche |
| L'app ne s'installe pas | Autorise les sources inconnues dans les réglages Android |
