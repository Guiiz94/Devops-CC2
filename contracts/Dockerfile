# Utiliser une image de base comme Node.js
FROM node:14

# Définir le répertoire de travail
WORKDIR /usr/src/app

# Copier les fichiers de dépendances
COPY package*.json ./

# Installer les dépendances
RUN npm install

# Copier les fichiers du projet
COPY . .

# Exposer le port utilisé par le service
EXPOSE 8080

# Commande pour démarrer l'application
CMD ["node", "app.js"]