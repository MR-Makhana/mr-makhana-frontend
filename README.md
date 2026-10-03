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
        ▼
⚡ FastAPI Backend
        │
        ▼
🐘 PostgreSQL
```

The frontend can consume backend resources such as:

```text
📦 Products
   │
   ├── Get products
   ├── Get product details
   └── Product information

🗂️ Categories
   │
   ├── Get categories
   └── Category information
```

---

# 🔐 Environment Configuration

Create a local environment file when environment-specific configuration is required:

```text
.env.local
```

Example:

```env
NEXT_PUBLIC_API_URL=http://localhost:8000
```

For production, configure the appropriate API URL through the deployment platform's environment-variable settings.

### 🚨 Security

Never commit sensitive environment variables to Git.

```gitignore
.env
.env.local
.env.*.local
```

Only variables intended for client-side exposure should use the `NEXT_PUBLIC_` prefix.

---

# 🚀 Getting Started

## 1️⃣ Clone the Repository

```bash
git clone https://github.com/MR-Makhana/mr-makhana-frontend.git
```

## 2️⃣ Enter the Project

```bash
cd mr-makhana-frontend
```

## 3️⃣ Install Dependencies

This project uses **pnpm**.

```bash
pnpm install
```

## 4️⃣ Configure Environment Variables

Create:

```text
.env.local
```

Example:

```env
NEXT_PUBLIC_API_URL=http://localhost:8000
```

## 5️⃣ Start Development Server

```bash
pnpm dev
```

Open:

```text
http://localhost:3000
```

---

# 🏗️ Production Build

Create a production build:

```bash
pnpm build
```

Start the production server:

```bash
pnpm start
```

---

# 🧹 Code Quality

Before pushing changes:

```bash
pnpm lint
```

Recommended development flow:

```text
👨‍💻 Code
   ↓
🧹 Lint
   ↓
🧪 Test
   ↓
🏗️ Build
   ↓
🚀 Deploy
```

---

# ☁️ Deployment

The frontend is designed for modern cloud deployment and can be deployed through **Vercel**.

```text
                    👨‍💻 Developer
                         │
                         ▼
                    Git Push
                         │
                         ▼
                    🐙 GitHub
                         │
                         ▼
                    ▲ Vercel
                         │
                         ▼
                    🌐 Production
                         │
                         ▼
                  🥜 MR Makhana
```

### Deployment Responsibilities

The frontend repository focuses on:

- 🖥️ Application code
- 🎨 UI/UX
- 🔌 API integration
- 🏗️ Frontend build
- 🚀 Frontend deployment

AWS infrastructure, Terraform, Docker infrastructure, Nginx and monitoring are maintained separately in:

**`mr-makhana-infrastructure`**

---

# 🔗 Project Ecosystem

MR Makhana is organized into separate repositories for cleaner architecture and maintainability.

### 🖥️ Frontend

**`mr-makhana-frontend`**

```text
Next.js
React
TypeScript
Tailwind CSS
shadcn/ui
```

### ⚙️ Backend

**`mr-makhana-backend`**

```text
Python
FastAPI
PostgreSQL
SQLAlchemy
Amazon S3
```

### ☁️ Infrastructure

**`mr-makhana-infrastructure`**

```text
AWS
Terraform
Docker
Nginx
CI/CD
Security
Monitoring
```

```text
          🥜 MR MAKHANA
                │
      ┌─────────┼─────────┐
      │         │         │
      ▼         ▼         ▼
   🖥️ UI     ⚙️ API    ☁️ INFRA
      │         │         │
   Next.js   FastAPI     AWS
   React     Python    Terraform
   TypeScript PostgreSQL Docker
                        CI/CD
