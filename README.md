# 🤖 Automatización de Reporterías (n8n)

## 🎯 Objetivo y Resumen

Diseñar e implementar un flujo de trabajo sin código (low-code) para la **automatización completa de un proceso de reportería repetitiva**. El objetivo fue reducir la intervención manual, minimizar errores de consolidación y optimizar el tiempo de entrega de resultados a stakeholders.

Este proyecto simula la eficiencia administrativa necesaria en sectores como la banca o el retail para tareas de reporte diario o semanal.

---

## 🛠️ Herramientas y Flujo del Proceso

El proyecto se centró en la integración de varias herramientas cloud mediante la plataforma de automatización n8n.

| Herramienta | Función en el Flujo |
| :--- | :--- |
| **n8n** | Motor principal para el diseño y ejecución del *workflow*. |
| **Google Drive/Sheets** | Lectura de datos de entrada (simulando boletas/facturas) y almacenamiento de reportes finales. |
| **Excel/CSV** | Procesamiento y generación del archivo de reporte consolidado. |
| **WhatsApp/Email** | Envío automatizado de los resultados a los destinatarios clave. |

### ⚙️ Diagrama Conceptual del Flujo
El flujo opera de forma secuencial:

1. **Trigger:** Evento programado o llegada de un nuevo archivo a Drive.
2. **Read & Process:** Lectura del archivo, extracción de datos clave (OCR o tabla).
3. **Transform:** Consolidación y aplicación de lógica de negocio (KPIs).
4. **Report Generation:** Creación del reporte en Excel/Google Sheets.
5. **Notification:** Envío del reporte final vía WhatsApp/Email al usuario final.

---

## ✨ Resultados Clave

### 1. Optimización Operativa
* **Reducción de Tiempos:** El tiempo operativo de generación y envío de reportes se redujo de **varias horas a menos de 10 minutos**.
* **Precisión:** **Eliminación de errores manuales** de consolidación y *copy-paste*, garantizando la integridad del dato entregado.

### 2. Escalabilidad
El flujo es fácilmente replicable y adaptable a otros procesos de reportería, mostrando un alto **ROI (Retorno de Inversión)** por la liberación de tiempo del personal.

## 📚 Estructura y Contenidos del Repositorio

| Archivo/Carpeta | Descripción |
| :--- | :--- |
| **`flujo_n8n.json`** | Exportación del *workflow* de n8n. Permite importar y ejecutar el flujo. |
| **`workflow_explicacion.md`** | Explicación detallada de cada nodo y la lógica implementada en el flujo. |
| **`screenshot_whatsapp.png`** | Captura de pantalla de la notificación final enviada. |
| **`reporte_ejemplo.xlsx`** | Ejemplo del formato de reporte generado automáticamente. |

---

## 💡 Lecciones Aprendidas

* **Manejo de Errores:** Se implementó una robusta gestión de errores dentro de n8n para notificar al administrador si el flujo fallaba al leer un archivo corrupto.
* **Seguridad de Datos:** El manejo de credenciales y *tokens* (APIs) se gestionó de forma segura, garantizando la confidencialidad de la información institucional.
