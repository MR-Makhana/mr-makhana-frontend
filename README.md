# 🥜 MR Makhana

### 🌰 Premium Makhana E-Commerce Platform

<p align="center">

  <img src="https://img.shields.io/badge/Next.js-000000?style=for-the-badge&logo=next.js&logoColor=white" />
  <img src="https://img.shields.io/badge/React-20232A?style=for-the-badge&logo=react&logoColor=61DAFB" />
  <img src="https://img.shields.io/badge/TypeScript-3178C6?style=for-the-badge&logo=typescript&logoColor=white" />
  <img src="https://img.shields.io/badge/FastAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white" />
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" />

</p>

<p align="center">

  <img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=for-the-badge&logo=postgresql&logoColor=white" />
  <img src="https://img.shields.io/badge/Amazon%20S3-569A31?style=for-the-badge&logo=amazons3&logoColor=white" />
  <img src="https://img.shields.io/badge/AWS%20EC2-FF9900?style=for-the-badge&logo=amazonec2&logoColor=white" />
  <img src="https://img.shields.io/badge/AWS%20IAM-DD344C?style=for-the-badge&logo=amazoniam&logoColor=white" />
  <img src="https://img.shields.io/badge/Vercel-000000?style=for-the-badge&logo=vercel&logoColor=white" />

</p>

<p align="center">

  <img src="https://img.shields.io/badge/SQLAlchemy-D71F00?style=for-the-badge&logo=sqlalchemy&logoColor=white" />
  <img src="https://img.shields.io/badge/Tailwind_CSS-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white" />
  <img src="https://img.shields.io/badge/shadcn/ui-000000?style=for-the-badge" />
  <img src="https://img.shields.io/badge/boto3-AWS_SDK-FF9900?style=for-the-badge" />

</p>

---

## 🌟 About The Project

**MR Makhana** is a modern, cloud-ready full-stack e-commerce platform built for selling premium roasted Makhana products online.

The platform combines a modern **Next.js storefront**, **FastAPI REST API**, **PostgreSQL**, **Amazon S3**, **AWS EC2**, and **AWS IAM role-based authentication** into a production-oriented architecture.

The project focuses on:

- 🛍️ Modern e-commerce experience
- ⚡ High-performance frontend
- 🔌 REST API architecture
- ☁️ AWS cloud infrastructure
- 🔐 Secure IAM-based authentication
- 🗄️ PostgreSQL database architecture
- 🪣 S3 object storage
- 🚀 DevOps-ready deployment
- 📈 Scalable application architecture
- 🛡️ Security-focused engineering

---

# 🥜 MR Makhana Architecture

```text
                         🌐 CUSTOMER
                              │
                              ▼
                   ┌────────────────────┐
                   │   Next.js Store    │
                   │     ⚛️ React       │
                   │    ☁️ Vercel       │
                   └─────────┬──────────┘
                             │
                       HTTPS / REST
                             │
                             ▼
                   ┌────────────────────┐
                   │   FastAPI Backend  │
                   │      🐍 Python     │
                   │      ☁️ AWS EC2     │
                   └─────────┬──────────┘
                             │
                  ┌──────────┴──────────┐
                  │                     │
                  ▼                     ▼
        ┌──────────────────┐   ┌──────────────────┐
        │   PostgreSQL     │   │    Amazon S3     │
        │    Database      │   │  Product Images  │
        └──────────────────┘   └────────┬─────────┘
                                        │
                                        │ 🔐 IAM Role
                                        ▼
                               ┌──────────────────┐
                               │    AWS IAM       │
                               │ Role-Based Auth  │
                               └──────────────────┘
```

---

# ✨ Key Features

## 🛍️ E-Commerce Storefront

- 🌰 Premium Makhana storefront
- 📱 Fully responsive design
- 🖥️ Desktop, tablet & mobile support
- 🛒 Product listing
- 🗂️ Product categories
- ⭐ Featured products
- 💰 Product pricing
- 🏷️ Discount / compare-at pricing
- 📦 Stock quantity
- 🖼️ Product image support
- ✨ Premium animations
- 🧩 Modern UI components
- 📱 Mobile-friendly navigation

---

## ⚡ FastAPI Backend

