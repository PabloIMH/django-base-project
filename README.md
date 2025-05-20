# 🐍 Proyecto Base Django

Este es un proyecto base para comenzar desarrollos en Django con:

✅ PostgreSQL como base de datos lista para configurar en `settings.py`  
✅ Admin personalizado con [Jazzmin] (https://github.com/farridav/django-jazzmin)  
✅ Estructura lista para clonar, renombrar y desplegar  
✅ También puedes usar SQLite3 (la base de datos por defecto de Django)

---

## 👤 Usuario de prueba recomendado

```
Usuario: admin
Correo: admin@gmail.com
Contraseña: admin123
```

---

## 🚀 Requisitos

- Python 3.10+
- PostgreSQL instalado (opcional si usarás SQLite)
- pip, virtualenv

---

## 📦 Clonar e instalar

```bash
git clone https://github.com/PabloIMH/django-base-project.git
cd django-base-project

python -m venv env
.\env\Scripts ctivate  # en Windows
source env/bin/activate  # en Mac/Linux

pip install -r requirements.txt
```

---

## 🔐 Configurar entorno `.env`

Crea un archivo llamado `.env` en la raíz con este contenido:

```env
SECRET_KEY=tu_clave_segura_generada
DEBUG=True

# PostgreSQL (deja en blanco para SQLite)
DB_NAME=
DB_USER=
DB_PASSWORD=
DB_HOST=
DB_PORT=
```

### 🧪 ¿Cómo generar una clave segura?

CTRL + Ñ (Windows)= Para abrir terminal en VS por ejemplo 
```bash
python -c "from django.core.management.utils import get_random_secret_key; print(get_random_secret_key())"   (copiar y pegar esta linea)
```

---

## ⚙️ Migraciones y superusuario

```bash
python manage.py migrate
python manage.py createsuperuser
```

---

## ▶️ Ejecutar el servidor

```bash
python manage.py runserver
```
Luego visita: [http://127.0.0.1:8000/](http://127.0.0.1:8000/)
Para admin: [http://127.0.0.1:8000/admin](http://127.0.0.1:8000/admin)

---

## 📁 Renombrar app `core`

1. Cambia la carpeta `core/` por el nombre deseado (ej: `blog/`)
2. En `settings.py`, cambia `'core'` por `'blog'` en `INSTALLED_APPS`
3. Ajusta todos los imports: `from core.` → `from blog.`
4. Renombra también las carpetas `templates/core/` y `static/core/`

---

## 🌐 Stack usado

- Django
- PostgreSQL
- Jazzmin
- Python-Decouple

---

© Proyecto base creado por PabloIMH – ¡listo para desarrollos profesionales! 🔥
