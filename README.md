# API REST avec Symfony pour Applications Mobiles

## Statut du Projet

🚧 **En cours de développement** 🚧

Ce projet est une API REST développée avec Symfony, destinée à servir de backend pour des applications mobiles. Elle est actuellement en cours de développement et cherche des contributeurs pour aider à ajouter de nouvelles fonctionnalités, améliorer la sécurité et la documentation.

## Fonctionnalités Actuelles

- Authentification JWT
- CRUD de base pour les utilisateurs
- Sécurité des endpoints
- Prise de RDV
- D'autres fonctionnalités seront ajoutées au fil du temps

## Technologies Utilisées

- Symfony 7.x
- Composer pour la gestion des dépendances
- MySQL pour la base de données
- LexikJWTAuthenticationBundle pour l'authentification

## Installation

### Prérequis

- PHP 8+
- Composer
- MySQL

### Étapes

1. **Clonez ce dépôt** :

    ```bash
    git clone git@github.com:tomsdev9/api_mobile.git
    ```

2. **Installez les dépendances avec Composer** :

    Naviguez dans le répertoire du projet cloné, puis exécutez :

    ```bash
    cd api_mobile
    composer install
    ```

3. **Configurez votre base de données** :

    Assurez-vous que le `DATABASE_URL` dans le fichier `.env` ou `.env.local` est configuré pour correspondre à votre environnement de base de données local.

4. **Générez les clés JWT** :

    Générez les clés privée et publique nécessaires pour l'authentification JWT :

    ```bash
    php bin/console lexik:jwt:generate-keypair
    ```

    Cette commande crée les fichiers `private.pem` et `public.pem` dans le dossier `config/jwt/` et configure automatiquement les variables d'environnement nécessaires dans votre fichier `.env`.

5. **Créez la base de données et appliquez les migrations** :

    ```bash
    php bin/console doctrine:database:create
    php bin/console doctrine:migrations:migrate
    ```