- 🚀 FastAPI REST API
- 📦 Product CRUD operations
- 🗂️ Category management
- 🐘 PostgreSQL integration
- 🔗 SQLAlchemy ORM
- ✅ Pydantic validation
- 📖 Automatic Swagger documentation
- 📚 OpenAPI specification
- ❤️ Health check endpoint
- ⚙️ Environment-based configuration
- ☁️ Amazon S3 integration
- 🖼️ Product image upload service
- 🔐 Unique S3 object naming
- ⚠️ HTTP error handling
- 🔗 Database relationships

---

# ☁️ AWS Cloud Architecture

MR Makhana uses AWS for backend infrastructure and object storage.

| AWS Service | Purpose |
|---|---|
| ☁️ **EC2** | FastAPI backend hosting |
| 🪣 **S3** | Product image storage |
| 🔐 **IAM** | Role-based AWS authentication |
| 🐍 **boto3** | AWS SDK integration |

The backend communicates with Amazon S3 through an **EC2 IAM Role**, avoiding long-lived AWS credentials inside the application.

---

# 🔐 Security Architecture

One of the important security aspects of MR Makhana is **IAM role-based AWS authentication**.

```text
              🐍 FastAPI
                   │
                   ▼
                boto3
                   │
                   ▼
              ☁️ AWS EC2
                   │
                   ▼
             🔐 IAM Role
                   │
                   ▼
              🪣 Amazon S3
```

### 🛡️ Security Benefits

- 🔐 IAM role-based authentication
- 🚫 No hard-coded AWS credentials
- 🔑 Temporary AWS credentials
- ⚙️ Environment-based configuration
- 🚫 `.env` excluded from Git
- 🗄️ Database credentials outside source code
- 🪣 S3 permissions controlled through IAM
- ✅ Pydantic request validation
- ⚠️ FastAPI exception handling
- 🔀 Unique S3 object names
- 🔒 Separation of application code and secrets
- 🎯 Least-privilege permissions where applicable

The project specifically avoids storing:

```text
AWS_ACCESS_KEY_ID
AWS_SECRET_ACCESS_KEY
```

inside the application.

---

# 🖼️ Product Image Storage

Product images are stored in **Amazon S3**, while the corresponding image URL/reference is stored with the product data.

```text
👨‍💻 Admin / Customer
        │
        ▼
┌───────────────────┐
│  Next.js Frontend │
└─────────┬─────────┘
          │
          ▼
┌───────────────────┐
│  FastAPI Backend  │
└─────────┬─────────┘
          │
        boto3
          │
          ▼
┌───────────────────┐
│    Amazon S3      │
│                   │
│    products/      │
│      image.jpg    │
└─────────┬─────────┘
          │
          ▼
     Image URL
          │
          ▼
┌───────────────────┐
│    PostgreSQL     │
│  Product Record   │
└───────────────────┘
```

### 🪣 Example S3 Structure

```text
mr-makhana-product-images/
│
└── products/
    ├── image-1.jpg
    ├── image-2.jpg
    ├── image-3.png
    └── image-4.webp
```

---

# 🧰 Technology Stack

## 🎨 Frontend

| Technology | Purpose |
|---|---|
| ⚛️ React | UI |
| ▲ Next.js | Frontend framework |
| 🔷 TypeScript | Type safety |
| 🎨 Tailwind CSS | Styling |
| 🧩 shadcn/ui | UI components |
| ✨ Framer Motion | Animations |
| ▲ Vercel | Frontend hosting |

## 🐍 Backend

| Technology | Purpose |
|---|---|
| 🐍 Python | Backend language |
| ⚡ FastAPI | REST API |
| 🚀 Uvicorn | ASGI server |
| 🔗 SQLAlchemy | ORM |
| ✅ Pydantic | Validation |
| ☁️ boto3 | AWS SDK |
| 📤 python-multipart | File uploads |

## 🗄️ Database & Cloud

| Technology | Purpose |
|---|---|
| 🐘 PostgreSQL | Relational database |
| ☁️ AWS EC2 | Backend hosting |
| 🪣 Amazon S3 | Object storage |
| 🔐 AWS IAM | Authentication & permissions |
| ▲ Vercel | Frontend deployment |

---

# 📁 Project Structure

