# Vue 3 + Vite + Tailwind CSS Setup

This project uses **Vue 3**, **Vite**, **Tailwind CSS**, **Vue Router**, **Headless UI**, and **Heroicons**.

---

## 1️⃣ Create a Vite + Vue Project

```bash
npm create vite@latest
```

## 2️⃣ Install Tailwind CSS

```bash
npm install tailwindcss @tailwindcss/vite
npm install @headlessui/vue @heroicons/vue
```

## 3️⃣ Configure Tailwind with Vite

vite.config.js

```bash
import { defineConfig } from 'vite'
import tailwindcss from '@tailwindcss/vite'

export default defineConfig({
  plugins: [
    tailwindcss(),
  ],
})

```

## 4️⃣ Add Tailwind to Styles

src/style.css

```bash
@import "tailwindcss";

```

## 5️⃣ Install Vue Router

```bash
npm install vue-router@4

```

## 6️⃣ Create Router Configuration

Create a new directory:

```bash
src/router/index.js

```

src/router/index.js

```bash
import { createRouter, createWebHistory } from 'vue-router'

import HomePage from '../views/HomeView.vue'
import AboutView from '../views/AboutView.vue'
import ProductItemPage from '../views/ProductItemView.vue'

const routes = [
  { path: '/', component: HomePage },
  { path: '/about', component: AboutView },
  { path: '/product/:id', component: ProductItemPage },
]

const router = createRouter({
  history: createWebHistory(import.meta.env.BASE_URL),
  routes,
})

export default router


```

## 7️⃣ App Layout Setup

App.vue

```bash
<script setup>
import Navbar from './components/Navbar.vue'
import Footer from './components/Footer.vue'
import Navbar2 from './components/Navbar2.vue'
import { RouterView } from 'vue-router'
</script>

<template>
  <Navbar />
  <RouterView />
  <Footer />
</template>


```

## 📁 Project Structure (Recommended)

```bash
src/
├─ components/
│  ├─ Navbar.vue
│  ├─ Navbar2.vue
│  └─ Footer.vue
├─ views/
│  ├─ HomeView.vue
│  ├─ AboutView.vue
│  └─ ProductItemView.vue
├─ router/
│  └─ index.js
├─ App.vue
├─ main.js
└─ style.css


```




