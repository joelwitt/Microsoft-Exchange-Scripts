# SecuPass  
Gestor sencillo de contraseñas con interfaz gráfica y por consola  
Trabajo final – Programación 1 – Tecnicatura Soporte de Infraestructura de Sistemas

---

## Descripción general

SecuPass es una aplicación desarrollada en Python cuyo objetivo es brindar una herramienta simple para la gestión básica de credenciales y la evaluación de la fortaleza de contraseñas.  
El proyecto fue construido aplicando las buenas prácticas vistas en la materia: modularidad, PEP8, uso de docstrings, manejo de excepciones y separación clara entre lógica y presentación.

La aplicación ofrece dos formas de uso:

### Interfaz por consola
Permite:
- Evaluar contraseñas
- Crear nuevas credenciales
- Listar las credenciales registradas
- Eliminar registros
- Verificar si una contraseña coincide con el hash almacenado

### Interfaz gráfica (Tkinter)
Ofrece dos secciones:
- Evaluación de contraseñas
- Gestión de credenciales (alta, baja, verificación y visualización)

En ambos casos, las contraseñas no se almacenan en texto plano: SecuPass utiliza `bcrypt` para generar hashes seguros.

---

## Estructura del proyecto

SecuPass/
│
├── gui_secupass.py # Interfaz gráfica (Tkinter)
├── main.py # Interfaz de consola
├── security.py # Funciones principales, manejo de datos y hashing
│
├── passwords.json # Archivo donde se almacenan las credenciales
├── secupass.log # Registro de eventos y errores
│
├── requirements.txt # Dependencias del entorno virtual
└── README.md # Documentación del proyecto


---

## Requisitos y entorno virtual

Se recomienda ejecutar el proyecto dentro de un entorno virtual de Python.

### Crear y activar un entorno virtual

Windows:

```bash
python -m venv venv
venv\Scripts\activate
```
Linux/macOS:

```bash
python3 -m venv venv
source venv/bin/activate
```
---

## Instalar dependencias

```bash
pip install -r requirements.txt
```
## Ejecución del programa

### Interfaz por consola
```bash
python main.py
```
### Interfaz por grafica
```bash
python gui_secupass.py
```

## Librerías utilizadas

### Externas:

bcrypt — hashing seguro de contraseñas

colorama — realce visual para la interfaz de consola

### Nativas:

tkinter — interfaz gráfica

json — manejo de datos persistentes

logging — registro de eventos

os — comprobación de archivos

## Autoría

Trabajo final realizado por Yanina Ramirez
Tecnicatura Universitaria en Soporte de Infraestructura de Sistemas – ISTEA
Año 2025