# TP AnCoGen — Modèles Génératifs et Contrôle par Bruit (SNR)

## Objectif du TP

Ce TP a pour objectif de **comprendre concrètement le fonctionnement d’un modèle génératif AnCoGen**, en étudiant comment :
- un signal est analysé et transformé en représentation latente,
- un processus génératif reconstruit ou génère un signal,
- le **bruit** et le **rapport signal/bruit (SNR)** influencent la qualité des générations.

Le TP est centré sur la **manipulation effective du pipeline generative model**, et non sur une simple utilisation boîte noire.

---

## Ce qui est fait concrètement dans le TP

### 1. Initialisation de l’environnement

Le TP commence par :
- l’import des librairies nécessaires (PyTorch, NumPy, outils AnCoGen),
- la détection automatique du matériel (CPU / GPU),
- le chargement des paramètres globaux du modèle.

Cette étape permet de garantir que les expériences sont **reproductibles** et exécutables sur différentes machines.

---

### 2. Chargement et préparation du modèle AnCoGen

Le modèle AnCoGen est :
- instancié avec ses hyperparamètres (dimensions latentes, nombre d’itérations, etc.),
- chargé sur le bon device (CPU ou GPU),
- préparé pour fonctionner en mode **analyse** ou **génération**.

À ce stade, le modèle est prêt à traiter un signal d’entrée.

---

### 3. Phase d’analysis (encodage du signal)

Dans cette étape :
- un signal d’entrée (exemple fourni dans le TP) est passé dans le modèle,
- le modèle **analyse le signal** et le projette dans un **espace latent**,
- cette représentation latente capture les caractéristiques essentielles du signal.

👉 Concrètement, on observe comment l’information du signal est compressée et structurée avant toute génération.

---

### 4. Phase de synthesis (génération / reconstruction)

À partir de la représentation latente :
- le modèle génère un signal de sortie,
- ce signal peut être une **reconstruction** du signal original ou une **nouvelle génération**,
- les sorties sont visualisées et comparées au signal d’entrée.

👉 Cette étape permet de comprendre comment le modèle transforme une information latente en un signal exploitable.

---

### 5. Ajout et contrôle du bruit

Le TP introduit explicitement :
- l’ajout de bruit contrôlé dans le pipeline,
- différentes valeurs de **SNR (Signal-to-Noise Ratio)**,
- l’observation de l’impact du bruit sur la qualité des résultats.

On compare :
- une génération avec faible bruit,
- une génération avec bruit modéré,
- une génération avec bruit élevé.

👉 Cela met en évidence le compromis entre **diversité** et **fidélité** des générations.

---

### 6. Expérimentations guidées

Plusieurs expériences sont menées :
- variation du SNR,
- comparaison analysis → synthesis directe vs génération bruitée,
- observation qualitative des sorties générées.

---

### 7. Interprétation des résultats

Le TP se termine par :
- l’analyse des différences entre les signaux générés,
- l’identification des effets du bruit,
- la compréhension du rôle du SNR dans les modèles génératifs.

Cette étape est essentielle pour relier la **théorie** (modèles génératifs, bruit, espace latent) à la **pratique**.

---

## Résultats attendus

- décrire le pipeline analysis → synthesis d’un modèle AnCoGen,
- expliquer le rôle du bruit dans un modèle génératif,
- comprendre l’impact du SNR sur la qualité des générations,
- manipuler un modèle génératif de manière contrôlée.

---

## Contenu du dépôt

