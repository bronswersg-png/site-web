# Site Portfolio Brutal (HTML/CSS/JS + Node/Express TS)

Petit site brutaliste avec une section **Contact**.
Le formulaire envoie un **POST** vers `POST /api/contact` et les messages sont sauvegardés dans : `data/contacts.json`.

## Prérequis
- Node.js installé (version récente)

## Installer
```bash
npm install
```

## Lancer en dev
```bash
npm run dev
```
Puis ouvre :
- http://localhost:3000

## Build + start (prod)
```bash
npm run build
npm run start
```

## API
- `GET /api/contact` → renvoie `{ ok: true }`
- `POST /api/contact` (JSON):
  - `name` (min 2)
  - `email` (format email)
  - `message` (min 5)

Exemple :
```bash
curl -X POST http://localhost:3000/api/contact ^
  -H "Content-Type: application/json" ^
  -d "{\"name\":\"Alice\",\"email\":\"alice@example.com\",\"message\":\"Bonjour !\"}"
```

## Où sont stockés les messages
- `data/contacts.json` (créé automatiquement)
