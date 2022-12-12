# Basis-Image verwenden
FROM python:3.8

# Arbeitsverzeichnis festlegen
WORKDIR /app

# Alle Dateien aus dem aktuellen Verzeichnis kopieren (ausgeschlossen die im .dockerignore aufgelisteten Files)
COPY . .

# Standardbefehl festlegen, der ausgeführt wird, wenn der Container gestartet wird
CMD ["python", "./app.py"]

# Container wird dem Port zugewiesen, der durch die Umgebungsvariable JOKE_CONSUMER_PYTHON_PORT (im .env file) angegeben wird
EXPOSE ${JOKE_CONSUMER_PYTHON_PORT}
