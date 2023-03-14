# Vue 3 + Vite + Tailwind

## Tailwind

```shell
npm install -D tailwindcss@latest postcss@latest autoprefixer@latest

npx tailwindcss init -p
```

tailwind.config.cjs에

```
purge: ["./index.html", "./src/**/*.{vue,js,ts,jsx,tsx}"]
```
