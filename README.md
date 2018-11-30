<h1 align="center"> Bookbot</h1> 
<div align="center">
  <strong>A Chatbot helping you to book rooms in your company</strong>
</div>

<div align="center">
  <!-- Subject -->
  <a href="https://nodejs.org/api/documentation.html#documentation_stability_index">
    <img src="https://img.shields.io/badge/subject-awesome-green.svg"
      alt="Subject" />
  </a>
</div>

Le cours/les conseils de la dernière fois ce trouve ici :
On a vu :

 1. Les nouveauté sur Rasa
 2. Le README (installation, TO-DO) : faire un readme pro avec markdown.
 3. Le travail collaboratif sur du code : Git, sa vie, ton oeuvre.

 Les ressources : 
  - [le guide, _migrations_](https://rasa.com/docs/core/migrations/)
  - [Un cours du site du zéro, _gérez votre code avec Git et GitHub_](https://openclassrooms.com/en/courses/2342361-gerez-votre-code-avec-git-et-github)
  - [La beauté sauvera le code, _awesome readme_](https://github.com/matiassingers/awesome-readme)
  
Ici, la correction du chatbot basé sur rasa. Le principal problème que j'ai rencontré était dû à la migration.

Dans le wiki setrouve le cours/les conseils du 29 novembre 2018.

## Installation

 1. Cloner ce dépôt.
 2. Installer les requirements `pip install requirements.txt`
 3. Installer [rasa-nlu-trainer](https://github.com/RasaHQ/rasa-nlu-trainer), un outil pour aller plus vite dans la création d'examples.
 4. Entrainer le modèle avec train_init.py
 5. Entrainer le modèle avec train_online.py s'il y a besoin d'aéliorer la précision.
 6. Tester le chatbot avec dialogue_management_model.py.

En cas de galère [le tutoriel par Justina](https://vimeo.com/254777331) est très bien fait.
 
Bientôt : comment interragir avec Slack.

## Composition

 - data/ :
   - data.json : exemples courants que je voudrais que mon chatbot apprenne
   - stories.md : anciennes conversations avec le chatbot qui aident à rendre le modèle plus précises.
 - config_spacy.json : les paramètres du modèles qui vont être utilisé : pipeline, path, data.
 - nlu.model : script qui crée le modèle d'entrainement
 - domain.yml : les scénarios de réponses, l'univers d'environnement du chatbot
 - actions.py : les opérations concrètes que l'on peut demander de faire et qui sont prévues par domain.py
 - train_init.py : script qui entraine le chatbot pour créer le modèles
 - train_online.py : script qui permet d'entrainer le modèle et mettre à jour stories.md pour améliorer le modèle.
 - models/
   - dialogue/
     Lot of files that make the model, will take the time to explain them later :p 
 - dialogue_management_model.py: script qui permet de tester le chatbot
 - rasa_slack_conector.py : soon ...
 - run_app.py : soon ...

## To-Do

Voir s'il y a des probèmes sur la partie Slack et les corriger.
