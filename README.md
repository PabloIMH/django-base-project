# Proyecto Base Django 🐍

Este es un proyecto base para comenzar desarrollos en Django con:

✅ PostgreSQL como base de datos lista para compeltar datos de manera local en settings.py
✅ Admin personalizado con (Biblioteca) Jazzmin  
✅ Estructura lista para clonar, renombrar y desplegar


✅También puedes usar la base de datos por defecto sqlite3, que viene incluida con Django.
No necesitas instalar ni configurar nada adicional.

👤 Te recomiendo crear un usuario administrador así:

Usuario: admin

Correo: admin@gmail.com

Contraseña: admin123

📝 Luego, cuando estés listo para producción o despliegue, puedes cambiar a PostgreSQL simplemente editando el archivo .env y el bloque DATABASES en settings.py.

---

## 🚀 Requisitos

- Python 3.10+
- PostgreSQL instalado
- pip, virtualenv

---

## 🧱 Estructura de instalación

```bash
git clone https://github.com/tu_usuario/tu_repo.git
cd django_base_project01

python -m venv env
.\env\Scriptsctivate  # en Windows
source env/bin/activate  # en Mac/Linux

pip install -r requirements.txt
```

---

## 🔐 Configuración del entorno `.env`

Crea un archivo `.env` en la raíz con el siguiente contenido:

```env
SECRET_KEY=tu_clave_generada
DEBUG=True

DB_NAME=django_base
DB_USER=postgres
DB_PASSWORD=tu_password
DB_HOST=localhost
DB_PORT=5432
```

---

## 🛠 Migraciones e inicio

```bash
python manage.py migrate
python manage.py createsuperuser
python manage.py runserver
```

Accede al panel de administración: [http://127.0.0.1:8000/admin](http://127.0.0.1:8000/admin)

---

## 📁 Renombrar app `core`

1. Cambia la carpeta `core/` por el nombre que quieras (ej: `baseDjango/`)
2. Renombra en `INSTALLED_APPS` de `'core'` a `'blog'`
3. Ajusta los imports: `from core.` → `from blog.`
4. Renombra las carpetas de `templates/core/` y `static/core/`

---

## 🌐 Stack usado

- Django
- PostgreSQL
- Jazzmin (panel admin)
- Python-Decouple (.env)
