# 📄 Report Service – School Vaccination Portal

This microservice is responsible for generating, filtering, paginating, and exporting student vaccination reports in various formats (CSV, PDF, XLS) as part of the **School Vaccination Portal**.

---

## 🚀 Features

- 📋 List and filter reports by vaccine name and date
- 📦 Paginated report listings
- 📁 Export reports in CSV, PDF, or XLS format
- 🔁 Integrates with `student-service` and `drive-service` via HTTP

---

## 🛠️ Tech Stack

- **Node.js** + **Express.js**
- **MongoDB** (optional, for caching)
- **Docker** + `docker-compose`
- File generation via `json2csv`, `exceljs`, or `pdfkit` (based on export format)

---

## 📦 API Endpoints

| Method | Endpoint               | Description                        |
|--------|------------------------|------------------------------------|
| GET    | `/reports`             | Filtered list of vaccination reports |
| GET    | `/reports/paginated`   | Paginated reports listing          |
| GET    | `/reports/export`      | Export reports in CSV/PDF/XLS      |

---

## 🐳 Docker Setup

```bash
# Build and start the container
docker-compose up --build
```

Make sure your `MONGO_URI` is set properly in the `.env` file:

```env
MONGO_URI=mongodb://mongo-report:27017/report-db
```

---

## 📁 Project Structure

```
report-service/
├── controllers/     # Business logic
├── routes/          # API routes
├── exports/         # File export utilities
├── index.js         # Entry point
├── Dockerfile
├── .env
└── package.json


