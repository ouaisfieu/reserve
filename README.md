# Projet SCP 329.02 - Prêt pour Vercel

## Structure des fichiers à créer

```
scp-reserve/
├── index.html
├── package.json
├── vite.config.js
├── tailwind.config.js
├── postcss.config.js
└── src/
    ├── main.jsx
    ├── index.css
    └── App.jsx
```

---

## 📄 package.json

```json
{
  "name": "scp-329-reserve",
  "private": true,
  "version": "1.0.0",
  "type": "module",
  "scripts": {
    "dev": "vite",
    "build": "vite build",
    "preview": "vite preview"
  },
  "dependencies": {
    "react": "^18.2.0",
    "react-dom": "^18.2.0",
    "lucide-react": "^0.263.1"
  },
  "devDependencies": {
    "@vitejs/plugin-react": "^4.2.1",
    "autoprefixer": "^10.4.18",
    "postcss": "^8.4.35",
    "tailwindcss": "^3.4.1",
    "vite": "^5.1.4"
  }
}
```

---

## 📄 index.html

```html
<!DOCTYPE html>
<html lang="fr">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Réserve SCP 329.02</title>
    <link rel="icon" type="image/svg+xml" href="data:image/svg+xml,<svg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 100 100'><text y='.9em' font-size='90'>🌐</text></svg>" />
  </head>
  <body>
    <div id="root"></div>
    <script type="module" src="/src/main.jsx"></script>
  </body>
</html>
```

---

## 📄 vite.config.js

```js
import { defineConfig } from 'vite'
import react from '@vitejs/plugin-react'

export default defineConfig({
  plugins: [react()],
})
```

---

## 📄 tailwind.config.js

```js
export default {
  content: [
    "./index.html",
    "./src/**/*.{js,jsx}",
  ],
  theme: {
    extend: {},
  },
  plugins: [],
}
```

---

## 📄 postcss.config.js

```js
export default {
  plugins: {
    tailwindcss: {},
    autoprefixer: {},
  },
}
```

---

## 📄 src/main.jsx

```jsx
import React from 'react'
import ReactDOM from 'react-dom/client'
import App from './App.jsx'
import './index.css'

ReactDOM.createRoot(document.getElementById('root')).render(
  <React.StrictMode>
    <App />
  </React.StrictMode>,
)
```

---

## 📄 src/index.css

```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

---

## 📄 src/App.jsx

Copiez le contenu de l'artifact "Réserve de Recrutement SCP 329.02" ici.

---

## 🚀 Instructions de déploiement

### En local (test)

```bash
# 1. Créer le dossier et les fichiers
mkdir scp-reserve
cd scp-reserve

# 2. Créer tous les fichiers ci-dessus

# 3. Installer les dépendances
npm install

# 4. Lancer en développement
npm run dev
```

### Sur Vercel

```bash
# 1. Initialiser Git
git init
git add .
git commit -m "Initial commit"

# 2. Créer un repo sur GitHub et pusher
gh repo create scp-reserve --public --push

# 3. Sur vercel.com :
#    - "Add New Project"
#    - Importer depuis GitHub
#    - Cliquer "Deploy"
```

### Alternative : Vercel CLI

```bash
npm install -g vercel
vercel
```

---

## ✅ Checklist avant déploiement

- [ ] Tous les fichiers créés
- [ ] `npm install` exécuté sans erreur
- [ ] `npm run dev` fonctionne localement
- [ ] App.jsx contient le code de l'application
