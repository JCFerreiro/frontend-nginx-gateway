# Usa una imagen base de Node.js
FROM node:16-alpine

# Establecer directorio de trabajo
WORKDIR /app

# Copiar archivos del proyecto al contenedor
COPY . .

# Instalar dependencias
RUN npm install

# Construir la aplicación Angular para producción
RUN npm run build:ssr

# Instalar el servidor HTTP para servir la aplicación
RUN npm install -g http-server

# Servir la aplicación desde el directorio dist
CMD ["http-server", "dist/"]
