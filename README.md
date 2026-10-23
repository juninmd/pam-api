<div align="center">

# PAM

**PAM, PAM, PAM! Automatize your tasks :)**<br/>
A personal assistant API built with NestJS. Today it exposes a single `GET /` endpoint.

[![Validate](https://img.shields.io/github/actions/workflow/status/juninmd/pam-api/validate.yml?branch=master&style=for-the-badge&label=validate&labelColor=111827)](https://github.com/juninmd/pam-api/actions/workflows/validate.yml)
[![Security Scan](https://img.shields.io/github/actions/workflow/status/juninmd/pam-api/security.yml?branch=master&style=for-the-badge&label=security&labelColor=111827)](https://github.com/juninmd/pam-api/actions/workflows/security.yml)
![NestJS](https://img.shields.io/badge/NestJS-9-E0234E?style=for-the-badge&logo=nestjs&logoColor=white&labelColor=111827)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white&labelColor=111827)
[![License](https://img.shields.io/badge/license-MIT-blue?style=for-the-badge&labelColor=111827)](package.json)

<br/>

<img src=".github/pam_readme.jpg" alt="Woman seated at an office desk with a computer" width="860" />

</div>

## Description

This project is a personal assistant.

## Install

Requires Node.js and npm. The Node.js version is not pinned in the repository.

```bash
npm install   # install dependencies from package-lock.json
```

## Usage

Start the dev server, then call the endpoint:

```bash
npm run start:dev                  # watch mode on port 3000
curl http://localhost:3000/        # GET / returns the greeting
```

```text
Hello World!
```

## How it works

```mermaid
flowchart LR
  Client -->|GET /| Ctrl["app.controller.ts<br/>AppController"]
  Ctrl --> Svc["app.service.ts<br/>AppService.getHello()"]
  Svc -->|"Hello World!"| Client
  Main["main.ts<br/>listen(3000)"] --> Mod["app.module.ts<br/>AppModule"]
  Mod --> Ctrl
```

- `main.ts` bootstraps Nest from `AppModule` and listens on port 3000.
- The controller only routes the request; `AppService` holds the logic, so new behavior lands in the service.

## Develop

```bash
npm run start:dev    # dev server with watch mode
npm run start        # run once through nest start
npm run build        # compile to dist/ (removes dist/ first)
npm run start:prod   # run dist/main.js; run build first
npm run test         # unit tests (src/**/*.spec.ts)
npm run test:e2e     # end-to-end tests (test/**/*.e2e-spec.ts)
npm run test:cov     # unit tests with coverage report in coverage/
npm run lint         # ESLint; applies fixes in place
npm run format       # Prettier; rewrites src and test files
```

## Contributing

Repository guidelines for contributors and AI agents are in [AGENTS.md](AGENTS.md).

## Known limitations

- Only `GET /` exists. It returns the fixed string `Hello World!`.
- The port is hard-coded to `3000` in `src/main.ts`; the project reads no environment variables.
- No authentication or authorization on any endpoint.
- `package.json` has no `engines` field. Both `package-lock.json` and `yarn.lock` are committed; this README uses npm.

## License

MIT, as declared in `package.json`. The repository has no `LICENSE` file yet.