## 🎨 Frontend

```text
mk-makhana/
│
├── app/
│
├── components/
│   └── ui/
│
├── lib/
│
├── public/
│
├── .gitignore
├── components.json
├── next.config.mjs
├── package.json
├── pnpm-lock.yaml
├── pnpm-workspace.yaml
├── postcss.config.mjs
└── tsconfig.json
```

## 🐍 Backend

```text
mr-makhana-backend/
│
├── app/
│   │
│   ├── database/
│   │   └── connection.py
│   │
│   ├── models/
│   │   ├── product.py
│   │   └── category.py
│   │
│   ├── routes/
│   │   ├── products.py
│   │   └── categories.py
│   │
│   ├── services/
│   │   └── s3.py
│   │
│   ├── schemas.py
│   └── main.py
│
├── requirements.txt
├── .gitignore
└── .env
```

---

# 🔌 REST API

## 📦 Products

| Method | Endpoint | Description |
|---|---|---|
| 🟢 GET | `/api/products/` | Get all products |
| 🟡 POST | `/api/products/` | Create product |
| 🟢 GET | `/api/products/{product_id}` | Get product |
| 🟠 PUT | `/api/products/{product_id}` | Update product |
| 🔴 DELETE | `/api/products/{product_id}` | Delete product |

## 🗂️ Categories

| Method | Endpoint | Description |
|---|---|---|
| 🟢 GET | `/api/categories/` | Get all categories |
| 🟡 POST | `/api/categories/` | Create category |
| 🟢 GET | `/api/categories/{category_id}` | Get category |

## ❤️ Health Check

```http
GET /health
```

Response:

```json
{
  "status": "ok"
}
```

---

# 📖 API Documentation

FastAPI automatically provides interactive API documentation.

### 🔵 Swagger UI

```text
http://YOUR_SERVER_IP:8000/docs
```

### 📘 OpenAPI

```text
http://YOUR_SERVER_IP:8000/openapi.json
```

Swagger can be used to test:

- GET requests
- POST requests
- PUT requests
- DELETE requests
- Request validation
- API responses
- HTTP status codes

---

# 🐍 Backend Setup

## 1️⃣ Clone Repository

```bash
git clone https://github.com/navnitkumar927/mr-makhana-backend.git
cd mr-makhana-backend
```

## 2️⃣ Create Virtual Environment

```bash
python3 -m venv venv
```

## 3️⃣ Activate Environment

### Linux / macOS

```bash
source venv/bin/activate
```

## 4️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

## 5️⃣ Configure Environment Variables

Create:

```text
.env
```

Example:

```env
DATABASE_URL=postgresql+psycopg2://USERNAME:PASSWORD@HOST:5432/DATABASE

S3_BUCKET=YOUR_S3_BUCKET
AWS_REGION=us-east-1
```

> ⚠️ **Never commit `.env` to GitHub.**

## 6️⃣ Start FastAPI

```bash
uvicorn app.main:app --host 0.0.0.0 --port 8000
```

### 🔥 Development Mode

```bash
uvicorn app.main:app --reload
```

Backend:

```text
http://localhost:8000
```

Swagger:

```text
http://localhost:8000/docs
```

---

# 🖥️ Frontend Setup

## 1️⃣ Clone Repository

```bash
git clone https://github.com/navnitkumar927/mk-makhana.git
```

## 2️⃣ Enter Project

```bash
cd mk-makhana
```

## 3️⃣ Install Dependencies

```bash
pnpm install
```

## 4️⃣ Start Development Server

```bash
pnpm dev
```

Frontend:

```text
http://localhost:3000
```

---

# 🐘 PostgreSQL

PostgreSQL is used as the primary relational database.

Current core data includes:

```text
PostgreSQL
│
├── categories
│
└── products
```

Example configuration:

```env
DATABASE_URL=postgresql+psycopg2://USERNAME:PASSWORD@HOST:5432/DATABASE
```

SQLAlchemy provides the ORM layer between FastAPI and PostgreSQL.

---

# 🪣 Amazon S3

Amazon S3 is used for product image storage.

Example:

```text
mr-makhana-product-images/
│
└── products/
    ├── image-1.jpg
    ├── image-2.jpg
    ├── image-3.png
    └── image-4.webp
```

