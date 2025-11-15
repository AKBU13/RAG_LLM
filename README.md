# Introduction

## Qu'est-ce que le RAG ?
Le RAG (Retrieval-Augmented Generation) est une méthode qui intègre des systèmes de recherche à l'IA générative, permettant aux chatbots d'accéder à des informations récentes et spécifiques provenant de sources externes.

En utilisant un pipeline de recherche, le chatbot peut récupérer des données pertinentes et à jour, puis les combiner avec les capacités linguistiques du modèle génératif afin de produire des réponses à la fois précises et enrichies par le contexte. Cela rend le RAG particulièrement utile pour les applications nécessitant la fourniture de connaissances factuelles en temps réel.

## Aperçu du projet
![alt text](image.png)

# Configuration du projet

## Prérequis

Avant de commencer, assurez-vous d'avoir installé la dernière version des éléments répertoriés ici :

* RStudio : l'IDE – RStudio est l'espace de travail principal dans lequel vous écrirez et testerez votre code R. Son interface conviviale, ses outils de débogage et son environnement intégré en font l'outil idéal pour l'analyse de données et le développement de chatbots.

* R : le langage de programmation – R est la colonne vertébrale de votre projet. Vous l'utiliserez pour manipuler les données, appliquer des modèles statistiques et intégrer de manière transparente les composants de votre chatbot de recettes.

* Python – Certaines bibliothèques, comme la bibliothèque d'intégration que vous utiliserez pour la vectorisation de texte, sont construites sur Python. Il est essentiel d'avoir installé Python pour activer ces fonctionnalités parallèlement à votre code R.

* Java – Java sert d'élément fondamental pour certaines bibliothèques d'intégration. Il garantit un traitement efficace et la compatibilité des tâches d'intégration de texte nécessaires à l'entraînement de votre chatbot.

* Docker Desktop – Docker Desktop vous permet d'exécuter ChromaDB, la base de données vectorielle, localement sur votre machine. Cela permet un stockage rapide et fiable des intégrations, garantissant que votre chatbot récupère rapidement les informations pertinentes.

* Ollama – Ollama apporte de puissants modèles linguistiques de grande taille (LLM) directement sur votre ordinateur local, éliminant ainsi le besoin de ressources cloud. Il vous permet d'accéder à plusieurs modèles, de personnaliser les résultats et de les intégrer facilement à votre chatbot.

## Installation d'Ollama

Ollama est un outil open source que vous pouvez utiliser pour exécuter et gérer des LLM sur votre ordinateur. Une fois installé, vous pouvez accéder à divers LLM en fonction de vos besoins. Vous utiliserez le modèle llama3.2:3b-instruct-q4_K_M pour créer ce chatbot.

Un modèle quantifié est une version d'un modèle d'apprentissage automatique qui a été optimisée pour utiliser moins de mémoire et de puissance de calcul en réduisant la précision des nombres qu'il utilise. Cela vous permet d'utiliser un LLM localement, en particulier lorsque vous n'avez pas accès à un GPU (unité de traitement graphique - un processeur spécialisé qui effectue des calculs complexes).

Pour commencer, vous pouvez télécharger et installer le logiciel Ollama ici.

Vous pouvez ensuite confirmer l'installation en exécutant cette commande :

![alt text](image-1.png)

Run the following command to start Ollama:

![alt text](image-2.png)

Ensuite, exécutez la commande suivante pour extraire la quantification Q4_K_M de llama3.2:3b-instruct :

![alt text](image-3.png)

Confirmez ensuite que le modèle a bien été extrait à l'aide de cette commande :

![alt text](image-4.png)

Si l'extraction du modèle a réussi, une liste contenant le nom, l'ID et la taille du modèle sera renvoyée, comme suit :

![alt text](image-5.png)

Vous pouvez désormais discuter avec le modèle :

![alt text](image-6.png)

Si l'opération réussit, vous devriez recevoir un message vous invitant à tester le système en posant une question et en obtenant une réponse. Par exemple :

![alt text](image-7.png)

Vous pouvez ensuite quitter la console en tapant /bye ou en appuyant sur Ctrl + D.