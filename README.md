# pooparcial2
# POO - PostMail
# 📦 API POSTMAIL - Gestión de Envíos con Créditos ✈️📬

Este proyecto es una API REST hecha con **Node.js + Express + MongoDB** que permite a los usuarios:

* Comprar créditos
* Registrar envíos
* Eliminar envíos (con reembolso de créditos)
* Ver sus envíos y créditos disponibles
* Consultar productos disponibles

---

## 🤖 Tecnologías usadas

* Node.js
* Express
* MongoDB + Mongoose
* Postman para pruebas (opcional)

---

## Cómo ejecutar el proyecto

### 1. Clonar el repositorio

```bash
git clone https://github.com/JosueEnrique/pooparcial2
cd postmail-api
```

### 2. Instalar dependencias

```bash
npm install
```

### 3. Crear archivo `.env`

Configúralo así:

```
MONGODB_URI=mongodb://localhost:27017/postmail
PORT=3000
```


### 4. Iniciar el servidor

```bash
npm start
```

> El servidor corre en: `http://localhost:3000`

---

## 🥪 Endpoints disponibles

### 👤 Usuarios

* `GET /usuario/:id/credito`
  Muestra los créditos de un usuario

* `POST /usuario/:id/comprar-creditos`
  Compra créditos (paquetes válidos: `30`, `40`, `60`)

  **Body JSON:**

  ```json
  { "paquete": "30" }
  ```

---

###  ✉️ Envíos

* `POST /envios`
  Registra un nuevo envío

  **Body JSON:**

  ```json
  {
    "usuarioId": "123",
    "producto": "id"
  }
  ```

* `GET /envios/:usuarioId`
  Muestra todos los envíos de un usuario

* `DELETE /envios/:envioId`
  Elimina un envío y reembolsa créditos según peso

---

### 📦 Productos

* `GET /productos`
  Muestra todos los productos disponibles

* `POST /productos` *(Si está habilitado)*
  Crea un nuevo producto

  **Ejemplo JSON:**

  ```json
  {
    "nombre": "pc",
    "descripcion": "pc gamer xd",
    "peso": 30
  }
  ```

---





---

## Autor

Made by Josue Moreno
