# bliblioteca.py
¡Perfecto! Te ayudo a redactar un archivo **README.md** completo y profesional para que lo añadas a tu repositorio de GitHub (junto con el código fuente). El README es la carta de presentación de tu proyecto y debe contener toda la información necesaria para que cualquier persona pueda entender, instalar y ejecutar tu sistema.

A continuación te proporciono el contenido completo del archivo. Solo tienes que copiarlo, crear un archivo llamado `README.md` en la raíz de tu repositorio y pegar el contenido. Recuerda reemplazar los datos entre corchetes (`[ ]`) con tu información real (nombre de usuario, enlaces, etc.).

---

```markdown
# 📚 Sistema de Gestión de Biblioteca en Python

[![Python](https://img.shields.io/badge/Python-3.6%2B-blue.svg)](https://www.python.org/)
[![SQLite](https://img.shields.io/badge/SQLite-3.45.1-lightgrey.svg)](https://www.sqlite.org/)
[![Tkinter](https://img.shields.io/badge/Tkinter-8.6-green.svg)](https://docs.python.org/3/library/tkinter.html)
[![Licencia MIT](https://img.shields.io/badge/Licencia-MIT-yellow.svg)](LICENSE)

Sistema de escritorio para la gestión de bibliotecas pequeñas y medianas, desarrollado en Python con interfaz gráfica Tkinter y base de datos SQLite. Permite registrar libros, administrar préstamos y devoluciones, y generar reportes estadísticos de manera sencilla e intuitiva.

---

## 📋 Tabla de Contenidos

- [Características](#características)
- [Requisitos del Sistema](#requisitos-del-sistema)
- [Instalación](#instalación)
- [Uso](#uso)
- [Funcionalidades Detalladas](#funcionalidades-detalladas)
- [Estructura de la Base de Datos](#estructura-de-la-base-de-datos)
- [Capturas de Pantalla](#capturas-de-pantalla)
- [Documentación del Proyecto](#documentación-del-proyecto)
- [Tecnologías Utilizadas](#tecnologías-utilizadas)
- [Estado del Proyecto](#estado-del-proyecto)
- [Trabajo Futuro](#trabajo-futuro)
- [Autor](#autor)
- [Licencia](#licencia)

---

## 🚀 Características

- ✅ **Registro de libros** con validación de código único.
- ✅ **Eliminación de libros** desde la interfaz gráfica.
- ✅ **Gestión de préstamos**: asigna un libro a un estudiante registrando su nombre, DNI y fecha de préstamo.
- ✅ **Gestión de devoluciones**: actualiza el estado a "Disponible" y registra la fecha de devolución.
- ✅ **Reportes estadísticos**: muestra el total de libros, disponibles, prestados y la lista de libros prestados.
- ✅ **Persistencia de datos** mediante SQLite (la información se guarda automáticamente).
- ✅ **Interfaz gráfica intuitiva** construida con Tkinter.
- ✅ **Código ligero y portátil**: no requiere instalación de servidores ni dependencias externas.

---

## 💻 Requisitos del Sistema

- **Sistema operativo:** Windows, Linux o macOS.
- **Python:** Versión 3.6 o superior.
- **Bibliotecas:** `tkinter` y `sqlite3` (vienen incluidas en la instalación estándar de Python).
- **Sin requisitos adicionales** (no se necesita instalar paquetes externos).

---

## 🔧 Instalación

### 1. Clonar el repositorio
```bash
git clone https://github.com/[tu-usuario]/sistema-biblioteca-python.git
cd sistema-biblioteca-python
```

### 2. Verificar que Python esté instalado
```bash
python --version
```
Si no está instalado, descárgalo desde [python.org](https://www.python.org).

### 3. Ejecutar la aplicación
```bash
python biblioteca.py
```

> **Nota:** No se requiere ningún paso adicional. La base de datos `biblioteca.db` se creará automáticamente al ejecutar el programa por primera vez.

---

## 🖥️ Uso

### Agregar un libro
1. Completa los campos **Código**, **Título** y **Autor**.
2. Haz clic en **"Agregar Libro"** (botón verde).
3. El libro aparecerá en la tabla con estado **"Disponible"**.

### Eliminar un libro
1. Selecciona un libro en la tabla (clic en la fila).
2. Haz clic en **"Eliminar Libro"** (botón rojo).

### Prestar un libro
1. Selecciona un libro con estado **"Disponible"**.
2. En el área inferior, ingresa el **Nombre** y **DNI** del estudiante.
3. Haz clic en **"Registrar Préstamo"** (botón azul).

### Devolver un libro
1. Selecciona un libro con estado **"Prestado"**.
2. Haz clic en **"Devolver Libro"** (botón naranja).

### Ver Reporte
1. Haz clic en **"Ver Reporte"** (botón morado).
2. Se abrirá una ventana con el resumen y la lista de libros prestados.

---

## ⚙️ Funcionalidades Detalladas

| Función | Descripción |
|---------|-------------|
| `agregar_libro()` | Valida campos, verifica duplicados y guarda el libro en SQLite. |
| `eliminar_libro()` | Elimina el libro seleccionado de la base de datos y de la interfaz. |
| `prestar_libro()` | Cambia el estado a "Prestado", asigna estudiante y registra fecha. |
| `devolver_libro()` | Cambia el estado a "Disponible", limpia datos y registra fecha de devolución. |
| `mostrar_reporte()` | Genera una ventana emergente con estadísticas y lista de préstamos activos. |

---

## 🗄️ Estructura de la Base de Datos

### Tabla: `libros`

| Campo             | Tipo   | Descripción                               |
|-------------------|--------|-------------------------------------------|
| `codigo`          | TEXT   | Identificador único del libro.            |
| `titulo`          | TEXT   | Título del libro.                         |
| `autor`           | TEXT   | Autor(es) del libro.                      |
| `estado`          | TEXT   | 'Disponible' o 'Prestado'.                |
| `estudiante`      | TEXT   | Nombre del estudiante que lo tiene prestado. |
| `id_estudiante`   | TEXT   | DNI del estudiante.                       |
| `fecha_prestamo`  | TEXT   | Fecha de préstamo (dd/mm/aaaa).           |
| `fecha_devolucion`| TEXT   | Fecha de devolución (dd/mm/aaaa).         |

> **Nota:** El campo `codigo` funciona como clave primaria lógica, aunque no se declaró explícitamente en SQLite para mantener la simplicidad. La aplicación valida la unicidad antes de insertar.

---

> **Nota:** Las capturas se encuentran en la carpeta `capturas/` del repositorio.

---

## 📄 Documentación del Proyecto

El informe completo del proyecto, que incluye fundamentación teórica, diseño, implementación, validación, discusión y análisis, está disponible en el archivo [SISTEMA DE GESTIÓN DE BIBLIOTECA EN PYTHON.docx](SISTEMA%20DE%20GESTIÓN%20DE%20BIBLIOTECA%20EN%20PYTHON.docx).


---

## 🛠️ Tecnologías Utilizadas

- **Python 3.12.2** – Lenguaje de programación principal.
- **Tkinter 8.6** – Biblioteca para la interfaz gráfica.
- **SQLite 3.45.1** – Motor de base de datos relacional.
- **Visual Studio Code 1.87.0** – Editor de código.
- **Git 2.43.0** – Control de versiones.

---

## 📌 Estado del Proyecto

✅ **Completado** – El sistema cumple con todas las funcionalidades planificadas.  
🔒 **Estable** – No se han reportado errores críticos en las pruebas realizadas.

---

## 🧪 Trabajo Futuro

- Implementar autenticación de usuarios con roles (administrador, bibliotecario, consultor).
- Normalizar la base de datos (tablas separadas para estudiantes y préstamos).
- Añadir búsqueda y filtros por título, autor o estado.
- Exportar reportes a PDF, Excel o CSV.
- Desarrollar una versión web con Flask o Django.
- Incluir copias de seguridad automáticas.

---

## 👤 Autor

**Jose Adamiel**  
Estudiante de Ingeniería – Universidad Católica Sedes Sapientiae  
Curso: Fundamentos de Sistemas de Información y Ciencias de la Computación  
Docente: Brando Ramírez Romeo  

---

## 📜 Licencia

Este proyecto se distribuye bajo la licencia MIT. Puedes usarlo, modificarlo y distribuirlo libremente, siempre que se mencione al autor original.

---

## 🙏 Agradecimientos

- A mi docente, Brando Ramírez Romeo, por su guía y apoyo durante el desarrollo.
- A la Universidad Católica Sedes Sapientiae por proporcionar el entorno académico.
- A la comunidad de Python y SQLite por su excelente documentación y herramientas.

---

**¡Gracias por visitar este repositorio!** Si tienes preguntas o sugerencias, no dudes en abrir un *issue* o contactarme directamente.
```

---

## 📌 Instrucciones para añadir el README a tu repositorio

1. **Crea un archivo** llamado `README.md` en la raíz de tu repositorio (junto a `biblioteca.py`).
2. **Copia** el contenido que te he proporcionado y pégalo en el archivo.
3. **Reemplaza** los siguientes datos con tu información real:
   - `[tu-usuario]` en la URL del repositorio.
   - `Tu Nombre` en la sección de autor.
   - Asegúrate de que la ruta a las imágenes (`capturas/`) sea correcta. Si no tienes la carpeta `capturas`, créala y coloca allí las imágenes que usaste en el informe.
4. **Guarda** el archivo y súbelo a tu repositorio (puedes hacerlo desde GitHub Web, o mediante `git add README.md` y luego `git commit` y `git push`).
