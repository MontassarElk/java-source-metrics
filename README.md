# Java Source Metrics

Un petit outil en ligne de commande pour explorer des métriques de code Java. Il parcourt un fichier ou un répertoire de sources et produit deux exports CSV : un pour les classes et un pour les méthodes.

## Utilisation

Depuis `tp/src`, avec un JDK installé :

```bash
javac *.java
java Main /chemin/vers/sources java
```

Les fichiers `class.csv` et `method.csv` sont créés dans le répertoire depuis lequel la commande est lancée. L'argument d'extension attendu est `java`.

## Métriques exportées

- **Classes** : chemin, nom, lignes de code et de commentaires, densité de commentaires, WMC et BC.
- **Méthodes** : chemin, classe et méthode, lignes de code et de commentaires, densité de commentaires, complexité cyclomatique et BC.

L'analyse repose sur des expressions régulières et des heuristiques ligne par ligne. Elle donne des estimations pratiques, mais ne remplace pas un parseur Java pour les constructions syntaxiques complexes. Les fichiers CSV sont écrasés à chaque exécution.

## Structure

Le code se trouve dans [`tp/src`](tp/src). Le rapport et l'énoncé d'origine restent dans [`tp`](tp) pour conserver le contexte du développement et l'historique du dépôt.

Projet initialement réalisé dans le cadre d'un cours par Ho jun Hwang et Montassar Elkolli, puis présenté ici comme démonstration de l'analyse de code et de l'export de métriques.
