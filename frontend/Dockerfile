# Imagen base Nodejs
FROM node:16-alpine

# directorio de trabajo
WORKDIR /app

# Copiar archivos del proyecto al contenedor
COPY . .

# Instalar dependencias
RUN npm install

# Construir la aplicación Angular para producción
RUN npm run build:ssr

# Instalar servidor HTTP para la aplicación
RUN npm install -g http-server

# Servir aplicación directorio dist
CMD ["http-server", "dist/"]
