# 🥜 MR Makhana

## Premium Makhana E-Commerce Platform

MR Makhana is a modern full-stack e-commerce platform designed for selling premium roasted Makhana products online.

The project combines a modern **Next.js storefront**, **FastAPI REST API**, **PostgreSQL database**, **Amazon S3 object storage**, **AWS EC2 infrastructure**, and **AWS IAM role-based security**.

The application is being developed with a production-oriented architecture focused on scalability, security, cloud infrastructure, and DevOps practices.

---

## 🚀 Project Overview

MR Makhana consists of two primary applications:

| Component | Technology |
|---|---|
| Frontend | Next.js |
| UI | React + TypeScript |
| Styling | Tailwind CSS |
| UI Components | shadcn/ui |
| Animations | Framer Motion |
| Backend | FastAPI |
| Language | Python |
| ORM | SQLAlchemy |
| Validation | Pydantic |
| Database | PostgreSQL |
| Object Storage | Amazon S3 |
| AWS SDK | boto3 |
| Backend Hosting | AWS EC2 |
| Frontend Hosting | Vercel |
| Cloud Authentication | AWS IAM Role |
| API Documentation | Swagger / OpenAPI |

---

# ✨ Features

## 🛍️ E-Commerce Storefront

- Premium modern storefront
- Responsive design
- Desktop, tablet, and mobile support
- Product listing
- Product categories
- Featured products
- Product pricing
- Compare-at / discount pricing
- Stock quantity management
- Product image support
- Premium animations
- Modern UI components
- Mobile-friendly navigation

---

## ⚙️ Backend Features

- FastAPI REST API
- Product CRUD operations
- Category management
- PostgreSQL database integration
- SQLAlchemy ORM
- Pydantic request validation
- Automatic Swagger documentation
- OpenAPI specification
- Health check endpoint
- Environment-based configuration
- Amazon S3 integration
- Product image upload service
- Unique S3 object naming
- HTTP error handling
- Database relationship support

---

## ☁️ AWS Features

- AWS EC2 backend deployment
- Amazon S3 product image storage
- AWS IAM role-based authentication
- boto3 AWS SDK integration
- Secure EC2-to-S3 communication
- No hard-coded AWS access keys
- S3 bucket-based object storage
- Cloud-ready application architecture

---

# 🏗️ System Architecture

