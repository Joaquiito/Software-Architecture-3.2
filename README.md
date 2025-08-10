# Ejercicio 2 - Sistema de Áreas y Empleados con MVC + Velocity + SQL2o

## 📌 Objetivo
Este ejercicio amplía el trabajo realizado en el **Ejercicio 1**, incorporando **Velocity** como motor de plantillas y combinando la arquitectura **MVC** con un enfoque **REST** para la creación de microservicios web.

Se mantiene el modelo de datos de áreas y empleados, pero ahora se proveen vistas dinámicas a través de archivos `.vtl` y se exponen rutas REST para la interacción con la información.

---

## 🛠 Herramientas y Requisitos
- **Java**
- **Spark Java**
- **Velocity** (motor de plantillas)
- **SQL2o**
- **MySQL** (o cualquier otro motor compatible)
- Proyecto base del **Ejercicio 1**
- Patrón **MVC** implementado
- Configuración de entorno según la Parte III del TP

---

## 🗄 Modelo de Base de Datos

### Tablas
Se reutiliza el modelo de datos del Ejercicio 1:

**AREA**
| Campo   | Tipo      | Descripción                      |
|---------|-----------|----------------------------------|
| codigo  | PK, int   | Identificador único del área      |
| nombre  | varchar   | Nombre del área                  |
| director| varchar   | Director del área                |

**EMPLEADO**
| Campo     | Tipo      | Descripción                              |
|-----------|-----------|------------------------------------------|
| nombre    | PK, varchar | Nombre del empleado                    |
| categoria | varchar   | Categoría laboral del empleado           |
| dedicacion| varchar   | Dedicación (por ejemplo, tiempo completo)|
| codigo    | FK, int   | Área en la que trabaja (referencia a AREA)|

---

## 📋 Funcionalidades Implementadas
1. **Retornar todas las áreas**  
2. **Dada un área, mostrar los empleados que pertenecen a la misma**  
3. **Agregar un área**  
4. **Listar todos los empleados**  
5. **Buscar un empleado y mostrar a qué área pertenece**  
6. **Obtener la cantidad de empleados por área**  
7. **Agregar un empleado indicando el área en la que trabaja (solo un área)**  

> **Nota**: Se construye un **único archivo `.vtl` cohesivo** que gestiona la presentación de los datos de todas estas funcionalidades, en lugar de un archivo por cada resultado.

---

## 🚀 Ejecución
1. **Clonar el repositorio**
   ```bash
   git clone https://github.com/usuario/nombre-repo.git
