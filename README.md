# MealLens web — deploy package

Compiled Expo web export of MealLens (no source, no secrets — the same files any
visitor's browser downloads; bundle passed `check-bundle-secrets`). Served by
nginx with an SPA fallback.

- Rebuild the site from the app repo: `EXPO_PUBLIC_OPENROUTER_API_KEY="" npm run build:web`,
  then replace `dist/` here.
- Deploy: Hostinger Docker Manager → this repo URL, or `docker compose up -d --build`.
- Container listens on host port **8090**.
