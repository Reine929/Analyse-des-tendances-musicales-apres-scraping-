# Analyse des tendances musicales : rap ivoirien

Projet réalisé individuellement, pendant un cours de mon Bachelor Business Intelligence & Data à Nexa Digital School.

## Objectif

Récupérer les morceaux d'une playlist Spotify de rap ivoirien, les enrichir avec des caractéristiques audio, puis les analyser pour en tirer des conclusions : quels titres sont les plus populaires, les featurings sont-ils plus populaires que les titres solo, quel est le tempo dominant, quels artistes ont les morceaux les plus dansants ou les plus énergiques.

## Ce que fait le notebook

1. **Collecte via API REST** : authentification auprès de l'API Spotify (flux "client credentials"), puis récupération des 202 morceaux de la playlist avec la pagination.
2. **Enrichissement** : appel de l'API ReccoBeats pour obtenir les caractéristiques audio (énergie, danceability, valence, tempo, etc.).
3. **Préparation des données** avec Pandas : création de deux tableaux de données, jointure sur l'identifiant Spotify, vérification des types, des doublons et des valeurs manquantes. 119 morceaux disposent des deux sources après jointure.
4. **Visualisations** avec Seaborn et Matplotlib : boîtes à moustaches, histogramme du tempo, diagrammes en barres, diagramme circulaire, nuage de points et cartes de corrélation.
5. **Interprétation** : chaque graphique est suivi d'un commentaire écrit.

## Lancer le projet

1. Installer les dépendances : `pip install -r requirements.txt`
2. Créer une application sur le [tableau de bord développeur Spotify](https://developer.spotify.com/dashboard) pour obtenir un identifiant et un secret.
3. Copier `.env.example` en `.env`, ou définir les variables d'environnement `SPOTIFY_CLIENT_ID` et `SPOTIFY_CLIENT_SECRET`.
4. Ouvrir `analyse_tendances_musicales.ipynb` avec Jupyter et exécuter les cellules dans l'ordre. Les fichiers `playlist.json` et `playlist_full.json` sont créés pendant l'exécution.

## Outils

Python, Requests, Pandas, Seaborn, Matplotlib, Jupyter.

## Notes

- Les identifiants Spotify ne sont pas dans le dépôt. Les résultats affichés dans le notebook sont ceux de ma dernière exécution.
- L'échantillon est petit (119 morceaux avec caractéristiques audio) : les conclusions décrivent cette playlist, elles ne valent pas pour tout le rap ivoirien.
