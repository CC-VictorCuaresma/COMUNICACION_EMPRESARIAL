# 💧 Sistema JASS Digital – Microservicios Distribuidos

## 🔧 Tech Stack

- **Backend:** Java 17 (Spring Boot, IntelliJ IDEA)
- **Frontend:** Angular (última versión estable)
- **Database:** MongoDB (Atlas)
- **API Docs:** Postman / Swagger

---

## ✅ Project Purpose

Este sistema JASS (Juntas Administradoras de Servicios de Saneamiento) digitaliza la gestión de agua potable en comunidades rurales. Permite gestionar usuarios, pagos, distribución, incidencias y notificaciones de forma eficiente y transparente, usando tecnologías modernas basadas en microservicios.

---

## 🛠️ Setup Instructions (Imperatives)

### 📦 Clona el repositorio:

```bash
git clone https://github.com/CC-VictorCuaresma/vg-jass-english.git
⚙️ Backend (Spring Boot)
cd vg-jass-english/distribution-microservice
./mvnw spring-boot:run
🌐 Frontend (Angular)
cd ../frontend
npm install
ng serve


🧩 How to Use the App (Advice with “should”)
You should open http://localhost:4200 after both backend and frontend are running.

You should register a user to access the system.

You should assign boxes to users before processing payments.

You should monitor distribution and submit reports for incidents.


🎯 Future Plans (Suggestions)
We should enable Firebase Authentication for better security.

We should integrate dashboards for payment and usage metrics.

We should schedule training sessions for JASS operators each quarter.

We should optimize performance with Redis caching in key services.


📁 Repository Structure
vg-jass-english/
├── backend/
│   ├── ms-organizaciones/
│   ├── ms-usuarios/
│   ├── ms-cajas/
│   ├── ms-pagos/
│   ├── ms-distribucion/
│   └── ms-notificaciones/
├── frontend/               # Angular SPA
├── docs/                   # Architecture, diagrams, DB schemas
├── README.md               # ← You are here
└── .env.example            # Env config example
🧑‍🏫 Contributing (Imperatives & Advice)
Fork this repository.

Create a new feature branch:

git checkout -b feature/nueva-funcionalidad
Implement and test locally.

Open a Pull Request with clear explanation.

You should include "Fixes #<issue>" if it resolves a ticket.

🚀 Deployment Requirements (Must & Need To)
You must configure MongoDB Atlas URI:

ini

MONGO_USERNAME=sistemajass
MONGO_PASSWORD=...
MONGO_DATABASE=JASS_DIGITAL
You need to enable CORS in Spring Boot config.

You must build the Angular frontend before deploy:

npm run build
Upload /dist/ to your hosting service (Firebase, Netlify, etc.)

💡 Best Practices & Tips
You should follow clean architecture principles.

You should document new endpoints in Swagger.

You should run:

mvn clean
npm run lint
before each commit.

You should version control the docs/ folder for all diagrams and schemas.

🔗 Microservices Overview
Microservice	Collections
MS-Organizaciones	organizaciones, sedes
MS-Usuarios	usuarios
MS-Cajas	cajas, asignacion_cajas
MS-Pagos	pagos, facturas, reclamos
MS-Distribución	zonas, calles, programacion_distribucion, tarifas, incidencias_distribucion
MS-Notificaciones	notificaciones, plantillas

🔄 Relationships Summary
organizaciones → sedes → usuarios → cajas, pagos, notificaciones

zonas → calles, tarifas, programacion_distribucion

pagos → facturas, reclamos

calles ↔ incidencias_distribucion

📞 Questions & Support
If you need help:

Open an Issue in this repository

Tag the microservice owner in the issue (e.g., @milenka-muñoz for MS-Organizaciones)

Join our Discord group for live tech support

✨ Let’s transform local water management with tech.
✊ Built with purpose, by CETPRO students and professionals.
