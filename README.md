
```markdown
# Inventory Shop

A full-stack web application for shop management with a customer storefront and admin panel.  
Built with Angular 17 (frontend) and Django REST Framework (backend).

---

## Team

| Name | Role |
|------|------|
| Abdrakhman Diana | Backend Developer |
| Khanshaiym Kaldybay | Frontend Developer |
| Aiym Buyesheva | Database Developer |

---

## About

Inventory Shop provides two interfaces:
- **Customer storefront** — product catalog, cart, order placement, order tracking
- **Admin panel** — product and order management, analytics, audit log

---

## Tech Stack

**Frontend**
- Angular 17, TypeScript, SCSS
- Chart.js, RxJS, Angular Router

**Backend**
- Django 4, Django REST Framework
- Token Authentication
- PostgreSQL
- django-cors-headers

---

## Project Structure

```
Web-project-main/
├── frontend/               # Angular application
│   └── src/app/
│       ├── core/           # services, guards, interceptors
│       ├── shared/         # reusable components, interfaces
│       ├── admin/          # dashboard, products, orders, audit
│       ├── shop/           # catalog, cart, product, track
│       └── app.routes.ts
├── backend/                # Django backend
│   ├── api/                # models, views, serializers, urls
│   ├── config/             # settings, root urls
│   └── manage.py
└── README.md
```

---

## Setup

**Backend**
```bash
cd backend
python -m venv venv
venv\Scripts\activate
pip install -r requirements.txt
python manage.py migrate
python manage.py createsuperuser
python manage.py runserver
```

**Frontend**
```bash
cd frontend
npm install
ng serve
```

| URL | Description |
|-----|-------------|
| http://localhost:4200 | Customer storefront |
| http://localhost:4200/login | Admin login |
| http://localhost:8000/api/ | Backend API |

---

## API Endpoints

**Auth**
```
POST   /api/auth/login/
POST   /api/auth/logout/
```

**Products**
```
GET    /api/products/
POST   /api/products/
GET    /api/products/{id}/
PATCH  /api/products/{id}/
DELETE /api/products/{id}/
POST   /api/products/{id}/rate/
GET    /api/products/{id}/recommendations/
```

**Orders**
```
GET    /api/orders/
POST   /api/orders/
PATCH  /api/orders/{id}/
GET    /api/orders/track/{code}/
GET    /api/orders/export/
```

**Categories**
```
GET    /api/categories/
POST   /api/categories/
```

**Stats**
```
GET    /api/stats/
GET    /api/stats/chart/
GET    /api/audit-logs/
```

---

## Requirements Coverage

**Frontend (Angular)**
- Interfaces and services for all API communication
- 4+ click events triggering API requests
- 4+ form controls using [(ngModel)]
- Component styling with SCSS
- Routing module with 8 named routes
- *ngFor and *ngIf for data rendering
- Token authentication with HTTP interceptor
- Centralized Angular Services using HttpClient
- API error handling with user-facing messages

**Backend (Django)**
- 6 models: Category, Product, Order, OrderItem, ProductRating, AuditLog
- 5+ ForeignKey relationships
- LoginSerializer and StatsSerializer (Serializer)
- ProductSerializer and OrderSerializer (ModelSerializer)
- 8 Function-Based Views
- 6 Class-Based Views
- Token login and logout endpoints
- Full CRUD for Product and Order models
- Objects linked to authenticated user via request.user
- CORS configured for Angular dev server

---

*KBTU — Web Development Project, 2026*
```

