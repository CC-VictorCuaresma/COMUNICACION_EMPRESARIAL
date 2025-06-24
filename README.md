# 💧 Sistema JASS Digital – Plataforma de Gestión Comunitaria

## 📌 Descripción General

El **Sistema JASS Digital** es una solución desarrollada por estudiantes y docentes del CETPRO para mejorar la gestión del servicio de agua potable en comunidades rurales mediante una arquitectura basada en microservicios.

Este proyecto forma parte de una iniciativa de Responsabilidad Social (CSR) para promover la transformación digital en sectores con acceso limitado a la tecnología.

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

### 1. Clona el repositorio

```bash
git clone https://github.com/CC-VictorCuaresma/vg-jass-english.git
2. Ejecuta el backend (Spring Boot)
cd vg-jass-english/ms-distribucion
./mvnw spring-boot:run
Repite este paso para cada microservicio (ms-usuarios, ms-cajas, etc.)

3. Ejecuta el frontend (Angular)
https://github.com/vallegrande/MS-DISTRIBUCION-AGUA-fr-end
cd ../frontend
npm install
ng serve


🧩 Cómo usar el sistema (Consejos con "should")
You should abrir http://localhost:4200 luego de iniciar backend y frontend.
You should registrar un usuario desde la sede correspondiente.
You should asignar cajas a los usuarios antes de procesar pagos.
You should verificar la programación de distribución y notificar incidencias.

📁 Estructura del Repositorio
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

🔄 Colecciones y Relaciones (MongoDB)

📦 Microservicios y Colecciones
Microservicio	Colecciones principales
Organizaciones	organizaciones, sedes
Usuarios	usuarios
Cajas	cajas, asignacion_cajas
Pagos	pagos, facturas, reclamos
Distribución	zonas, calles, programacion_distribucion, tarifas, incidencias_distribucion
Notificaciones	notificaciones, plantillas

🔗 Relaciones Clave
organizaciones → sedes → usuarios

usuarios ↔ cajas (relación N:M)

usuarios → pagos → facturas

pagos → reclamos

sedes → zonas → calles

calles → programacion_distribucion

zonas → tarifas

calles → incidencias_distribucion

usuarios → notificaciones

🧑‍💻 Contribuir al Proyecto (Imperativos y Consejos)
Forkea este repositorio.

Crea una nueva rama:

git checkout -b feature/nombre-funcionalidad

Implementa, prueba y documenta tu código.

Haz un Pull Request detallado.

You should usar "Fixes #número" si resuelves un issue abierto.

🚀 Requisitos de Despliegue (Must & Need To)
You must configurar estas variables de entorno:

MONGO_USERNAME=sistemajass
MONGO_PASSWORD=*****
MONGO_DATABASE=JASS_DIGITAL
JWT_SECRET=clave_super_secreta
You need to habilitar CORS en la configuración de Spring Boot.

You must compilar el frontend antes de desplegar:

npm run build
Luego subir /dist/ al servicio de hosting (Firebase, Netlify, etc.)

💡 Buenas Prácticas
You should escribir pruebas unitarias (JUnit / Jasmine).

You should documentar nuevos endpoints en Swagger o /docs.

You should ejecutar:

mvn clean
npm run lint
antes de cada commit.

📚 Documentación Técnica
Diagrama de entidades: docs/entities.pdf
Swagger UI: http://localhost:8080/swagger-ui.html
Manual de usuario: docs/manual-usuario.pdf
Diagrama de despliegue: docs/infraestructura.png

👨‍🏫 Autores y Responsables
Módulo	Responsable
MS-Organizaciones	Milenka Muñoz
MS-Usuarios	Isael Fatama
MS-Cajas	Frank Salazar, Deyton Garcia, Santiago Prada
MS-Pagos	Johan Malasquez, Ronaldinho Ccencho
MS-Distribución	Equipo de distribución
MS-Notificaciones	Coordinador general

📞 Support and Help
Open an issue in this repository.
Tag your microservices manager.

Join the support group on Telegram or Discord for real-time assistance.

🙌 Acknowledgments
Thanks to everyone at Jass de Conta for their support of this project. 💙

✨ “Technology is useful when it improves people's lives.”
