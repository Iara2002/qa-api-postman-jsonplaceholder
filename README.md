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
API-Demo-JSONPlaceholder.postman_collection.json

environment/
JSONPlaceholder-Dev.postman_environment.json

evidencias/
test_listar_posts.png
test_crear_post.png

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

### 🔹 **POST – Crear post**
Body utilizado:

```json
{
  "title": "Post de prueba QA",
  "body": "Probando creación de posts con Postman",
  "userId": 1
}

----
##  Tests:
- 201 Created
- Validación del título enviado

📸 Evidencias
Las capturas reales de ejecución se encuentran en la carpeta evidencias/

🎯 Objetivo

Este proyecto forma parte de mi formación como QA Tester, reforzando:
- Pruebas sobre APIs REST
- Lectura e interpretación de respuestas JSON
- Automatización básica de validaciones
- Manejo de environments y variables
- Organización y estructuración profesional de colecciones