Backend configuration:

```env
S3_BUCKET=YOUR_S3_BUCKET
AWS_REGION=us-east-1
```

---

# 🧪 AWS / S3 Testing

### 🔍 Verify AWS Identity

```bash
aws sts get-caller-identity
```

### 🪣 Test S3 Bucket

```bash
aws s3 ls s3://YOUR_S3_BUCKET
```

### 🖼️ Test Product Images

```bash
aws s3 ls s3://YOUR_S3_BUCKET/products/
```

---

# 🧪 API Testing

### ❤️ Health Check

```bash
curl http://localhost:8000/health
```

Expected:

```json
{
  "status": "ok"
}
```

### 📦 Get Products

```bash
curl http://localhost:8000/api/products/
```

### 🗂️ Get Categories

```bash
curl http://localhost:8000/api/categories/
```

### ➕ Create Category

```bash
curl -X POST http://localhost:8000/api/categories/ \
-H "Content-Type: application/json" \
-d '{
  "name": "Classic Makhana",
  "slug": "classic-makhana",
  "description": "Classic roasted makhana snacks.",
  "image_url": null,
  "is_active": true
}'
```

---

# 📦 Example Product

```json
{
  "name": "Classic Salted Makhana",
  "slug": "classic-salted-makhana",
  "description": "Crunchy roasted makhana with a delicious light salted flavour.",
  "price": 199,
  "compare_at_price": 249,
  "image_url": "https://example.com/classic-makhana.jpg",
  "stock_quantity": 100,
  "is_active": true,
  "is_featured": true,
  "category_id": 1
}
```

---

# 🚀 Deployment Architecture

MR Makhana is designed around a **Vercel + AWS deployment architecture**.

```text
                         🌐 INTERNET
                              │
                              ▼
                   ┌────────────────────┐
                   │       Vercel       │
                   │    Next.js App     │
                   └─────────┬──────────┘
                             │
                          REST API
                             │
                             ▼
                   ┌────────────────────┐
                   │      AWS EC2       │
                   │ FastAPI + Uvicorn  │
                   └─────────┬──────────┘
                             │
                  ┌──────────┴──────────┐
                  │                     │
                  ▼                     ▼
          ┌───────────────┐     ┌───────────────┐
          │  PostgreSQL   │     │   Amazon S3   │
          │    Database   │     │ Product Images│
          └───────────────┘     └───────────────┘
```

---

# 📊 Project Status

| Component | Status |
|---|---|
| 🥜 Premium Storefront | ✅ |
| 📱 Responsive UI | ✅ |
| ▲ Next.js Frontend | ✅ |
| ⚡ FastAPI Backend | ✅ |
| 📦 Product API | ✅ |
| 🗂️ Category API | ✅ |
| 🐘 PostgreSQL | ✅ |
| 🔗 SQLAlchemy | ✅ |
| 📖 Swagger Documentation | ✅ |
| ☁️ AWS EC2 | ✅ |
| 🔐 AWS IAM Role | ✅ |
| 🪣 Amazon S3 | ✅ |
| 🐍 boto3 Integration | ✅ |
| 📤 S3 Upload Service | ✅ |
| 🖼️ Product Image Upload API | 🚧 |
| 🔗 Frontend API Integration | 🚧 |
| 🔐 Authentication | 🔜 |
| 🛒 Shopping Cart | 🔜 |
| ❤️ Wishlist | 🔜 |
| 📦 Orders | 🔜 |
| 💳 Payment Gateway | 🔜 |
| 🛠️ Admin Dashboard | 🔜 |
| 🔄 CI/CD | 🔜 |
| 📊 Monitoring | 🔜 |

---

# 🗺️ Roadmap

## 🟢 Phase 1 — Core Platform

- [x] 🥜 Premium storefront
- [x] 📱 Responsive frontend
- [x] 📦 Product API
- [x] 🗂️ Category API
- [x] 🐘 PostgreSQL integration
- [x] 🔗 SQLAlchemy integration
- [x] ☁️ AWS EC2 deployment
- [x] 🪣 Amazon S3 integration
- [x] 🔐 IAM role configuration
- [x] 📤 S3 upload service

## 🟡 Phase 2 — E-Commerce

