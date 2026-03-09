# gmaps-dossier

Field research dossier on Google Maps scraping: APIs, third-party services, browser automation, anti-detection, and legal landscape (2025–2026).

## Live

https://gmaps-dossier.shellnode.lol

## Stack

- Static HTML/CSS/JS (vanilla, no frameworks)
- nginx:alpine container
- Ghost VPS / Docker
- SSL via SWAG + Cloudflare DNS

## Run Locally

Open `index.html` in a browser, or:

    docker build -t gmaps-dossier .
    docker run -p 8080:8080 gmaps-dossier

## Deploy

    docker context use ghost
    docker build -t gmaps-dossier .
    docker run -d --name gmaps-dossier \
      --network=swag-network \
      -p 8080:8080 \
      --restart unless-stopped \
      gmaps-dossier
