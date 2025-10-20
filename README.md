# GEO-AYUDA
# 🔐 Sistema de Inicio de Sesión en JavaScript

Este proyecto es una aplicación web simple que permite a los usuarios **registrarse, iniciar sesión y cerrar sesión**, utilizando **almacenamiento local (`localStorage`)** para guardar la información del usuario y mantener la sesión activa.  
Además, el sistema **detecta en qué página se encuentra el usuario** y **resalta el botón correspondiente del menú de navegación**.  

---

## 🚀 Características principales

- 🧍‍♂️ Registro de nuevos usuarios  
- 🔑 Inicio y cierre de sesión con validación de datos  
- 💾 Almacenamiento de información en `localStorage`  
- 🔄 Persistencia de sesión (el usuario permanece logueado al recargar la página)  
- 🎨 Cambio dinámico de color en el botón **“Cerrar sesión”** cuando hay una sesión activa  
- 📍 Detección de la página actual y resaltado automático en el menú  
- 📱 Interfaz simple, clara y adaptable  

---

## 🧠 Tecnologías utilizadas

- **HTML5** → Estructura del sitio  
- **CSS3** → Estilos y diseño visual  
- **JavaScript (Vanilla JS)** → Lógica del sistema  
- **LocalStorage** → Persistencia local de datos  

---

## ⚙️ Funcionamiento general

### 🔹 Registro
1. El usuario completa un formulario con **nombre, correo y contraseña**  
2. Los datos se guardan en `localStorage` bajo la clave `"usuarios"`  
3. Si el correo ya existe, se muestra un mensaje de error  

### 🔹 Inicio de sesión
1. El usuario ingresa correo y contraseña  
2. El sistema verifica los datos en `localStorage`  
3. Si son correctos:
   - Se guarda la sesión activa en `localStorage` bajo `"usuarioActivo"`  
   - Se cambia el botón de “Iniciar sesión” por “Cerrar sesión”  
   - El botón se pinta con un color especial (por ejemplo, rojo)  

### 🔹 Cierre de sesión
- Al hacer clic en “Cerrar sesión”, se elimina `"usuarioActivo"` del `localStorage`, y la interfaz vuelve al estado original  

### 🔹 Detección de página activa
- El script analiza la **URL actual** y añade una clase CSS (`active`) al botón del menú correspondiente, para indicar en qué sección está el usuario  