- [ ] 🔐 User authentication
- [ ] 👤 User accounts
- [ ] 🛒 Shopping cart
- [ ] ❤️ Wishlist
- [ ] 💳 Checkout
- [ ] 📦 Orders
- [ ] 💰 Payment gateway
- [ ] 🚚 Order tracking
- [ ] 📧 Email notifications

## 🔵 Phase 3 — Admin Platform

- [ ] 🔐 Admin authentication
- [ ] 📊 Admin dashboard
- [ ] 📦 Product management
- [ ] 🗂️ Category management
- [ ] 📊 Inventory management
- [ ] 📦 Order management
- [ ] 🖼️ Product image management
- [ ] 📈 Analytics dashboard

## 🟣 Phase 4 — DevOps & Production

- [ ] 🐳 Docker
- [ ] 🐳 Docker Compose
- [ ] 🔄 GitHub Actions
- [ ] 🚀 Automated CI/CD
- [ ] 🛡️ Security scanning
- [ ] 🏗️ Infrastructure as Code
- [ ] 📊 Application monitoring
- [ ] 📝 Centralized logging
- [ ] 🔒 HTTPS
- [ ] 🌐 Production domain
- [ ] 💾 Automated backups
- [ ] ☁️ CloudWatch monitoring

---

# 🎯 Project Goals

MR Makhana is being developed as a production-oriented e-commerce platform focused on:

```text
🎨 Modern Frontend
        ↓
🔌 REST API Architecture
        ↓
☁️ Cloud Infrastructure
        ↓
🔐 Secure IAM Architecture
        ↓
🪣 Object Storage
        ↓
🗄️ Database Engineering
        ↓
🚀 DevOps Automation
        ↓
🛡️ Secure Deployment
        ↓
📈 Scalable Architecture
        ↓
🏭 Production Engineering
```

---

# 🔒 Environment Variables

Example backend `.env`:

```env
DATABASE_URL=postgresql+psycopg2://USERNAME:PASSWORD@HOST:5432/DATABASE

S3_BUCKET=YOUR_S3_BUCKET
AWS_REGION=us-east-1
```

### 🚨 Security Rule

Never commit `.env` to GitHub.

Recommended `.gitignore`:

```gitignore
.env
.venv/
venv/
__pycache__/
*.pyc
```

---

# 🧹 Useful Backend Commands

### 🐍 Activate Environment

```bash
source venv/bin/activate
```

### 🔎 Check Python

```bash
python --version
```

### 📦 Check Installed Packages

```bash
pip freeze
```

### 🧪 Compile Python

```bash
python -m py_compile app/main.py
```

### 🚀 Start Server

```bash
uvicorn app.main:app --host 0.0.0.0 --port 8000
```

### 🔍 Check Uvicorn

```bash
ps aux | grep uvicorn
```

### ❤️ Check API

```bash
curl http://localhost:8000/health
```

---

# 📚 Repositories

### 🎨 Frontend

👉 https://github.com/navnitkumar927/mk-makhana

### 🐍 Backend

👉 https://github.com/navnitkumar927/mr-makhana-backend

---

# 👨‍💻 Author

## Navnit Kumar

**DevOps Engineer | Cloud & DevSecOps Enthusiast**

### 🛠️ Focus Areas

- ☁️ AWS
- 🐳 Docker
- ☸️ Kubernetes
- 🏗️ Terraform
- 🔄 CI/CD
- 🐧 Linux
- 🔐 Cloud Security
- 🛡️ DevSecOps
- ⚙️ Infrastructure Automation

### 🐙 GitHub

👉 https://github.com/navnitkumar927

---

# 📄 License

This project is currently private and intended for:

- 📚 Development
- 🎓 Learning
- 💼 Portfolio
- 🧪 Demonstration
- ☁️ Cloud & DevOps experimentation

---

# 🥜 MR Makhana

### 🌰 Premium Makhana • ⚡ Next.js • 🐍 FastAPI • 🐘 PostgreSQL • ☁️ AWS • 🪣 S3 • 🔐 IAM

<p align="center">

**Built with ❤️ using modern web technologies, cloud infrastructure, and DevOps practices.**

</p>

<p align="center">

🥜 **MR MAKHANA** 🥜

</p>
