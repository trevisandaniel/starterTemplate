# Nuxt 3 + Tailwind + Pinia Starter Template

![Nuxt 3](https://img.shields.io/badge/Nuxt-3.16.2-00DC82?style=flat-square&logo=nuxt.js)
![Vue 3](https://img.shields.io/badge/Vue-3.5.13-4FC08D?style=flat-square&logo=vue.js)
![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-3.4.1-38B2AC?style=flat-square&logo=tailwind-css)
![Pinia](https://img.shields.io/badge/Pinia-0.11.0-yellow?style=flat-square&logo=pinia)

A pre-configured Nuxt 3 starter template that includes Tailwind CSS for styling, Pinia for state management, and ApexCharts for data visualization. Perfect for quickly starting new projects without the hassle of initial setup.

## Features

- ⚡️ **Nuxt 3** - The intuitive Vue framework
- 🎨 **Tailwind CSS 3.4** - A utility-first CSS framework
- 📦 **Pinia** - The official Vue store for state management
- 📊 **ApexCharts** - Interactive charting library
- 🚀 **Modern tooling** - Latest Vue ecosystem packages

## Prerequisites

- Node.js (v18+)
- npm or yarn or pnpm

## Getting Started

### Setup

Clone this repository and install the dependencies:

```bash
# Clone the repository
git clone https://github.com/trevisandaniel/starterTemplate.git my-project
cd my-project

# Install dependencies
npm install
# or
yarn install
```

### Development

Start the development server on `http://localhost:3000`:

```bash
npm run dev
# or
yarn dev
```

### Production

Build the application for production:

```bash
npm run build
# or
yarn build
```

Preview the production build:

```bash
npm run preview
# or
yarn preview
```

Generate a static version of the site:

```bash
npm run generate
# or
yarn generate
```

## Project Structure

```
nuxt-app/
├── assets/             # Static assets like CSS, fonts, images
│   └── css/
│       └── tailwind.css
├── components/         # Vue components
├── composables/        # Reusable Vue composition functions
├── layouts/            # Page layouts
├── pages/              # Application pages
├── public/             # Public static assets
├── stores/             # Pinia stores
├── .gitignore          # Git ignore file
├── app.vue             # Main application component
├── nuxt.config.ts      # Nuxt configuration
├── package.json        # Project dependencies and scripts
├── tailwind.config.js  # Tailwind CSS configuration
└── tsconfig.json       # TypeScript configuration
```

## Customization

### Tailwind CSS

Tailwind CSS is pre-configured. You can customize the theme in `tailwind.config.js`:

```js
/** @type {import('tailwindcss').Config} */
export default {
  content: [
    "./components/**/*.{js,vue,ts}",
    "./layouts/**/*.vue",
    "./pages/**/*.vue",
    "./plugins/**/*.{js,ts}",
    "./app.vue",
    "./error.vue"
  ],
  theme: {
    extend: {
      // Your custom theme extensions
      colors: {
        'brand': '#4f46e5',
      }
    },
  },
  plugins: [],
}
```

### Pinia Stores

Create new stores in the `stores` directory:

```ts
// stores/counter.ts
import { defineStore } from 'pinia'

export const useCounterStore = defineStore('counter', {
  state: () => ({
    count: 0
  }),
  actions: {
    increment() {
      this.count++
    }
  }
})
```

### ApexCharts

The project includes Vue3-ApexCharts for data visualization. Use it in your components:

```vue
<template>
  <apexchart type="bar" :options="chartOptions" :series="series"></apexchart>
</template>

<script setup>
const chartOptions = {
  chart: {
    id: 'basic-bar'
  },
  xaxis: {
    categories: [1991, 1992, 1993, 1994, 1995, 1996, 1997, 1998]
  }
}

const series = [{
  name: 'series-1',
  data: [30, 40, 45, 50, 49, 60, 70, 91]
}]
</script>
```

## Dependencies

### Core

- `nuxt`: ^3.16.2
- `vue`: ^3.5.13
- `vue-router`: ^4.5.0

### State Management

- `@pinia/nuxt`: ^0.11.0

### UI and Visualization

- `vue3-apexcharts`: ^1.8.0
- `tailwindcss`: ^3.4.1
- `@nuxtjs/tailwindcss`: ^6.13.2
- `postcss`: ^8.5.3
- `autoprefixer`: ^10.4.21

## License

[MIT](LICENSE)