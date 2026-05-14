# TailAdmin Hub — Management Dashboard

**A free, open-source admin dashboard template built with React 19, Vite, and Tailwind CSS 4.**

This is the **TailAdmin v2.3.0** free edition. It provides a rich set of UI components, charts, tables, and pages out of the box — used here as the central **"Command Center"** for your MVP suite.

---

## Tech Stack

| Layer | Technology |
|---|---|
| Language | TypeScript 5.7 |
| Framework | React 19 |
| Build Tool | Vite 6 |
| Styling | Tailwind CSS 4 |
| Charts | ApexCharts (via `react-apexcharts`) |
| Calendar | FullCalendar 6 |
| Maps | @react-jvectormap (World map) |
| Routing | React Router 7 |
| Drag & Drop | react-dnd |

---

## Prerequisites

- **Node.js 18+** (Node 20 recommended)
    - Check: `node --version` → must show `18.x` or higher
- **npm 9+**
    - Check: `npm --version`

---

## Clone the Repository

```bash
git clone https://github.com/stephen3123/TailAdmin-Hub.git
cd TailAdmin-Hub
```

---

## Install Dependencies

```bash
npm install
```

This installs all React, Tailwind, ApexCharts, and calendar dependencies. Takes ~30 seconds on first run.

---

## Run in Development Mode

```bash
npm run dev
```

The dashboard will be available at: **`http://localhost:5173`**

You should see the Vite dev server start with output like:
```
  VITE v6.x.x  ready in 300ms
  ➜  Local:   http://localhost:5173/
```

---

## Build for Production

```bash
npm run build
```

This runs TypeScript compilation (`tsc -b`) followed by Vite's production build. Output is placed in the `dist/` folder. You can then deploy it to any static hosting (Vercel, Netlify, S3, etc.)

---

## Preview Production Build

```bash
npm run preview
```

Serves the `dist/` folder locally so you can verify the production build before deploying.

---

## Available Pages

| Page | Route | Description |
|---|---|---|
| **Dashboard (Ecommerce)** | `/` | Main overview with revenue charts, order stats, and map |
| **User Profiles** | `/profile` | Editable user profile page |
| **Calendar** | `/calendar` | FullCalendar with drag-and-drop event scheduling |
| **Forms** | `/forms/form-elements` | All standard form controls (input, select, toggle, etc.) |
| **Tables** | `/tables/basic-tables` | Sortable, paginated data tables |
| **Bar Chart** | `/charts/bar-chart` | ApexCharts bar chart |
| **Line Chart** | `/charts/line-chart` | ApexCharts line chart |
| **Alerts** | `/ui-elements/alerts` | All alert component variants |
| **Badges** | `/ui-elements/badges` | Badge component variants |
| **Buttons** | `/ui-elements/buttons` | Button component variants |
| **Images** | `/ui-elements/images` | Image display components |
| **Videos** | `/ui-elements/videos` | Video player components |
| **Sign In** | `/signin` | Auth — login page |
| **Sign Up** | `/signup` | Auth — registration page |
| **Not Found** | `*` | 404 page |

---

## Project Structure

```
TailAdmin-Hub/
├── index.html              # Vite HTML entry point
├── vite.config.ts          # Vite + React plugin config
├── tailwind.config.ts      # Tailwind CSS 4 config
├── package.json            # Dependencies and scripts
├── tsconfig.json           # TypeScript config
└── src/
    ├── main.tsx            # React entry point (renders App)
    ├── App.tsx             # Root component with routing
    ├── index.css           # Global CSS + Tailwind directives
    ├── layout/             # Sidebar, header, and page shell
    ├── components/         # Reusable UI components
    │   ├── charts/         # ApexCharts wrappers
    │   ├── tables/         # Table components
    │   └── ui/             # Buttons, badges, alerts, etc.
    ├── pages/
    │   ├── Dashboard/      # Main dashboard page (Home.tsx)
    │   ├── Charts/         # BarChart.tsx, LineChart.tsx
    │   ├── Forms/          # FormElements.tsx
    │   ├── Tables/         # BasicTables.tsx
    │   ├── UiElements/     # Alerts, Badges, Buttons, etc.
    │   ├── AuthPages/      # SignIn, SignUp
    │   ├── Calendar.tsx    # FullCalendar integration
    │   └── UserProfiles.tsx
    ├── context/            # React context providers
    ├── hooks/              # Custom React hooks
    └── icons/              # SVG icon components
```

---

## How to Customise for Your Brand

1. **Change the logo**: Replace the logo in `src/layout/` sidebar component.
2. **Change the colours**: Edit the Tailwind theme in `tailwind.config.ts`.
3. **Replace chart data**: Open `src/pages/Dashboard/Home.tsx` and update the static data arrays passed to the `ApexCharts` components.
4. **Add a new page**: Create a new `.tsx` file under `src/pages/`, then add a route in `src/App.tsx`.

---

## License

This template is released under the **MIT License**. The original project is [TailAdmin](https://tailadmin.com/) by TailAdmin Team.
