# Atelier Nord, a free Power BI report for an architecture studio

Atelier Nord is a fictional architecture studio in Lyon, running 12 projects across France. This is its full Power BI project: four pages (Overview, Projects, Planning, Finance), a project page you open from any project, a project card on hover, notifications, a New milestone panel, and Light and Dark mode. 136 visuals, 192 DAX measures and not a single custom visual: nothing to install.

Made by Omar Arrim, founder of ChartCraft: https://chartcraft.io

## Open it in 3 steps

You need Power BI Desktop for Windows, a 2026 release.

1. Unzip this folder to `C:\AtelierNord`.
2. Open `AtelierNord.pbip`.
3. Click **Refresh**. The data loads from the `data` folder.

Unzipped somewhere else? In Power BI Desktop, go to **Transform data > Edit parameters** and set `DossierDonnees` to the full path of the `data` folder, ending with a backslash (for example `D:\Projects\AtelierNord\data\`). Then refresh.

In Desktop, hold **Ctrl** to click the report buttons (menu, Open project, Grid and List, the bell, the + of Next milestones). Once published to the Power BI Service, a simple click works.

## What you can do in it

- **Click the project planning.** Each row of the Gantt is a project you can select: the featured project and the studio teams follow it.
- **Hover a project** anywhere (planning, register, profitability, invoices) to see its card: render, phase, budget, hours, next milestone and team.
- **Open a project.** Right-click a row and pick **Drill through > Project**, or use **Open project**. The project page shows the building rising to its progress, hours against plan, its phases, and where it sits on the map of France.
- **Browse the register** in List or Grid, filtered by phase.
- **Plan the weeks ahead.** A weekly timeline with milestones and alerts, a month you can move, a milestone calendar, this week's meetings, and a portfolio pipeline one toggle away.
- **Read the finances** by month, quarter or year against last year: fees and costs, receivables, profitability by project and the invoices to follow.
- **Open the notifications** from the bell, or add a milestone from the + of Next milestones and see where it lands.
- **Switch to Dark mode** from the sidebar: every page follows.

## What's inside

| Path | Content |
|---|---|
| `AtelierNord.pbip` | The file to open |
| `AtelierNord.Report/` | The report, in PBIR format (one JSON file per visual), with its theme and bookmarks |
| `AtelierNord.SemanticModel/` | The model, in TMDL format: 31 tables, 24 relationships, 192 measures |
| `data/` | 17 Parquet files: 19 projects (12 in progress), 24 people, 39,328 timesheet lines, 249 invoices, 74 milestones and the planned hours of every phase |

## Good to know

- The studio, its projects, its clients and every number are fictional. The data was generated, then checked against the design so that the figures add up.
- The report's "now" is fixed at **14 October 2026, 09:42**: "today", "this week" and every "year to date" are computed from that moment.
- The building renders, the portraits and the background drawings were generated with AI. They show no real building or person.
- The New milestone panel shows what a planning form looks like inside Power BI. It writes no data: saving a milestone needs a write-back flow, such as a Fabric translytical task flow.

## Want this on your own data?

ChartCraft Bespoke builds reports like this one on your model, for your team: https://chartcraft.io/bespoke

## License and credits

Atelier Nord is released under the [MIT License](LICENSE): use it, adapt it and share it, including in commercial and client work. Keep the copyright notice.

A few parts come from third parties and keep their own licences, listed in [THIRD-PARTY-NOTICES.md](THIRD-PARTY-NOTICES.md):

- Icons: [Lucide](https://lucide.dev), ISC License (see `LICENSES/lucide.txt`).
- Map of France: regions from [france-geojson](https://github.com/gregoiredavid/france-geojson), Etalab Open Licence 2.0.

---

# Atelier Nord, un rapport Power BI gratuit pour un cabinet d'architecture

Atelier Nord est un cabinet d'architecture fictif installé à Lyon, avec 12 projets en cours partout en France. Voici son projet Power BI complet : quatre pages (Overview, Projects, Planning, Finance), une page projet qui s'ouvre depuis n'importe quel projet, une fiche au survol, des notifications, un panneau New milestone, un mode clair et un mode sombre. 136 visuels, 192 mesures DAX et aucun visuel personnalisé : rien à installer.

## L'ouvrir en 3 étapes

Il faut Power BI Desktop pour Windows, une version de 2026.

1. Décompressez ce dossier dans `C:\AtelierNord`.
2. Ouvrez `AtelierNord.pbip`.
3. Cliquez sur **Actualiser**. Les données se chargent depuis le dossier `data`.

Décompressé ailleurs ? Dans Power BI Desktop, ouvrez **Transformer les données > Modifier les paramètres** et donnez à `DossierDonnees` le chemin complet du dossier `data`, terminé par une barre oblique inverse (par exemple `D:\Projets\AtelierNord\data\`). Puis actualisez.

Dans Desktop, maintenez **Ctrl** pour cliquer sur les boutons du rapport. Une fois publié dans le service Power BI, un simple clic suffit.

## Bon à savoir

- Le cabinet, ses projets, ses clients et tous les chiffres sont fictifs.
- Le « maintenant » du rapport est fixé au **14 octobre 2026, 9 h 42**.
- Les rendus de bâtiments, les portraits et les dessins du fond ont été générés par IA.
- Le panneau New milestone n'écrit aucune donnée : enregistrer un jalon demande un flux d'écriture (par exemple un translytical task flow de Fabric).
- Un rapport comme celui-ci sur vos données : https://chartcraft.io/bespoke
- Licence MIT (fichier `LICENSE`) : libre d'utiliser, d'adapter et de partager, y compris dans un travail commercial ou pour un client, en gardant la mention de copyright. Les icônes et la carte de France gardent leur propre licence (`THIRD-PARTY-NOTICES.md`).
