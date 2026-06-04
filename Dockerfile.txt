FROM nginx:latest

# Arbeitsverzeichnis
WORKDIR /usr/share/nginx/html

# Kopiere Webseiten Dateien
COPY website/ /usr/share/nginx/html/

# Port freigeben
EXPOSE 80

# Nginx starten
CMD ["nginx", "-g", "daemon off;"]
