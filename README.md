# 🧪 API Testing Demo – JSONPlaceholder

Este proyecto es una práctica de **Testing de APIs REST** utilizando **Postman**.  
Se utiliza la API pública [JSONPlaceholder](https://jsonplaceholder.typicode.com/) para realizar pruebas sobre endpoints reales.

Incluye:

- Requests GET y POST  
- Validaciones automáticas con scripts de test  
- Uso de variables y environment  
- Evidencias en formato imagen  
- Exportación de colección y entorno  

---

## 📁 Contenido del repositorio
collection/
└── API-Demo-JSONPlaceholder.postman_collection.json

environment/
└── JSONPlaceholder-Dev.postman_environment.json

evidencias/
├── test_listar_posts.png
├── test_crear_post.png
├── test_actualizar_post.png (si querés agregar)
└── test_get_por_id_encadenado.png

---

## ▶️ Cómo usar este proyecto

### 1. Importar la colección
Postman → **Import** → Seleccionar archivo  
`API-Demo-JSONPlaceholder.postman_collection.json`

### 2. Importar el environment
Postman → **Import** →  
`JSONPlaceholder-Dev.postman_environment.json`

Activar el environment arriba a la derecha.

---

## ✔️ Requests incluidos

### 🔹 **GET – Listar posts**
Tests:
- Código 200  
- JSON válido  

---

### 🔹 **GET – Obtener post por ID**
Tests:
- Código 200  
- Propiedades `title` y `body` presentes  

---
### **POST – Crear post**

Body utilizado:

```json
{
    "title": "Post de prueba QA",
    "body": "Probando creación de posts con Postman",
    "userId": 1
}
```
### 🔹 GET – Obtener post usando ID almacenado
Flujo:
1. El request `POST /posts` crea un post y guarda el `id_creado` en el environment.
2. El request `GET /posts/{{id_creado}}` usa esa variable para consultar ese ID.

Tests:
- Status code 200 o 404 (según comportamiento de la API mock).
- La respuesta devuelve un body válido (aunque sea vacío).

### 🔹 PUT – Actualizar post
Tests:
- Código 200 0 204.
- Respuesta vacía o mínima ({}, " ")
---

### 🧪 Tests
- **201 Created**
- **Validación del título enviado**

---

### 📸 Evidencias
Las capturas reales de ejecución se encuentran en la carpeta **evidencias/**.

---

### 🎯 Objetivo
Este proyecto forma parte de mi formación como QA Tester, reforzando:

- Testing de APIs REST
- Lectura y validación de respuestas JSON
- Automatización de tests dentro de Postman
- Manejo de variables y environments
- Encadenamiento de requests
- Organización profesional de una colección de pruebas
