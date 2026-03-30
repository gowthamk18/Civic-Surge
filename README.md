# Hyper-Local Civic Intelligence Platform
A full-stack web application that detects nearby public infrastructure projects, visualizes them on interactive maps, and explains their real-world impact using geospatial data. Production-oriented civic intelligence stack for verified Indian public-infrastructure projects. The app detects device location, finds nearby projects location , renders them on a multi-mode map, and explains civic impact with source-linked project detail.

Features
📍 Live Location Detection – Finds projects near the user
🗺️ Interactive Maps – Visualize infrastructure with map layers
📊 Impact Insights – Understand real-world effects of projects
🔔 Geo Alerts – Get notified about nearby developments
🧠 Smart Data Processing – Clean and structured project insights

## What Ships

- React/Vite frontend with map modes, nearby alerts, impact panels, reporting, and admin intake
- Express backend with `/api/projects`, `/api/projects/nearby`, `/api/projects/:id`, `/api/report`, and `/api/admin/project`
- Postgres/PostGIS schema in [`server/sql/schema.sql`](/Users/charan/Downloads/indiainno-main/server/sql/schema.sql)
- Verified 31-project source dataset in [`shared/verifiedProjects.js`](/Users/charan/Downloads/indiainno-main/shared/verifiedProjects.js)
- Dataset validation script in [`server/scripts/validate-data.js`](/Users/charan/Downloads/indiainno-main/server/scripts/validate-data.js)

## Stack

- Frontend: React 19, Vite, `react-map-gl`, Tailwind CSS utilities, Lucide icons
- Backend: Node.js, Express 5, Zod validation, Postgres, PostGIS
- Data layer: shared verified project catalogue plus Postgres seed path

## Run Locally

1. Install dependencies:
```bash
npm install
```
2. Copy env files:
```bash
cp .env.example .env
cp server/.env.example server/.env
```
3. Start the frontend:
```bash
npm run dev
```
4. Start the backend in a second terminal:
```bash
npm run server
```
5. Optional PostGIS seed:
```bash
npm run server:seed
```

## Validation

```bash
npm run validate:data
npm run lint
npm run build
```

## Key Files
## 🔑 Key Files

- [App.jsx](src/App.jsx) – Main application workspace  
- [MapCanvas.jsx](src/components/MapCanvas.jsx) – Map rendering  
- [GeoFenceNotification.jsx](src/components/GeoFenceNotification.jsx) – Alerts  
- [projectService.js](server/services/projectService.js) – Backend logic  
- [projects.js](server/routes/projects.js) – API routes  
- [architecture.md](docs/architecture.md) – Architecture  
- [data-sourcing.md](docs/data-sourcing.md) – Data sourcing  

## Notes

- The seed catalogue uses verified project identities only. Missing source fields stay `unknown`.
- Coordinates are representative anchors for named stations, campuses, facilities, or corridor midpoints. They are not survey-grade parcel coordinates.
- The backend runs with an in-memory fallback when `DATABASE_URL` is not configured; production mode should use Postgres/PostGIS.
# astra Bharat
Gowtham
GitHub: https://github.com/gowthamk18
