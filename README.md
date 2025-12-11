TuPrimeraPagina + GHIGI
Tercera Pre-Entrega – Curso Python – Coderhouse

Este proyecto corresponde a la tercera pre-entrega del curso de Python.
El objetivo es crear una aplicación web utilizando Django con el patrón MVT, incluyendo:

Herencia de plantillas (templates)

Mínimo 3 modelos

Formularios para insertar datos en los 3 modelos

Un formulario de búsqueda en la base de datos

Organización correcta del proyecto y funcionamiento completo

🚀 Tecnologías utilizadas

Python 3.10+

Django 6.0

SQLite (base de datos por defecto)

HTML con herencia de plantillas

📁 Estructura del proyecto
TuPrimeraPagina+GHIGI/
│
├── tuprimera_pagina/        → Configuración principal de Django
├── blog/                     → App principal del proyecto
│   ├── templates/blog/       → Templates HTML (con herencia)
│   ├── models.py             → Modelos Autor, Categoria, Post
│   ├── forms.py              → Formularios basados en ModelForm
│   ├── views.py              → Lógica del proyecto
│   ├── urls.py               → Rutas de la app
│
└── db.sqlite3                → Base de datos generada por Django

🧱 Modelos incluidos
1. Autor

nombre

apellido

email

bio

2. Categoria

nombre

descripcion

3. Post

titulo

contenido

fecha_publicacion (automática)

autor (relación ForeignKey)

categoria (relación ForeignKey)

📝 Formularios incluidos

Se crearon formularios con ModelForm para:

Crear Autor

Crear Categoría

Crear Post

Cada formulario guarda datos directamente en la base de datos.

🔍 Formulario de búsqueda

Incluye un formulario simple para buscar posts por título.

Se accede desde el menú superior.

La búsqueda filtra por coincidencias parciales (icontains).

Muestra una lista de resultados encontrados.

🌐 Rutas principales
URL	Función
/	Página de inicio
/autor/nuevo/	Crear autor
/categoria/nueva/	Crear categoría
/post/nuevo/	Crear post
/buscar/	Buscar posts
▶️ Cómo ejecutar el proyecto

Clonar el repositorio

git clone https://github.com/TuUsuario/TuPrimeraPagina+GHIGI.git


Instalar dependencias (si es necesario)

pip install django


Ejecutar migraciones

python manage.py migrate


Levantar el servidor

python manage.py runserver


Abrir en el navegador:
👉 http://127.0.0.1:8000/

🧪 Orden recomendado para probar las funcionalidades

Crear un Autor

Crear una Categoría

Crear un Post (asociándolo al autor y categoría creados)

Usar el buscador para encontrar el post por título

Ver que los formularios redirigen correctamente a la página de inicio

🎯 Estado final del proyecto

✔ Cumple el patrón MVT
✔ Tiene herencia de plantillas
✔ Tiene 3 modelos
✔ Tiene 3 formularios completos
✔ Tiene formulario de búsqueda
✔ Proyecto organizado y funcional
✔ Subible a GitHub como pre-entrega

🏁 Autor

Matias Ghigi