# 💄 Shop Cosmetic

A secure e-commerce web application for cosmetic products, built with a classic Servlet/JSP MVC architecture and a JWT-authenticated backend. Developed as a group project, with the backend fully implemented by this repo's main contributor.

---

## ✨ Features

- **Product Browsing & Search** — categorization and advanced search/filtering by category, brand, price range, and keyword
- **Shopping Cart & Orders** — add / edit / remove items in cart, place orders, and track order status
- **Authentication & Security** — JWT-based token authentication, HTTPS/TLS-secured client-server communication
- **Notifications** — automated order confirmation and promotional emails via the Gmail API
- **Admin Dashboard** — sales statistics, product management, and user/order processing
- **Multi-role Management** — separate workflows for regular users and administrators

---

## 🏗️ Architecture

Built as an **MVC-based** application with secure backend workflows:

```
┌─────────────────────────┐
│   Frontend (Bootstrap)  │  Responsive UI
└───────────┬─────────────┘
            │  HTTPS / TLS
┌───────────▼─────────────┐
│   Backend (Servlet/JSP) │
│   - Auth (JWT)          │
│   - Cart & Order Logic  │
│   - Product Search      │
│   - Admin Dashboard     │
└───────────┬─────────────┘
            │  JPA (ORM)
┌───────────▼─────────────┐
│        Database           │
└───────────────────────────┘
            │
┌───────────▼───────────────┐
│ Gmail API (Notifications) │
└───────────────────────────┘
```

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| Backend | Java, Servlet, JSP |
| Frontend | Bootstrap |
| ORM / Data Access | JPA |
| Authentication | JWT |
| Security | HTTPS / TLS |
| Notifications | Gmail API |

---

## 🚀 Getting Started

```bash
# Clone the repository
git clone https://github.com/<your-username>/shop-cosmetic.git
cd shop-cosmetic

# Build and run (Maven-based Servlet/JSP project)
mvn clean install
```

Deploy the generated WAR file to a servlet container (e.g. Apache Tomcat) and visit `https://localhost:<port>` to access the application.

---

## 🔑 Environment Variables

Set the following before running the project. **Never commit real secrets to the repository:**

```properties
# Database
DB_URL=
DB_USERNAME=
DB_PASSWORD=

# JWT
JWT_SECRET_KEY=

# Gmail API / SMTP
MAIL_USERNAME=
MAIL_PASSWORD=

# SSL / TLS
SSL_KEYSTORE_PATH=
SSL_KEYSTORE_PASSWORD=
```

---
