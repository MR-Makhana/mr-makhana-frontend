# 🥜 MR Makhana

### Premium Makhana E-Commerce Platform

MR Makhana is a modern full-stack e-commerce platform built for selling premium roasted Makhana products online.

The project combines a modern Next.js storefront with a FastAPI backend, PostgreSQL database, Amazon S3 image storage, and AWS infrastructure.

---

## ✨ Features

- 🛍️ Modern premium e-commerce storefront
- 📱 Responsive design for desktop, tablet, and mobile
- 📦 Product management
- 🗂️ Category management
- 💰 Product pricing and discount pricing
- 📊 Stock management
- ⭐ Featured products
- 🖼️ Product image management
- ☁️ Amazon S3 image storage
- 🗄️ PostgreSQL database
- 🚀 FastAPI REST API
- 📖 Automatic Swagger API documentation
- 🔐 AWS IAM role-based authentication
- 🌐 AWS EC2 backend deployment
- ⚡ Vercel frontend deployment
- 🔒 Environment-based configuration
- 🧩 Scalable application architecture

---

# 🏗️ Architecture

```text
                         ┌──────────────────┐
                         │     Customer     │
                         │    Web Browser   │
                         └────────┬─────────┘
                                  │
                                  ▼
                         ┌──────────────────┐
                         │ Next.js Frontend │
                         │     Vercel       │
                         └────────┬─────────┘
                                  │
                              REST API
                                  │
                                  ▼
                         ┌──────────────────┐
                         │ FastAPI Backend  │
                         │     AWS EC2      │
                         └────────┬─────────┘
                                  │
                    ┌─────────────┴─────────────┐
                    │                           │
                    ▼                           ▼
             ┌──────────────┐           ┌──────────────┐
             │  PostgreSQL  │           │  Amazon S3   │
             │   Database   │           │ Product Img. │
             └──────────────┘           └──────────────┘

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
- PostgreSQL
- Pydantic
- boto3
- python-multipart
Cloud & DevOps
- AWS EC2
- Amazon S3
- AWS IAM
- Git
- GitHub
- Vercel
📁 Project Structure
Frontend
mk-makhana/
│
├── app/
├── components/
│   └── ui/
├── lib/
├── public/
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
Products
Method	Endpoint	Description
GET	/api/products/	Get all products
POST	/api/products/	Create product
GET	/api/products/{product_id}	Get product
PUT	/api/products/{product_id}	Update product
DELETE	/api/products/{product_id}	Delete product


Categories
Method	Endpoint	Description
GET	/api/categories/	Get all categories
POST	/api/categories/	Create category
GET	/api/categories/{category_id}	Get category


Health
GET /health

Response:
{
  "status": "ok"
}

📖 API Documentation
FastAPI automatically provides interactive Swagger documentation.
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
🐍 Backend Setup
Clone the Repository
git clone https://github.com/navnitkumar927/mr-makhana-backend.git
cd mr-makhana-backend

Create Virtual Environment
python3 -m venv venv

Activate Virtual Environment
source venv/bin/activate

Install Dependencies
pip install -r requirements.txt

Start FastAPI
uvicorn app.main:app --host 0.0.0.0 --port 8000

Development mode:
uvicorn app.main:app --reload

🖥️ Frontend Setup
Clone Repository
git clone https://github.com/navnitkumar927/mk-makhana.git
cd mk-makhana

Install Dependencies
pnpm install

Start Development Server
pnpm dev

Frontend:
http://localhost:3000

🗄️ PostgreSQL
The backend uses PostgreSQL with SQLAlchemy.
Current database structure:
PostgreSQL
│
├── categories
│
└── products

Example environment configuration:
DATABASE_URL=postgresql+psycopg2://USERNAME:PASSWORD@localhost:5432/DATABASE

☁️ Amazon S3
Amazon S3 is used to store product images.
Example:
S3 Bucket
│
└── products/
    ├── image-1.jpg
    ├── image-2.jpg
    ├── image-3.png
    └── ...

The backend uses boto3 to upload and manage objects in S3.
Example configuration:
S3_BUCKET=YOUR_S3_BUCKET
AWS_REGION=us-east-1

🔐 AWS IAM Security
The backend runs on AWS EC2 and uses an IAM Role to access Amazon S3.
Example role:
MR-Makhana-EC2-S3-Role

Architecture:
FastAPI
   │
   ▼
boto3
   │
   ▼
EC2 IAM Role
   │
   ▼
Amazon S3

This avoids storing long-lived AWS access keys inside the application.
The application does NOT require:
AWS_ACCESS_KEY_ID
AWS_SECRET_ACCESS_KEY

to be hard-coded into the project.
🔒 Security Practices
The project follows these security practices:
- AWS IAM role-based authentication
- No hard-coded AWS credentials
- Environment variables for configuration
- .env excluded from Git
- Database credentials stored in environment variables
- S3 access controlled through IAM
- Pydantic request validation
- FastAPI HTTP exception handling
- Unique S3 object names
- Separation of application code and secrets
🖼️ Product Image Flow
User
 │
 ▼
Frontend
 │
 ▼
FastAPI Upload API
 │
 ▼
boto3
 │
 ▼
Amazon S3
 │
 ▼
Image URL
 │
 ▼
PostgreSQL
 │
 ▼
Product Record

The actual image file is stored in Amazon S3 while the database stores the corresponding image reference.
🧪 API Testing
Check backend health:
curl http://localhost:8000/health

Get products:
curl http://localhost:8000/api/products/

Get categories:
curl http://localhost:8000/api/categories/

Create a category:
curl -X POST http://localhost:8000/api/categories/ \
-H "Content-Type: application/json" \
-d '{
  "name": "Classic Makhana",
  "slug": "classic-makhana",
  "description": "Classic roasted makhana snacks.",
  "image_url": null,
  "is_active": true
}'

🚀 Deployment
The project is designed for cloud deployment using AWS and Vercel.
                   INTERNET
                       │
                       ▼
                ┌─────────────┐
                │   Vercel    │
                │   Next.js   │
                └──────┬──────┘
                       │
                       │ REST API
                       ▼
                ┌─────────────┐
                │   AWS EC2   │
                │   FastAPI   │
                └──────┬──────┘
                       │
              ┌────────┴────────┐
              │                 │
              ▼                 ▼
       ┌────────────┐    ┌────────────┐
       │ PostgreSQL │    │ Amazon S3  │
       │  Database  │    │   Images   │
       └────────────┘    └────────────┘

📊 Project Status
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
Orders	🔜
Payment Gateway	🔜
Admin Dashboard	🔜
CI/CD	🔜
Monitoring	🔜


🗺️ Roadmap
Phase 1 — Core Platform
- [x] Premium storefront
- [x] Product API
- [x] Category API
- [x] PostgreSQL integration
- [x] AWS EC2 deployment
- [x] S3 integration
- [x] IAM role configuration
Phase 2 — E-Commerce
- [ ] User authentication
- [ ] User accounts
- [ ] Shopping cart
- [ ] Wishlist
- [ ] Checkout
- [ ] Orders
- [ ] Payment gateway
- [ ] Order tracking
Phase 3 — Admin
- [ ] Admin authentication
- [ ] Admin dashboard
- [ ] Product management
- [ ] Category management
- [ ] Inventory management
- [ ] Order management
- [ ] Image management
Phase 4 — DevOps
- [ ] Docker
- [ ] GitHub Actions
- [ ] Automated CI/CD
- [ ] Security scanning
- [ ] Infrastructure as Code
- [ ] Application monitoring
- [ ] Centralized logging
- [ ] HTTPS
- [ ] Production domain
- [ ] Automated backups
🎯 Project Goals
MR Makhana is being developed as a production-oriented e-commerce platform with an emphasis on:
- Modern frontend engineering
- REST API development
- Cloud infrastructure
- AWS services
- Secure IAM architecture
- Object storage
- Database design
- DevOps automation
- Scalable application architecture
- Production deployment
👨‍💻 Author
Navnit Kumar
DevOps Engineer | Cloud & DevSecOps Enthusiast
GitHub:
https://github.com/navnitkumar927
🔗 Repositories
Frontend
https://github.com/navnitkumar927/mk-makhana
Backend
https://github.com/navnitkumar927/mr-makhana-backend
📄 License
This project is currently private and intended for development, learning, portfolio, and demonstration purposes.
🥜 MR Makhana
Premium Makhana • Next.js • FastAPI • PostgreSQL • AWS EC2 • Amazon S3 • IAM • Cloud Architecture
