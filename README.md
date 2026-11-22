# Site vitrine OpenSphere

Site statique : tout est dans `index.html` (CSS, JavaScript et logo inclus). Le dossier `assets/` garde les fichiers du logo d'origine.

## Voir le site en local
Double-cliquer sur `index.html`, il s'ouvre dans le navigateur.

## Mettre en ligne sur Cloudflare Pages (gratuit)

### Méthode 1 — Glisser-déposer (la plus simple)
1. Créer un compte sur dash.cloudflare.com.
2. Menu **Workers & Pages** → **Créer** → onglet **Pages** → **Importer des ressources** (upload).
3. Nom du projet : `opensphere`.
4. Glisser le dossier `site-vitrine` → **Déployer**.
5. Le site est en ligne sur `https://opensphere.pages.dev`.

### Méthode 2 — Avec Claude Code (recommandé ensuite)
Dans le terminal, depuis ce dossier :
```powershell
npx wrangler login
npx wrangler pages deploy . --project-name=opensphere
```

### Méthode 3 — Depuis GitHub (mise à jour automatique)
1. Pousser ce dossier dans un dépôt GitHub `opensphere-site`.
2. Cloudflare → Pages → **Connecter à Git** → choisir le dépôt.
3. Paramètres de build : aucun framework, commande de build vide, dossier de sortie `/`.
4. Chaque `git push` remet le site à jour automatiquement.

## Passer plus tard sur Vercel
Importer le même dépôt GitHub sur vercel.com (aucun réglage nécessaire pour un site statique), puis faire pointer le nom de domaine vers Vercel.
