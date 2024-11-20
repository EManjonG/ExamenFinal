# Imagen base
FROM node:22

LABEL developer="Estefania"

# Especificar el directorio de trabajo en la imagen docker
WORKDIR /app

# Copiar los fichero del proyecto
# Empezamos por los que cargan las dependencias
# COPY package.json
# COPY package-lock.json
COPY package*.json ./


# ejecutar las sentencias: instalar todo los modulos, eliminar el cache
RUN npm install \
    && npm cache clean --force \
    && rm -rf /tmp/* /root/.npm/_cacache

# copiar el resto del proyecto
COPY . .

#indicar el puerto que usara la maquina virutal
EXPOSE 8000

# Ejecuta la aplicación
# CMD ["node", "src/index.js"]
CMD ["npm","start"]