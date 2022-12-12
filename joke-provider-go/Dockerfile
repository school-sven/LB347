# Basis-Image verwenden
FROM golang:1.19

# Arbeitsverzeichnis festlegen
WORKDIR /app

# Alle Dateien aus dem aktuellen Verzeichnis kopieren (ausgeschlossen die im .dockerignore aufgelisteten Files)
COPY . .

# Erforderliche Abhängigkeiten herunterladen
RUN go mod download

# Go-Code im aktuellen Verzeichnis builden
RUN go build -o /joke-provider-go

# Standardbefehl festlegen, der ausgeführt wird, wenn der Container gestartet wird
CMD ["/joke-provider-go"]

# Container wird dem Port zugewiesen, der durch die Umgebungsvariable JOKE_PROVIDER_GO_PORT (im .env file) angegeben wird
EXPOSE ${JOKE_PROVIDER_GO_PORT}
