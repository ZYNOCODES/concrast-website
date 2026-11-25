# API server

Express, Sequelize and PostgreSQL. Part of [CONCRAST](../README.md).

> **Structure only.** The source code is private. Source files here are intentionally empty so you can see how the project is organized. Commands describe the private codebase.

## Responsibilities

- Public, admin and authentication route groups
- Projects, services, content, orders and settings
- Image validation and WebP conversion
- Rotating refresh tokens stored in the database
- Separate Socket.IO namespaces
- SEO endpoints

## Main dependencies

`bcrypt`, `compression`, `cookie-parser`, `cors`, `dotenv`, `express`, `express-rate-limit`, `helmet`, `hpp`, `joi`, `jsonwebtoken`, `multer`, `pg`, `pg-hstore`, `sequelize`, `sequelize-cli`, `sharp`, `socket.io`, `winston`

## Structure

```text
src/                              3 files
src/config/                       4 files
src/database/                     49 files
src/middlewares/                  9 files
src/modules/                      18 files
src/sockets/                      1 file
src/utils/                        3 files
tests/                            7 files
```

## Commands

```bash
npm install
npm run dev
npm start
npm run db:migrate
npm run db:seed
npm test
npm run lint
```
