# 🎫 Sistema de Boletería Electrónica

## 📝 Descripción del Proyecto
Este sistema es una solución de software escalable diseñada para mitigar problemas críticos de alta concurrencia, sobreventa y colisiones de transacciones durante la venta de entradas para eventos masivos (musicales y deportivos). El núcleo del sistema implementa un enfoque distribuido y asíncrono para gestionar picos masivos de tráfico de forma eficiente y ordenada.

---

## 👥 Integrantes del Equipo
- **Alexander Lopez** — Developer & DevOps
- **Marcelo Bacon** — Developer
- **Mateo Alba** — Developer
- **Heymi De la Cruz** — Developer
- **Pachar** — Developer

---

## 🏗️ Arquitectura y Tecnologías (AWS Serverless)
Para garantizar la alta disponibilidad y tolerancia a fallos, el backend está diseñado sobre el ecosistema serverless de **Amazon Web Services (AWS)**:

*   **Persistencia de Datos:** **AWS DynamoDB** para el almacenamiento de perfiles de usuario, credenciales y estados de los boletos.
*   **Procesamiento Asíncrono:** **AWS Lambda** para desacoplar el procesamiento de comentarios, reseñas y tareas secundarias sin degradar el core de ventas.
*   **Control de Concurrencia (Fila Virtual):** **AWS SQS FIFO** (First-In, First-Out) para encolar y procesar estrictamente las solicitudes en orden de llegada exacto, eliminando la sobreventa.
*   **Caché de Alto Rendimiento:** **AWS ElastiCache (Redis)** para la distribución inmediata del catálogo de eventos, reduciendo las lecturas directas a la base de datos.

---

## 📊 Tablero de Gestión (Agile / Kanban)
El desarrollo de las Historias de Usuario (HU) y el flujo de trabajo del equipo se gestiona activamente mediante un tablero Kanban en **GitHub Projects**, utilizando estimaciones basadas en la serie de Fibonacci (*Story Points*).