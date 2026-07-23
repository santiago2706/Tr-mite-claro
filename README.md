# 🏛️ Trámite Claro — AI Backend & RAG Pipeline

**Trámite Claro** es un backend distribuido de alto rendimiento diseñado para automatizar, consultar e interpretar trámites y documentación administrativa pública mediante técnicas avanzadas de **RAG (Retrieval-Augmented Generation)** e **Inteligencia Artificial**.

---

## 🎯 Objetivo del Proyecto

Facilitar la búsqueda e interacción con procedimientos administrativos oficiales mediante un sistema capaz de:
1. Extraer y procesar documentos oficiales de manera automatizada.
2. Indexar y vectorizar información estructurada y no estructurada.
3. Responder consultas ciudadanas con exactitud y fuentes citadas mediante LLMs.

---

## 🏗️ Arquitectura y Tecnologías

El proyecto sigue una **Arquitectura por Capas (Clean Architecture / Service-Repository Pattern)** priorizando el desacoplamiento, la escalabilidad y el rendimiento.

* **Lenguaje:** Python 3.12+
* **Gestor de Paquetes & Entorno:** `uv`
* **Framework Web:** FastAPI (ASGI)
* **Servidor HTTP:** Uvicorn
* **Web Crawler & Scraper:** Playwright (Headless Browser)
* **Validación de Datos:** Pydantic v2
* **Base de Datos Vectorial:** *(pgvector / Qdrant)*
* **ORM:** SQLAlchemy v2
* **Frontend:** Next.js *(Fase futura)*

---

## 📂 Estructura del Proyecto

```text
backend/
├── app/
│   ├── api/          # Endpoints HTTP y rutas REST
│   ├── core/         # Configuración global, seguridad y logs
│   ├── crawler/      # Automatización de scraping y descargas (Playwright)
│   ├── db/           # Conexiones, sesión de base de datos y migraciones
│   ├── models/       # Entidades SQLAlchemy (ORM)
│   ├── repositories/ # Capa de acceso a datos (Queries)
│   ├── schemas/      # Modelos Pydantic para validación de DTOs
│   ├── services/     # Lógica de negocio (RAG, procesamiento, etc.)
│   └── main.py       # Punto de entrada de la aplicación FastAPI
├── tests/            # Pruebas unitarias e integración
├── pyproject.toml    # Configuración central del proyecto y dependencias
└── README.md
