# Laboratorio 04 - Firebase

Este laboratorio consiste en transformar un proyecto desarrollado previamente en PHP a una propuesta ejecutada en la plataforma Google Firebase, implementando la misma funcionalidad pero aprovechando las características de Google Firestore para la manipulación y almacenamiento de datos.

## Descripción del Proyecto Original

En clases pasadas, se desarrolló una aplicación en PHP para la manipulación de la base de datos NorthWind, la cual incluía los siguientes módulos y funcionalidades:

### Módulo de Usuarios
- **Registro de un nuevo usuario**: Permite registrar nuevos usuarios en la base de datos.
- **Autenticación del usuario**: Los usuarios pueden autenticarse en la aplicación.
- **Cerrar sesión del usuario**: Función para que los usuarios finalicen su sesión.

### Módulo de Categorías
- **Listar categorías existentes**: Muestra todas las categorías disponibles.
- **Insertar, modificar y borrar categorías**: Permite la gestión completa de las categorías (creación, edición y eliminación).
- **Listar productos de una categoría específica**: Muestra los productos asociados a una categoría.
- **Manipulación de imagen por categoría**: Manejo de imágenes asociadas a cada categoría.

### Módulo de Productos
- **Listar productos existentes**: Muestra la lista de productos.
- **Insertar, modificar y borrar productos**: Gestión completa de los productos en la base de datos.

## Objetivo del Laboratorio

Migrar el proyecto anterior a Google Firebase, manteniendo la funcionalidad existente en una nueva arquitectura basada en Firestore. La aplicación final deberá replicar todos los procesos de manipulación de datos que se realizaban en el proyecto en PHP.

## Requisitos

Para que este proyecto funcione, es necesario realizar un proceso de migración de datos desde la base de datos NorthWind a Google Firestore. Esto incluye:

1. **Migración de Tablas Originales**: Se deben trasladar todas las tablas originales de la base de datos NorthWind a colecciones en Firestore.

2. **Migración de la Tabla Orders**:
   - En el caso de la tabla `Orders`, cada factura debe ser migrada como un documento completo que incluya:
     - **Detalles del Pedido (Order Details)**: Incluir los datos relevantes del pedido.
     - **Empleado**: Los datos del empleado asociado al pedido.
     - **Nombre y Contacto del Cliente**: Incluir los campos `Name` y `Contact Name` del cliente.
     - **Totales por Línea de Compra**: Incluir el total de cada línea de compra junto con el nombre del producto.

3. **Recursos Adicionales**: Este trabajo incluye los recursos necesarios para desarrollar la propuesta.

## Estructura del Proyecto

El proyecto se estructura en los siguientes módulos y colecciones en Firestore:

- **Usuarios**: Colección para gestionar la autenticación y el manejo de usuarios.
- **Categorías**: Colección para almacenar y manipular las categorías junto con sus productos asociados.
- **Productos**: Colección para la gestión de productos, que incluye su creación, modificación y eliminación.
- **Pedidos (Orders)**: Colección que almacena los pedidos completos con toda la información necesaria para una factura detallada.

## Requerimientos Técnicos

- Google Firebase y Firestore como plataforma de almacenamiento de datos.
- Migración de datos desde la base de datos NorthWind al formato de Firestore.
- Reestructuración de la lógica de autenticación y manipulación de datos para operar con Firebase.

## Pasos para Configuración

1. **Configuración de Firebase**:
   - Crear un proyecto en Google Firebase.
   - Configurar Firestore y habilitar las colecciones necesarias para cada módulo (Usuarios, Categorías, Productos, Orders).

2. **Migración de Datos**:
   - Ejecutar scripts de migración que extraigan los datos de la base de datos NorthWind y los inserten en las colecciones de Firestore con la estructura especificada.

3. **Implementación de Funcionalidades**:
   - Desarrollar las funciones para CRUD en Firestore que repliquen la funcionalidad de PHP, adaptando las operaciones de autenticación, gestión de categorías, productos y pedidos a Firebase.

4. **Pruebas**:
   - Validar que todas las funcionalidades migradas funcionan correctamente en el entorno de Firebase y que los datos se presentan de forma consistente en Firestore.

## Recursos Incluidos

Este repositorio incluye los archivos y recursos necesarios para la implementación en Firebase, así como la estructura básica para la migración de datos y la ejecución del proyecto.

---

**Nota**: Asegúrate de que todos los usuarios y módulos se configuren correctamente para cumplir con los estándares de seguridad y autenticación de Firebase.
