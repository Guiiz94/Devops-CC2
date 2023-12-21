# Utiliser une image de base Node.js
FROM node:14

# Définir le répertoire de travail
WORKDIR /usr/src/app

# Copier les fichiers package.json et package-lock.json
COPY package*.json ./

# Installer les dépendances
RUN npm install

# Copier les fichiers et dossiers du projet dans le conteneur
COPY . .

# Construire l'application pour la production
RUN npm run build

# Utiliser une image Nginx pour servir le contenu statique
FROM nginx:alpine

# Copier le contenu statique construit
COPY --from=0 /usr/src/app/build /usr/share/nginx/html

# Exposer le port 80
EXPOSE 80

# Démarrer Nginx
CMD ["nginx", "-g", "daemon off;"]