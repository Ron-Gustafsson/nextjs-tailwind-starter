# nextjs-tailwind-starter

A reusable Next.js starter for new web projects, with TypeScript, Tailwind CSS, and consistent linting and formatting defaults.

## Stack and tools

- Next.js 16.4.3 with the App Router and Turbopack
- React 19.3.0 and TypeScript 5
- Tailwind CSS 4 with `@tailwindcss/turbopack`
- ESLint 9 with the Next.js configuration
- Prettier with `prettier-plugin-tailwindcss` for automatic Tailwind class sorting
- pnpm 12.16.1
- VS Code workspace settings and extension recommendations

## Requirements

- Node.js supported by both Next.js and the configured pnpm version
- pnpm 12.16.1, as specified in `package.json`
- Git and a GitHub account to create a repository from this template

## Use this template

1. Open `nextjs-tailwind-starter` on GitHub.
2. Select **Use this template → Create a new repository**.
3. Choose the owner, repository name, and visibility, then create the repository.
4. Clone your new repository and enter its directory:

   ```sh
   git clone https://github.com/YOUR-USERNAME/YOUR-REPOSITORY.git
   cd YOUR-REPOSITORY
   ```

## Local setup

Install dependencies and start the development server:

```sh
pnpm install
pnpm dev
```

Open [localhost:3000](http://localhost:3000). Edit `app/page.tsx` to update the home page.

## Available scripts

| Command             | Description                              |
| ------------------- | ---------------------------------------- |
| `pnpm dev`          | Start the development server.            |
| `pnpm build`        | Create an optimized production build.    |
| `pnpm start`        | Serve the production build locally.      |
| `pnpm lint`         | Check the project with ESLint.           |
| `pnpm lint:fix`     | Apply available automatic ESLint fixes.  |
| `pnpm format`       | Format project files with Prettier.      |
| `pnpm format:check` | Check formatting without changing files. |

Run `pnpm build` before `pnpm start`.

## VS Code setup

Open the repository root in VS Code and install the workspace's recommended extensions:

- ESLint (`dbaeumer.vscode-eslint`)
- Prettier (`esbenp.prettier-vscode`)
- Tailwind CSS IntelliSense (`bradlc.vscode-tailwindcss`)

The workspace settings use Prettier as the default formatter, format files on save, and apply ESLint fixes on explicit saves. JSONC files are excluded from format-on-save. CSS unknown-at-rule warnings are suppressed to accommodate Tailwind directives such as `@theme`.

## Project structure

```text
.
├── .vscode/
│   ├── extensions.json    # Recommended editor extensions
│   └── settings.json      # Workspace editor settings
├── app/
│   ├── globals.css        # Global styles and Tailwind theme
│   ├── layout.tsx         # Root layout, fonts, and metadata
│   └── page.tsx           # Home page
├── eslint.config.mjs      # ESLint configuration
├── next-env.d.ts          # Generated Next.js type declarations
├── next.config.ts         # Next.js and Tailwind integration
├── package.json           # Dependencies and scripts
├── pnpm-lock.yaml         # Locked dependency versions
├── pnpm-workspace.yaml    # pnpm workspace configuration
├── prettier.config.mjs    # Formatting and Tailwind class sorting
└── tsconfig.json          # TypeScript configuration
```

## Verification

Before committing changes, format the project and run the checks:

```sh
pnpm format
pnpm format:check
pnpm lint
pnpm build
```

## Customization

- Update the package name in `package.json` and adapt this README for your project.
- Set the title, description, document language, and fonts in `app/layout.tsx`.
- Replace the starter page in `app/page.tsx` and add routes under `app/`.
- Adjust global styles and Tailwind theme variables in `app/globals.css`.
- Create a `public/` directory when you need images, icons, or other static assets.
- Configure `next.config.ts` for your application's features and deployment environment.
