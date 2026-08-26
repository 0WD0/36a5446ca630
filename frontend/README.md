# Laboratory Reservation System — Web Frontend

An operator-facing web application for managing laboratories, semesters, schedules, administrators, privileges, login logs, and online users.

Built with React, TypeScript, Ant Design Pro, and Umi Max. This repository is the frontend half of a full-stack course project and connects to the companion [Spring Boot backend](https://github.com/JaspinXu/lab-reservation-system-web-backend).

## Highlights

- Role- and privilege-aware navigation and page access.
- CRUD workflows for laboratories, semesters, and reservation schedules.
- Administrator and permission configuration.
- Login-log and online-user monitoring.
- Reusable chart, table, form, and dialog components.
- Typed API integration with a local development proxy.

## Tech stack

| Area | Technology |
|---|---|
| UI | React 18, Ant Design 5, Ant Design Pro Components |
| Framework | Umi Max 4 |
| Language | TypeScript |
| Charts | ECharts |
| Quality | ESLint, Prettier, Jest, TypeScript |
| Package manager | pnpm |

## Application modules

```text
Login
├── Base data
│   ├── Laboratories
│   ├── Semesters
│   ├── Schedules
│   └── Presets
└── System administration
    ├── Administrators and privileges
    ├── Login logs
    └── Online users
```

## Getting started

### Prerequisites

- Node.js 16 or newer
- pnpm
- The backend running on `http://localhost:9311`

```bash
git clone https://github.com/JaspinXu/lab-reservation-system-web-frontend.git
cd lab-reservation-system-web-frontend
pnpm install
pnpm start
```

Open `http://localhost:8000`. Requests beginning with `/api/` are proxied to the backend configured in [`config/proxy.ts`](config/proxy.ts).

To run without a backend for UI-only development, use the project's mock configuration:

```bash
pnpm dev
```

## Useful commands

```bash
pnpm start          # development server with backend proxy
pnpm build          # production build
pnpm lint           # ESLint, Prettier, and TypeScript checks
pnpm test           # Jest test suite
pnpm test:coverage  # tests with coverage
```

## Project structure

```text
config/
  routes.ts          Route and access-control configuration
  proxy.ts           Local backend proxy
src/
  pages/base/        Laboratory, semester, schedule, and preset modules
  pages/system/      Administrator, login-log, and online-user modules
  pages/User/        Authentication UI
  components/        Shared charts and interface components
  utils/             Requests, files, hooks, and UI helpers
mock/                Local mock endpoints
tests/               Frontend test setup
```

## Backend

The matching API server is maintained separately:

- Repository: [lab-reservation-system-web-backend](https://github.com/JaspinXu/lab-reservation-system-web-backend)
- Default local port: `9311`
- Swagger UI after startup: `http://localhost:9311/swagger-ui/index.html`

## Project context

This system was developed for a software-engineering practicum at Shandong University. The repository keeps the original course-project architecture and is presented as a portfolio artifact rather than a production deployment.

## License

[MIT](LICENSE)

