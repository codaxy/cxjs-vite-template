# CxJS + Vite

A starter template for CxJS with Vite, TypeScript, and Tailwind CSS.

## Setup

```bash
npm install
npm run dev
```

## Scripts

- `npm run dev` - Start development server with HMR
- `npm run build` - Build for production
- `npm run preview` - Preview production build

## TypeScript Configuration

CxJS uses a custom JSX transform. Configure `tsconfig.json`:

```json
{
  "compilerOptions": {
    "jsx": "react-jsx",
    "jsxImportSource": "cx",
    "module": "es2022",
    "moduleResolution": "bundler",
    "esModuleInterop": true
  }
}
```

## Hot Module Replacement

For HMR to work correctly with CxJS, add this at the end of your entry file:

```ts
if (import.meta.hot) import.meta.hot.accept();
```

## Tailwind CSS

Tailwind is configured via `@tailwindcss/vite` plugin. Import it in a CSS file:

```css
@import "tailwindcss";
```