```text
                         ┌─────────────────────┐
                         │      Customer       │
                         │     Web Browser     │
                         └──────────┬──────────┘
                                    │
                                    ▼
                         ┌─────────────────────┐
                         │   Next.js Frontend  │
                         │       Vercel        │
                         └──────────┬──────────┘
                                    │
                              HTTPS / REST API
                                    │
                                    ▼
                         ┌─────────────────────┐
                         │   FastAPI Backend   │
                         │       AWS EC2       │
                         └──────────┬──────────┘
                                    │
                    ┌───────────────┴───────────────┐
                    │                               │
                    ▼                               ▼
          ┌──────────────────┐            ┌──────────────────┐
          │    PostgreSQL    │            │    Amazon S3     │
          │     Database     │            │  Product Images  │
          └──────────────────┘            └──────────────────┘
                                                    ▲
                                                    │
                                                 boto3
                                                    │
                                                    │
                                          ┌──────────────────┐
                                          │    AWS IAM Role  │
                                          │  EC2 Permissions │
                                          └──────────────────┘
🔄 Product Image Architecture
Product images are stored in Amazon S3 instead of storing the actual image files directly inside the application server.
                    Customer / Admin
                           │
                           ▼
                  ┌─────────────────┐
                  │ Next.js Frontend│
                  └────────┬────────┘
                           │
                           ▼
                  ┌─────────────────┐
                  │ FastAPI Backend │
                  └────────┬────────┘
                           │
                           ▼
                        boto3
                           │
                           ▼
                  ┌─────────────────┐
                  │   Amazon S3     │
                  │                 │
                  │    products/    │
                  │      image.jpg  │
                  └────────┬────────┘
                           │
                           ▼
                      Image URL
                           │
                           ▼
                    PostgreSQL
                    Product Record

The image file is stored in S3, while the corresponding image URL/reference is stored with the product data.
🔐 AWS IAM Security
The backend uses an EC2 IAM Role to access AWS services.
Example role:
MR-Makhana-EC2-S3-Role

The EC2 instance receives temporary AWS credentials automatically through the attached IAM role.
FastAPI
   │
   ▼
 boto3
   │
   ▼
EC2 Instance
   │
   ▼
IAM Role
   │
   ▼
Amazon S3

This approach avoids storing long-lived AWS access keys inside the application.
The project does not require hard-coded:
AWS_ACCESS_KEY_ID
AWS_SECRET_ACCESS_KEY

The application can use the AWS credentials provided automatically to the EC2 instance through its IAM role.
🛡️ Security Practices
The project follows several security-focused practices:
- IAM role-based AWS authentication
- No hard-coded AWS credentials
- Environment variables for configuration
- .env excluded from Git
- Database credentials stored outside source code
- S3 permissions controlled through IAM
- Pydantic request validation
- FastAPI HTTP exception handling
- Unique S3 object names
- Separation of application code and secrets
- AWS least-privilege permissions where applicable
🛠️ Tech Stack
Frontend
- Next.js
- React
- TypeScript
- Tailwind CSS
- shadcn/ui
- Framer Motion
- Vercel
Backend
- Python
- FastAPI
- Uvicorn
- SQLAlchemy
- Pydantic
- boto3
- python-multipart
Database
- PostgreSQL
Cloud & Infrastructure
- AWS EC2
- Amazon S3
- AWS IAM
- Vercel
Development & Version Control
- Git
- GitHub
- pnpm
- Python Virtual Environment
📁 Project Structure
Frontend
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

Backend
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

🔌 REST API
Products API
Method	Endpoint	Description
GET	/api/products/	Get all products
POST	/api/products/	Create product
GET	/api/products/{product_id}	Get product
PUT	/api/products/{product_id}	Update product
DELETE	/api/products/{product_id}	Delete product


Categories API
Method	Endpoint	Description
GET	/api/categories/	Get all categories
POST	/api/categories/	Create category
GET	/api/categories/{category_id}	Get category


Health API
GET /health

Response:
{
  "status": "ok"
}

📖 API Documentation
FastAPI automatically generates interactive API documentation.
Swagger UI:
http://YOUR_SERVER_IP:8000/docs

OpenAPI specification:
http://YOUR_SERVER_IP:8000/openapi.json

Swagger allows developers to test:
- GET requests
- POST requests
- PUT requests
- DELETE requests
- Request validation
- API responses
- HTTP status codes
🐍 Backend Setup
1. Clone the Backend Repository
git clone https://github.com/navnitkumar927/mr-makhana-backend.git

cd mr-makhana-backend

2. Create Virtual Environment
python3 -m venv venv

3. Activate Virtual Environment
Linux / macOS:
source venv/bin/activate

4. Install Dependencies
pip install -r requirements.txt

5. Configure Environment Variables
Create:
.env

Example:
DATABASE_URL=postgresql+psycopg2://USERNAME:PASSWORD@HOST:5432/DATABASE

S3_BUCKET=YOUR_S3_BUCKET
AWS_REGION=us-east-1

Never commit .env to GitHub.

6. Start FastAPI
uvicorn app.main:app --host 0.0.0.0 --port 8000

Development mode:
uvicorn app.main:app --reload

Backend:
http://localhost:8000

Swagger:
http://localhost:8000/docs

🖥️ Frontend Setup
1. Clone Repository
git clone https://github.com/navnitkumar927/mk-makhana.git

2. Enter Project
cd mk-makhana

3. Install Dependencies
pnpm install

4. Start Development Server
pnpm dev

Frontend:
http://localhost:3000

🗄️ PostgreSQL
The backend uses PostgreSQL as the primary relational database.
The application contains database models for:
PostgreSQL
│
├── categories
│
└── products

Example database configuration:
DATABASE_URL=postgresql+psycopg2://USERNAME:PASSWORD@HOST:5432/DATABASE

SQLAlchemy is used as the ORM layer between FastAPI and PostgreSQL.
☁️ Amazon S3
Amazon S3 is used for product image storage.
Example bucket structure:
mr-makhana-product-images
│
└── products/
    │
    ├── image-1.jpg
    ├── image-2.jpg
    ├── image-3.png
    └── image-4.webp

The backend uses boto3 to communicate with S3.
Example configuration:
S3_BUCKET=YOUR_S3_BUCKET
AWS_REGION=us-east-1

🧪 S3 Connection Test
Verify AWS identity:
aws sts get-caller-identity

Test the S3 bucket:
aws s3 ls s3://YOUR_S3_BUCKET

Test the product image directory:
aws s3 ls s3://YOUR_S3_BUCKET/products/

🧪 Backend Testing
Health Check
curl http://localhost:8000/health

Expected response:
{
  "status": "ok"
}

Get Products
curl http://localhost:8000/api/products/

Get Categories
curl http://localhost:8000/api/categories/

Create Category
curl -X POST http://localhost:8000/api/categories/ \
-H "Content-Type: application/json" \
-d '{
  "name": "Classic Makhana",
  "slug": "classic-makhana",
  "description": "Classic roasted makhana snacks.",
  "image_url": null,
  "is_active": true
}'

📦 Example Product
Example product payload:
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

🚀 Deployment Architecture
The project is designed for cloud deployment using Vercel and AWS.
                         INTERNET
                             │
                             ▼
                    ┌────────────────┐
                    │     Vercel     │
                    │   Next.js App  │
                    └───────┬────────┘
                            │
                         REST API
                            │
                            ▼
                    ┌────────────────┐
                    │    AWS EC2     │
                    │ FastAPI/Uvicorn│
                    └───────┬────────┘
                            │
                  ┌─────────┴─────────┐
                  │                   │
                  ▼                   ▼
          ┌──────────────┐    ┌──────────────┐
          │  PostgreSQL  │    │  Amazon S3   │
          │   Database   │    │ Product Image│
          └──────────────┘    └──────────────┘

📊 Current Project Status
Component	Status
Premium Storefront	✅
Responsive UI	✅
Next.js Frontend	✅
FastAPI Backend	✅
Product API	✅
Category API	✅
PostgreSQL	✅
SQLAlchemy	✅
Swagger Documentation	✅
AWS EC2	✅
AWS IAM Role	✅
Amazon S3	✅
boto3 Integration	✅
S3 Upload Service	✅
Product Image Upload API	🚧
Frontend API Integration	🚧
Authentication	🔜
Shopping Cart	🔜
Wishlist	🔜
Orders	🔜
Payment Gateway	🔜
Admin Dashboard	🔜
CI/CD	🔜
Monitoring	🔜


🗺️ Roadmap
Phase 1 — Core Platform
- [x] Premium storefront
- [x] Responsive frontend
- [x] Product API
- [x] Category API
- [x] PostgreSQL integration
- [x] SQLAlchemy integration
- [x] AWS EC2 deployment
- [x] Amazon S3 integration
- [x] IAM role configuration
- [x] S3 upload service
Phase 2 — E-Commerce
- [ ] User authentication
- [ ] User accounts
- [ ] Shopping cart
- [ ] Wishlist
- [ ] Checkout
- [ ] Orders
- [ ] Payment gateway
- [ ] Order tracking
- [ ] Email notifications
Phase 3 — Admin Platform
- [ ] Admin authentication
- [ ] Admin dashboard
- [ ] Product management
- [ ] Category management
- [ ] Inventory management
- [ ] Order management
- [ ] Product image management
- [ ] Analytics dashboard
Phase 4 — DevOps & Production
- [ ] Docker
- [ ] Docker Compose
- [ ] GitHub Actions
- [ ] Automated CI/CD
- [ ] Security scanning
- [ ] Infrastructure as Code
- [ ] Application monitoring
- [ ] Centralized logging
- [ ] HTTPS
- [ ] Production domain
- [ ] Automated backups
- [ ] CloudWatch monitoring
🎯 Project Goals
MR Makhana is being developed as a production-oriented e-commerce platform with a strong focus on:
- Modern frontend development
- REST API architecture
- Cloud infrastructure
- AWS services
- Secure IAM architecture
- Object storage
- Database design
- API development
- DevOps automation
- Secure deployments
- Scalable architecture
- Production-ready engineering
🔒 Environment Variables
Example backend .env:
DATABASE_URL=postgresql+psycopg2://USERNAME:PASSWORD@HOST:5432/DATABASE

S3_BUCKET=YOUR_S3_BUCKET
AWS_REGION=us-east-1

The .env file should remain local and must not be committed to GitHub.
Recommended .gitignore entries:
.env
.venv/
venv/
__pycache__/
*.pyc

🧹 Useful Backend Commands
Activate environment:
source venv/bin/activate

Check Python:
python --version

Check installed packages:
pip freeze

Compile Python files:
python -m py_compile app/main.py

Start server:
uvicorn app.main:app --host 0.0.0.0 --port 8000

Check running Uvicorn process:
ps aux | grep uvicorn

Check API:
curl http://localhost:8000/health

🌐 Repository
Frontend
https://github.com/navnitkumar927/mk-makhana
Backend
https://github.com/navnitkumar927/mr-makhana-backend
👨‍💻 Author
Navnit Kumar
DevOps Engineer | Cloud & DevSecOps Enthusiast
Focused on:
- AWS
- Docker
- Kubernetes
- Terraform
- CI/CD
- Linux
- Cloud Security
- DevSecOps
- Infrastructure Automation
GitHub:
https://github.com/navnitkumar927
📄 License
This project is currently private and intended for development, learning, portfolio, and demonstration purposes.
🥜 MR Makhana
Premium Makhana • Next.js • FastAPI • PostgreSQL • AWS EC2 • Amazon S3 • IAM
Built with modern web technologies and cloud infrastructure.

**Bas itna hi:** GitHub repo → `README.md` → Edit → purana content delete → **upar wala pura content paste → Commit changes**.
