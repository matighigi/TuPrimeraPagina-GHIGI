# TuPrimeraPagina+GHIGI

## Tercera Pre-Entrega – Curso Python – Coderhouse

Este proyecto corresponde a la tercera pre-entrega del curso Python de Coderhouse.  
Es una aplicación web desarrollada con **Django**, siguiendo el patrón **MVT**.

Incluye:

- Herencia de plantillas HTML  
- Tres modelos con formularios  
- Un formulario de búsqueda en base de datos  
- Proyecto completo y funcional  
- Subido a GitHub como se solicita  

---

## 🛠 Tecnologías utilizadas

- Python 3.10+
- Django 6.0
- HTML5
- SQLite

---

## 📁 Estructura del proyecto

```text
TuPrimeraPagina+GHIGI/
│
├── tuprimera_pagina/
│   ├── settings.py
│   ├── urls.py
│   └── ...
│
├── blog/
│   ├── models.py
│   ├── forms.py
│   ├── views.py
│   ├── urls.py
│   └── templates/
│       └── blog/
│           ├── base.html
│           ├── inicio.html
│           ├── crear_autor.html
│           ├── crear_categoria.html
│           ├── crear_post.html
│           └── buscar_post.html
│
├── db.sqlite3
└── README.md

🧱 Modelos
🧍 Autor
Campo	Tipo
nombre	CharField
apellido	CharField
email	EmailField (único)
bio	TextField (opcional)
🗂️ Categoría
Campo	Tipo
nombre	CharField
descripcion	TextField (opcional)
📝 Post
Campo	Tipo
titulo	CharField
contenido	TextField
fecha_publicacion	DateField (auto_now_add=True)
autor	ForeignKey a Autor
categoria	ForeignKey a Categoría
🧾 Formularios (forms.py)

En forms.py se definieron formularios basados en ModelForm, los cuales permiten cargar datos a los modelos:

AutorForm

CategoriaForm

PostForm

Cada formulario incluye validación automática y renderizado sencillo desde los templates HTML.

🔍 Búsqueda de posts

Se añadió una vista y un formulario de búsqueda que permite buscar posts por título.

La consulta utiliza coincidencias parciales con:

Post.objects.filter(titulo__icontains=termino)


Ruta de la búsqueda:
/buscar/

🌐 Rutas principales del sistema
URL	Descripción
/	Página de inicio
/autor/nuevo/	Crear autor
/categoria/nueva/	Crear categoría
/post/nuevo/	Crear post
/buscar/	Buscar posts
▶️ Cómo ejecutar el proyecto
1. Clonar el repositorio
git clone https://github.com/TUUSUARIO/TuPrimeraPagina+GHIGI.git


Reemplazar TUUSUARIO por tu usuario real de GitHub.

2. Instalar Django (si es necesario)
pip install django

3. Aplicar migraciones
python manage.py migrate

4. Ejecutar servidor
python manage.py runserver

5. Abrir en navegador
http://127.0.0.1:8000/

🧪 Orden recomendado para probar

Crear un Autor

Crear una Categoría

Crear un Post

Ir a la sección Buscar Post y buscar por el título

Confirmar que los formularios funcionan y la búsqueda arroja resultados

👤 Autor
