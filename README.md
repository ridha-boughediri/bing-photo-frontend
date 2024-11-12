
# Bing Photo Frontend

## Description

Ce projet est une application frontend utilisant Next.js pour afficher des photos de Bing. L'application est dockerisée pour simplifier le déploiement et l'exécution dans n'importe quel environnement.

## Prérequis

- **Docker** : Assurez-vous que Docker est installé sur votre machine.
- **Node.js** (optionnel) : Si vous souhaitez exécuter ou tester l'application en dehors de Docker.

## Structure du projet

```
bing-photo-frontend/
├── .eslintrc.json
├── .gitignore
├── Dockerfile
├── jsconfig.json
├── next.config.mjs
├── node_modules/
├── package.json
├── package-lock.json
├── postcss.config.mjs
├── public/
├── README.md
├── src/
└── tailwind.config.js
```

## Utilisation avec Docker

### Étape 1 : Construire l'image Docker

Depuis le répertoire racine de l'application, exécutez la commande suivante pour construire l'image Docker :

```bash
docker build -t bing-photo-frontend .
```

Cette commande crée une image Docker nommée `bing-photo-frontend` basée sur la configuration spécifiée dans le `Dockerfile`.

### Étape 2 : Exécuter le conteneur Docker

Une fois l'image construite, lancez le conteneur en utilisant la commande suivante :

```bash
docker run -p 3000:3000 bing-photo-frontend
```

Cela démarre l'application et la rend accessible à l'adresse [http://localhost:3000](http://localhost:3000).

### Commandes Docker utiles

- **Arrêter le conteneur** : Identifiez l'ID du conteneur avec `docker ps`, puis utilisez :
  ```bash
  docker stop <container_id>
  ```

- **Supprimer l'image Docker** :
  ```bash
  docker rmi bing-photo-frontend
  ```

## Développement Local (hors Docker)

Pour exécuter l'application en local sans Docker, suivez ces étapes :

1. **Installer les dépendances** :
   ```bash
   npm install
   ```

2. **Lancer le serveur de développement** :
   ```bash
   npm run dev
   ```

3. **Accéder à l'application** :
   L'application sera disponible à l'adresse [http://localhost:3000](http://localhost:3000).

## Informations supplémentaires

### Variables d'environnement

Si votre application nécessite des variables d'environnement, créez un fichier `.env.local` à la racine du projet et y spécifiez vos clés de configuration. Assurez-vous que le fichier `.env.local` est listé dans le fichier `.gitignore` pour éviter de commiter des informations sensibles.

### Remarques

- **Modifications** : Si vous apportez des modifications au code, vous devrez reconstruire l'image Docker en exécutant à nouveau `docker build -t bing-photo-frontend .`.
- **Problèmes** : En cas de problème avec Docker, assurez-vous que les ports sont disponibles et que l'application fonctionne en local avant de la dockeriser.

## Contributeurs
@ridha-boughediri
@AlizeaMasse
@MathieuPlateforme
@tchessiDev
@yonathan-darmon


---

Merci d'utiliser l'application Bing Photo Frontend !
