# 🥜 MR Makhana — Frontend

<p align="center">
  <img src="https://img.shields.io/badge/🥜-MR%20MAKHANA-F4B400?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=next.js&logoColor=white" />
  <img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" />
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white" />
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Tailwind%20CSS-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white" />
  <img src="https://img.shields.io/badge/shadcn%2Fui-000000?style=for-the-badge" />
  <img src="https://img.shields.io/badge/Framer%20Motion-EF008C?style=for-the-badge&logo=framer&logoColor=white" />
  <img src="https://img.shields.io/badge/Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white" />
</p>

<p align="center">

### 🌰 Premium Makhana E-Commerce Experience

A modern, responsive and production-oriented storefront for **MR Makhana**.

</p>

---

## 🥜 About MR Makhana

**MR Makhana** is a modern e-commerce platform focused on delivering premium roasted Makhana products through a clean, responsive and engaging shopping experience.

This repository contains the **frontend application** built with **Next.js, React and TypeScript**.

The frontend is designed to provide:

- 🛍️ Premium e-commerce experience
- ⚡ Fast and responsive user interface
- 📱 Mobile-first design
- 🎨 Modern component-based UI
- ✨ Smooth animations and interactions
- 🔌 REST API integration
- 🖼️ Product image support
- 🛒 Scalable e-commerce architecture

---

# ✨ Highlights

```text
                    🥜 MR MAKHANA
                          │
          ┌───────────────┴───────────────┐
          │                               │
       🎨 UI/UX                       ⚡ Performance
          │                               │
          ▼                               ▼
    🧩 Components                    Next.js
          │                               │
          └───────────────┬───────────────┘
                          │
                          ▼
                    🔌 REST API
                          │
                          ▼
                  ⚙️ Backend Services
```

---

# 🛍️ Storefront Features

### 🌰 Product Experience

- 🛍️ Product listing
- 🗂️ Product categories
- ⭐ Featured products
- 💰 Product pricing
- 🏷️ Compare-at / discount pricing
- 📦 Stock quantity display
- 🖼️ Product images
- 🔎 Product-focused browsing
- ✨ Premium product presentation

### 📱 Responsive Experience

The storefront is designed for:

- 📱 Mobile
- 📲 Tablet
- 💻 Laptop
- 🖥️ Desktop

```text
📱 Mobile
   ↓
📲 Tablet
   ↓
💻 Laptop
   ↓
🖥️ Desktop
```

### 🎨 User Interface

- 🧩 Reusable UI components
- 🎨 Tailwind CSS styling
- 🖤 shadcn/ui components
- ✨ Smooth animations
- 🧭 Responsive navigation
- 📐 Consistent layouts
- ⚡ Interactive elements

---

# 🧰 Tech Stack

| Technology | Purpose |
|---|---|
| ▲ **Next.js** | React framework |
| ⚛️ **React** | UI development |
| 🔷 **TypeScript** | Type-safe development |
| 🎨 **Tailwind CSS** | Styling |
| 🧩 **shadcn/ui** | UI components |
| ✨ **Framer Motion** | Animations |
| 🔌 **REST API** | Backend communication |
| ▲ **Vercel** | Frontend deployment |

---

# 🏗️ Frontend Architecture

```text
                         🌐 USER
                           │
                           ▼
                  ┌──────────────────┐
                  │   🥜 MR Makhana  │
                  │    Storefront    │
                  └────────┬─────────┘
                           │
                           ▼
                  ┌──────────────────┐
                  │     Next.js      │
                  │      ⚛️ React    │
                  └────────┬─────────┘
                           │
             ┌─────────────┼─────────────┐
             │             │             │
             ▼             ▼             ▼
        🛍️ Products    🗂️ Categories   🧩 UI
             │             │             │
             └─────────────┼─────────────┘
                           │
                           ▼
                     🔌 REST API
                           │
                           ▼
                  ⚙️ FastAPI Backend
```

---

# 📁 Project Structure

```text
mr-makhana-frontend/
│
├── 📂 app/
│   ├── layout.*
│   ├── page.*
│   └── ...
│
├── 🧩 components/
│   └── ui/
│
├── 📚 lib/
│
├── 🖼️ public/
│
├── ⚙️ components.json
├── ⚙️ next.config.mjs
├── 📦 package.json
├── 🔒 pnpm-lock.yaml
├── ⚙️ pnpm-workspace.yaml
├── 🎨 postcss.config.mjs
├── 🔷 tsconfig.json
├── 🚫 .gitignore
└── 📖 README.md
```

> The exact application structure may evolve as new storefront features are introduced.

---

# 🔌 API Integration

The frontend communicates with the MR Makhana backend through REST APIs.

```text
🥜 Next.js Frontend
        │
        │ HTTPS / REST
