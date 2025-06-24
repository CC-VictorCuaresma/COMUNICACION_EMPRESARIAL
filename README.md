# 💧 JASS Digital System – Community Management Platform

## 📌 General Description

The **JASS Digital System** is a solution developed by CETPRO students and faculty to improve the management of drinking water services in rural communities using a microservices-based architecture.

This project is part of a Corporate Social Responsibility (CSR) initiative to promote digital transformation in sectors with limited access to technology.

---

## 🔧 Tech Stack

- **Backend:** Java 17 (Spring Boot, IntelliJ IDEA)
- **Frontend:** Angular (última versión estable)
- **Base de datos:** MongoDB (MongoDB Atlas)
- **APIs:** OpenAPI / Swagger

---

## ✅ Project Objective

- Modernize the administration of water boards (JASS).
- Digitize processes: users, cash registers, payments, distribution, and incidents.
- Facilitate automated notifications for better communication with users.
- Empower local operators with current technical tools.
---

## 🛠️ Instrucciones de Instalación (Imperativas)

### 1. Clona el repositorio del Backend

```bash
git clone https://github.com/CC-VictorCuaresma/vg-jass-english.git

cd vg-jass-english/ms-distribucion

./mvnw spring-boot:run

Repeat this step for each microservice (ms-users, ms-boxes, etc.)
```
### 1. Clona el repositorio del FrontEnd
```bash
git clone https://github.com/vallegrande/MS-DISTRIBUCION-AGUA-fr-end

cd ../frontend

npm install

ng serve
```

## 🧩 How to Use the System (Tips with "should")

- You should open http://localhost:4200 after starting the backend and frontend.
- You should register a user from the corresponding location.
- You should assign registers to users before processing payments.
- You should check the distribution schedule and report issues.


## 📁 Estructura del Repositorio

```text
vg-jass-english/
├── ms-organizaciones/    # Gestión de organizaciones y sedes
├── ms-usuarios/          # Gestión de usuarios del sistema
├── ms-cajas/             # Asignación y registro de cajas
├── ms-pagos/             # Pagos, facturación y reclamos
├── ms-distribucion/      # Distribución del recurso y programación
├── ms-notificaciones/    # Notificaciones automáticas (SMS/email)
├── frontend/             # Aplicación Angular
├── docs/                 # Diagramas, modelos y documentación
├── .env.example          # Plantilla de variables de entorno
└── README.md             # ← Este archivo
```

## 🔄 Colecciones y Relaciones (MongoDB)

📦 Microservices and Collections:
- Main Collections Microservice
- Organizations, locations
- Users
- Boxes, boxes, box assignment
- Payments, invoices, complaints
- Distribution of zones, streets, distribution scheduling, rates, distribution incidents
- Notifications, templates


## 🔗 Key Relationships
```text
Organizations → Locations → Users

Users ↔ Cashiers (N:M relationship)

Users → Payments → Invoices

Payments → Claims

Locations → Zones → Streets

Streets → Distribution_Scheduling

Zones → Rates

Streets → Distribution_Incidents

Users → Notifications
```

## 🧑‍💻 Contribute to the Project (Imperatives and Advice)
Fork this repository.

- Create a new branch:
```bash
git checkout -b feature/feature-name
```
- Deploy, test, and document your code.

Make a detailed Pull Request.

You should use "Fixes #number" if you are resolving an open issue.

## 🚀 Deployment Requirements (Must & Need To)
You must configure these environment variables:
```text
MONGO_USERNAME=JASS_System

MONGO_PASSWORD=*****

MONGO_DATABASE=JASS_DIGITAL

JWT_SECRET=Super_Secret_Key
```
You need to enable CORS in your Spring Boot configuration.

You must compile the frontend before deploying:

npm run build


## 💡 Best Practices
You should write unit tests (JUnit / Jasmine).

You should document new endpoints in Swagger or /docs.

You should run:
-------------------------------------------------
- mvn clean
- npm run lint

## 📚 Documentación Técnica
Diagrama de entidades: docs/entities.pdf

Swagger UI: http://localhost:8080/swagger-ui.html

Manual de usuario: docs/manual-usuario.pdf

Diagrama de despliegue: docs/infraestructura.png

## 👨‍🏫 Autores y Responsables
```text
Módulo	-  Responsable
MS-Organizaciones :	Milenka Muñoz
MS-Usuarios	: Isael Fatama
MS-Cajas :	Frank Salazar, Deyton Garcia, Santiago Prada
MS-Pagos	: Johan Malasquez, Ronaldinho Ccencho
MS-Distribución :	Equipo de distribución
MS-Notificaciones :	Coordinador general
```

## 📞 Support and Help
Open an issue in this repository.
Tag your microservices manager.

Join the support group on Telegram or Discord for real-time assistance.

## 🙌 Acknowledgments
Thanks to everyone at Jass de Conta for their support of this project. 💙

✨ “Technology is useful when it improves people's lives.”
