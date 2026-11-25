# CONCRAST

Website and administration system for a construction and architecture business.

A public website with projects, services and quotation requests, a visual content editor and an administration panel, backed by one API.

> **Structure only.** The source code is private. Source files here are intentionally empty so you can see how the project is organized. Commands describe the private codebase.

![Home](docs/screenshots/home.png)

## Features

- Portfolio and services
- Quotation requests with statuses
- Visual page editor with publication versions
- Real-time updates
- Responsive design

## Applications

| Application | Role |
| --- | --- |
| [API server](server-side/README.md) | Express, Sequelize and PostgreSQL |
| [Public website](client-side/README.md) | React website |
| [Administration](admin-side/README.md) | React administration |
| [Deployment](deployment/README.md) | Server setup scripts |

## Architecture

```mermaid
flowchart LR
  V[Visitors] --> C[Public website] --> API[API server]
  A[Administrators] --> AD[Administration] --> API
  API --> DB[(PostgreSQL)]
```

## Engineering highlights

- Uploads are checked by content, re-encoded and stripped of metadata
- Only published media is reachable publicly
- Database trigger protects the main administrator
- Publication history

## Screenshots

| Home | Services |
| --- | --- |
| ![Home](docs/screenshots/home.png) | ![Services](docs/screenshots/services.png) |
| **Projects** | **Contact** |
| ![Projects](docs/screenshots/projects.png) | ![Contact](docs/screenshots/contact.png) |
| **Dashboard** | **Site editor** |
| ![Dashboard](docs/screenshots/admin-dashboard.png) | ![Site editor](docs/screenshots/admin-site-editor.png) |
| **Projects** | **Services** |
| ![Projects](docs/screenshots/admin-projects.png) | ![Services](docs/screenshots/admin-services.png) |
| **Requests** | **Business information** |
| ![Requests](docs/screenshots/admin-orders.png) | ![Business information](docs/screenshots/admin-settings.png) |
| **Sign in** |
| ![Sign in](docs/screenshots/admin-login.png) |

Captured on a local demo database without the production photos, so image slots show placeholders.

## Repository layout

```text
server-side/                            Express, Sequelize and PostgreSQL
client-side/                            React website
admin-side/                             React administration
deployment/                             Server setup scripts
docs/screenshots/
```

Each application has its own README with responsibilities, dependencies, structure and commands.

## Usage

Published for portfolio and presentation purposes. No license is granted for reuse.
