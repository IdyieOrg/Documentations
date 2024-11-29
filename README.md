# Idyie

### Développeurs
- Levet Corentin - (corentin.levet@epitech.eu)
- Vanelle Gwendoline - (gwendoline.vanelle@epitech.eu)
- Grisel Hugo - (hugo.grisel@epitech.eu)

## **Description**
Ce projet a été initié pour permettre aux personnes non techniques en entreprise, telles que les directeurs, commerciaux ou RH, de visualiser et analyser les données clients de leur base de données sans solliciter de spécialistes techniques. Idyie utilise l'intelligence artificielle pour produire automatiquement ces visualisations et analyses en réponse aux requêtes API effectuées via  prompt dans l’interface graphique.

## **Architecture du projet**
Ce projet est organisé en quatre repositories distincs :
- [IdyieAPI](https://github.com/IdyieOrg/IdyieAPI)
- [IdyieFormater](https://github.com/IdyieOrg/IdyieFormatter)
- [IdyieLLM](https://github.com/IdyieOrg/IdyieLLM)
- [IdyieWeb](https://github.com/IdyieOrg/IdyieWeb)

### IdyieAPI
API en RubyOnRails pour faire le lien entre le front et les différents services backend.

### IdyieFormater
IA en Python chargée de formater les données récupérées par l'API conformément à la requête de l'utilisateur.

### IdyieLLM
IA de type Large Language Model en Python chargée de transformer la requête de l'utilisateur en requêtes utilisables par l'API pour récupérer les données souhaitées.

### IdyieWeb
Page web en RubyOnRails avec une interface de type chat pour permettre aux utilisateurs de saisir des requêtes de manière intuitive.

### ***Docker***
Tous ces repositories sont contenerisés dans des services Docker.

## **Organisation du projet**
### Méthodologie SCRUM
Sprint de trois semaines, les tâches sont choisies en fonction de celle dans le backlog.


### Méthodologie Github
[Lien de la méthodologie Github](MethodologyGithub.md#test)

## **Installation**
Pour installer ce projet, vous aurez besoin de :
- [Docker](https://docs.docker.com/engine/install/)
- [Docker compose](https://docs.docker.com/compose/install/)

Une fois ces deux outils installés, vous pourrez construire le docker en utilisant la commande :
```bash
docker compose build
```

Une fois le conteneur construit, vous pouvez exécuter le projet en utilisant:

```bash
docker compose up -d
```