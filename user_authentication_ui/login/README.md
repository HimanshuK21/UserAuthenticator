Basic Login / Sign-up UI for the authentication service that receives a JWT from the backend.

**Overview**
- **Project**: Login UI for the User Authentication service.
- **Purpose**: Provide a simple frontend for user registration, login, and token-based session handling.

**Tech Stack**
- **Framework**: Vite + React + TypeScript
- **Bundler**: Vite

**Prerequisites**
- **Node.js**: 16+ installed
- **Package manager**: npm or yarn

**Environment Variables**
- **VITE_API_URL**: Base URL of the authentication API (e.g., `http://localhost:8080`).

**Run Locally**
- Install dependencies: `npm install` or `yarn install`
- Start dev server: `npm run dev` or `yarn dev`

**Build**
- Create production build: `npm run build` or `yarn build`

**Authentication Flow**
- The UI posts credentials to the backend login endpoint and receives a JWT.
- The JWT is stored in `localStorage` (or memory depending on implementation) and attached to subsequent API requests.

**Project Structure**
- **src/**: React components and pages
- **public/**: Static assets and index.html
- **vite.config.ts**: Vite configuration

**Testing & Linting**
- Run ESLint: `npm run lint` or `yarn lint` (if scripts present)

**Troubleshooting**
- If you get CORS errors, ensure the backend allows requests from the UI origin.
- Verify `VITE_API_URL` points to a running backend.

If you want, I can also add example environment files and a demo screenshot.
