# Hard Anger — liv og død for brosma

Et journalistisk nettspill om miljøutfordringene i Hardangerfjorden, basert på Havforskningsinstituttets rapport *«Hardangerfjorden under press»* (2025).

## Filer

| Fil | Beskrivelse |
|-----|-------------|
| `index.html` | Forsiden med bakgrunnsstoff om fjorden |
| `spill.html` | Selve spillet (HTML5 Canvas, alle assets embeddet) |
| `vercel.json` | Vercel-konfigurasjon |

## Oppsett: GitHub + Vercel

### 1. Opprett GitHub-repo

```bash
git init
git add .
git commit -m "first commit"
gh repo create hard-anger --public --source=. --push
```

Eller manuelt på [github.com/new](https://github.com/new) — last opp filene.

### 2. Koble til Vercel

1. Gå til [vercel.com](https://vercel.com) og logg inn med GitHub
2. Klikk **Add New → Project**
3. Velg ditt `hard-anger`-repo
4. **Framework Preset**: velg `Other`
5. La alle andre innstillinger stå — klikk **Deploy**

Vercel oppdager at dette er statiske filer og deployer automatisk.

### 3. Automatiske oppdateringer

Etter første deploy: hver gang du pusher til `main`-branchen oppdateres nettsiden automatisk.

```bash
# Oppdater spillet
git add spill.html
git commit -m "oppdater spill"
git push
```

## Lokal testing

Åpne filene direkte i nettleseren, eller kjør en enkel lokal server:

```bash
npx serve .
# Åpnes på http://localhost:3000
```
