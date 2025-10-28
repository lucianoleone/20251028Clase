cuales son los pasos para crear un proyecto en django desde cero# Crear un Proyecto Django desde Cero con GitHub y VS Code

Guía paso a paso para crear un proyecto Django, usar Git y GitHub, y trabajar cómodamente con Visual Studio Code.

---

## 🧰 Requisitos Previos

- Python instalado (recomendado 3.10+)
- Git instalado y configurado (`git config --global user.name "TuNombre"`)
- Cuenta en GitHub
- Visual Studio Code instalado

---

## 1. Crear la Carpeta del Proyecto

```bash
mkdir mi_proyecto_django
cd mi_proyecto_django
```

---

## 2. Crear y Activar el Entorno Virtual

```bash
# Linux / macOS
python3 -m venv venv
source venv/bin/activate

# Windows
python -m venv venv
venv\Scripts\activate
```

---

## 3. Instalar Django

```bash
pip install django
```

Opcionalmente: guardar dependencias en un archivo

```bash
pip freeze > requirements.txt
```

---

## 4. Crear el Proyecto Django

```bash
django-admin startproject config .
```

> Esto crea el proyecto en la carpeta actual con el nombre `config`.

---

## 5. Ejecutar el Servidor para Verificar

```bash
python manage.py runserver
```

Visita `http://127.0.0.1:8000/` en tu navegador para comprobar que funciona.

---

## 6. Inicializar un Repositorio Git

```bash
git init
```

Crear un archivo `.gitignore`:

```bash
touch .gitignore
```

Agregar esto al `.gitignore`:

```text
venv/
__pycache__/
*.pyc
db.sqlite3
.env
```

---

## 7. Subir el Proyecto a GitHub

1. Crear un nuevo repositorio vacío en GitHub (sin README ni .gitignore).
2. En terminal:

```bash
git add .
git commit -m "Primer commit"
git branch -M main
git remote add origin https://github.com/TU_USUARIO/TU_REPO.git
git push -u origin main
```

---

## 8. Abrir el Proyecto en Visual Studio Code

```bash
code .
```

> Asegúrate de tener la extensión de Python y Django instaladas en VS Code.

---

## 9. Trabajar con el Proyecto

- Crear apps con `python manage.py startapp`
- Activar el entorno cada vez que trabajes con:

```bash
source venv/bin/activate  # Linux/macOS
venv\Scripts\activate     # Windows
```

---

## ✅ Listo

Tu entorno de desarrollo Django está listo, con Git y GitHub integrados, y VS Code como editor.
