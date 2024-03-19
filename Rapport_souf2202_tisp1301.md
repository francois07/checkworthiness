---
classoption: 
    - twocolumn
title: IFT714 - Projet
author:
    - François Soulié (souf2202)
    - Paul Tissedre (tisp1301)
numbersections: true
geometry: "top=2cm,left=2cm,right=2cm"
citeproc: true
bibliography: "./projet.bib"
nocite: |
    @*
csl: https://www.zotero.org/styles/association-for-computational-linguistics
---

# Problème

Dans le contexte des discours politiques et des débats, il est crucial de pouvoir identifier les affirmations qui nécessitent une vérification des faits. 

**Exemples**

* "Le taux de chômage a atteint son plus bas niveau historique."
* "Le changement climatique n'est pas une réalité."
* "Notre gouvernement a investi des milliards de dollars dans l'éducation."

**Entrée** 

* **line_number :** L'indice de la phrase dans le transcript du débat
* **speaker :** La personne prononçant la phrase
* **text :** Le contenu de la phrase
* **label :** 1 si la phrase doit être vérifiée, 0 sinon

**Sortie :** Pour chaque phrase, un score indiquant sa priorité pour la vérification des faits entre 0 et 1. On surnommera ce score _check-worthiness_.

# Importance

La vérification des faits est essentielle pour lutter contre la désinformation et garantir un débat public éclairé. 

Un système efficace de vérification des faits permettrait de:

* Améliorer la qualité du débat public.
* Donner aux citoyens les outils nécessaires pour discerner la vérité de la fiction.
* Renforcer la confiance dans les institutions démocratiques.


Notre objectif dans ce projet sera d'établir un modèle capable d'identifier les informations à vérifier.

# Défis

**Facteurs à prendre en compte**

* Le contexte de l'affirmation.
* La présence de mots clés ou d'expressions caractéristiques d’informations à vérifier.

Le défi suivant est le manque de données annotées pour la vérification des faits. La création de telles données est un processus coûteux et chronophage (voir taille du dataset en référence).

# Travaux existants

Pour évaluer la check-worthiness des affirmations en utilisant des techniques de traitement automatique du langage naturel (TALN), les chercheurs se sont concentrés sur plusieurs aspects techniques.

1. Analyse de la structure grammaticale [@zuo_hybrid_2018]
2. Analyse du sentiment [@biyani_using_2014; @gencheva_context-aware_2017]
3. Détection d'entités nommées [@guo_survey_2022; @zuo_hybrid_2018; @gencheva_context-aware_2017]
4. Analyse du contexte [@gencheva_context-aware_2017]

# Proposition de solution

Pour l’instant, le seul modèle que nous avons vu en cours est le N-Gramme. Cependant, d'autres modèles pourraient être pertinents tel que le modèle seq2seq ou encore un réseau de convolution.

\clearpage

# Références