```

---

# 📊 Project Status

| Component | Status |
|---|---|
| 🥜 Premium Storefront | ✅ |
| 🎨 Modern UI | ✅ |
| 📱 Responsive Design | ✅ |
| ▲ Next.js | ✅ |
| ⚛️ React | ✅ |
| 🔷 TypeScript | ✅ |
| 🎨 Tailwind CSS | ✅ |
| 🧩 shadcn/ui | ✅ |
| ✨ Animations | ✅ |
| 🛍️ Product Interface | ✅ |
| 🗂️ Category Interface | ✅ |
| 🔌 API Integration | 🚧 |
| 🔐 Authentication | 🔜 |
| 🛒 Shopping Cart | 🔜 |
| ❤️ Wishlist | 🔜 |
| 📦 Orders | 🔜 |
| 💳 Payment Integration | 🔜 |
| 👨‍💼 Admin Dashboard | 🔜 |

---

# 🗺️ Roadmap

## 🟢 Phase 1 — Storefront

- [x] 🥜 Premium storefront
- [x] 🎨 Modern UI
- [x] 📱 Responsive design
- [x] 🛍️ Product presentation
- [x] 🗂️ Category presentation
- [x] ✨ Animations

## 🟡 Phase 2 — Shopping Experience

- [ ] 🔎 Product search
- [ ] 🛒 Shopping cart
- [ ] ❤️ Wishlist
- [ ] 👤 User accounts
- [ ] 🔐 Authentication
- [ ] 💳 Checkout
- [ ] 📦 Order tracking

## 🔵 Phase 3 — Customer Experience

- [ ] ⭐ Product reviews
- [ ] 🔔 Notifications
- [ ] 📧 Email integration
- [ ] 🎁 Offers & coupons
- [ ] 📦 Order history
- [ ] 👤 Profile management

## 🟣 Phase 4 — Production

- [ ] 🚀 CI/CD
- [ ] 🧪 Automated testing
- [ ] 🔐 Security checks
- [ ] 📊 Performance monitoring
- [ ] 📈 Analytics
- [ ] ♻️ Performance optimization

---

# 🧪 Development Workflow

```text
              👨‍💻 Developer
                    │
                    ▼
               🌿 Feature Branch
                    │
                    ▼
                 💻 Code
                    │
                    ▼
                 🧹 Lint
                    │
                    ▼
                 🧪 Test
                    │
                    ▼
                🔍 Review
                    │
                    ▼
                🔀 Pull Request
                    │
                    ▼
                  🐙 GitHub
                    │
                    ▼
                🚀 Deployment
```

---

# 🎯 Frontend Goals

The frontend is being built with a focus on:

```text
🎨 Beautiful UI
      ↓
📱 Responsive Experience
      ↓
⚡ Fast Performance
      ↓
🧩 Reusable Components
      ↓
🔷 Type Safety
      ↓
🔌 Clean API Integration
      ↓
♻️ Maintainable Code
      ↓
🚀 Production Readiness
```

---

# 🌟 Why MR Makhana?

MR Makhana aims to combine:

- 🌰 Premium Makhana products
- 🎨 Modern digital experience
- ⚡ Fast web performance
- 📱 Mobile-first usability
- ☁️ Cloud-ready architecture
- 🔐 Secure engineering practices
- 🚀 Scalable application design

---

# 📚 Related Repository

### ⚙️ Backend

👉 **[mr-makhana-backend](https://github.com/MR-Makhana/mr-makhana-backend)**

### ☁️ Infrastructure

👉 **[mr-makhana-infrastructure](https://github.com/MR-Makhana/mr-makhana-infrastructure)**

---

# 👨‍💻 Author

## Navnit Kumar

**DevOps Engineer | Cloud & DevSecOps Enthusiast**

### 🛠️ Focus Areas

```text
☁️ AWS
🐳 Docker
☸️ Kubernetes
🏗️ Terraform
🔄 CI/CD
🐧 Linux
🔐 Cloud Security
🛡️ DevSecOps
⚙️ Infrastructure Automation
```

### 🌐 Connect

<p align="center">

<a href="https://github.com/navnitkumar927">
  <img src="https://img.shields.io/badge/GitHub-Navnit%20Kumar-181717?style=for-the-badge&logo=github" />
</a>

<a href="https://www.linkedin.com/in/navnit-kumar-0b7475307/">
  <img src="https://img.shields.io/badge/LinkedIn-Navnit%20Kumar-0A66C2?style=for-the-badge&logo=linkedin" />
</a>

</p>

---

# 🥜 MR MAKHANA

<p align="center">

### 🌰 Premium Makhana • ⚛️ Next.js • 🔷 TypeScript • 🎨 Tailwind CSS

**Built with ❤️ for a modern e-commerce experience.**

</p>

<p align="center">

🥜 **MR MAKHANA** 🥜

</p>
