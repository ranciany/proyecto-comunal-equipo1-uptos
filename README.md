# SIGECOC - Sistema Automatizado de Gestión Comunal

## 1. Descripción del Proyecto
SIGECOC es una plataforma web orientada a modernizar y optimizar los procesos administrativos de los Consejos Comunales. El sistema permite gestionar el censo demográfico, automatizar la emisión de constancias (cartas de residencia, buena conducta) y llevar el control de los proyectos socio-productivos de la comunidad.

## 2. Requisitos Técnicos Estimados (Stack Tecnológico)
* **Lenguaje Backend:** Python 3.12
* **Framework Web:** Flask
* **Motor de Base de Datos:** PostgreSQL 16 (Relacional)
* **Frontend:** HTML5, CSS3 (Tailwind CSS) y JavaScript Vanilla.
* **Control de Versiones:** Git y GitHub.

## 3. Manual de Instalación del Entorno de Desarrollo

Siga estos pasos para ejecutar el proyecto en su máquina local:

**Paso 1: Clonar el repositorio**
Abre la terminal de comandos y ejecuta:
> git clone https://github.com/UPTOS-Equipo1/sigecoc-app.git
> cd sigecoc-app

**Paso 2: Crear y activar el entorno virtual**
> python -m venv .venv
* En Windows: `.venv\Scripts\activate`
* En Linux/Mac: `source .venv/bin/activate`

**Paso 3: Instalar las dependencias**
Con el entorno virtual activado, instala los requerimientos del proyecto:
> pip install -r requirements.txt

**Paso 4: Configurar la Base de Datos**
Crea una base de datos en PostgreSQL llamada `sigecoc_db`. Luego, renombra el archivo `.env.example` a `.env` y configura la cadena de conexión de SQLAlchemy:
> DATABASE_URL=postgresql://usuario:contraseña@localhost:5432/sigecoc_db

**Paso 5: Ejecutar las migraciones y levantar el servidor**
> flask db upgrade
> python app.py

El sistema estará disponible en su navegador ingresando a `http://localhost:5000`.
