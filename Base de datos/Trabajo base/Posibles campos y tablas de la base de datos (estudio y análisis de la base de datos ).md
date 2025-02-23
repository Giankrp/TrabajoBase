---
created: 2025-02-10T00:17
updated: 2025-02-15T20:11
tags:
  - Trabajobase
---
# Análisis Preliminar

Antes de proceder con el diseño, se realizó un análisis inicial para identificar los principales requerimientos funcionales y no funcionales de la base de datos.

##  Requerimientos Funcionales:

- Registrar, actualizar y eliminar productos del inventario.
- Controlar las categorías a las que pertenece cada producto.
- Gestionar la información de los proveedores.
- Generar reportes básicos sobre el estado del inventario (e.g., productos con bajo stock).
## Requerimientos No Funcionales:

- La base de datos debe ser ligera, eficiente y fácil de escalar.
- Se debe garantizar la integridad de los datos mediante restricciones adecuadas.
- Debe implementarse en **MySQL** por ser el sistema gestor de bases de datos elegido para el módulo.
## Objetivo General

Diseñar e implementar una base de datos relacional en **MySQL** para la gestión de inventarios, que permita el registro, consulta, actualización y eliminación de información relacionada con productos, categorías y proveedores de manera eficiente.

### Objetivos Específicos:

1. Diseñar un modelo Entidad-Relación (ER) que refleje las relaciones entre los datos del inventario.
2. Implementar el esquema de la base de datos en MySQL mediante sentencias SQL (`CREATE TABLE`, `ALTER TABLE`, etc.).
3. Realizar pruebas básicas para garantizar la funcionalidad del sistema.
4. Documentar el proceso de diseño, implementación y pruebas.
## Metodología

El desarrollo del proyecto seguirá una metodología estructurada, dividiendo el trabajo en las siguientes etapas:

1. **Definición de Requisitos:**
    - Identificar las entidades y relaciones principales (productos, categorías, proveedores).
    - Definir las funcionalidades básicas requeridas por el sistema.
2. **Diseño Conceptual:**
    - Elaborar un diagrama Entidad-Relación para representar visualmente las entidades y sus relaciones.
    - Describir cada entidad y sus atributos.
3. **Diseño Lógico:**
    - Traducir el modelo conceptual en un esquema SQL.
    - Definir claves primarias, claves foráneas y restricciones.
4. **Implementación:**
    - Escribir las sentencias SQL necesarias para crear la base de datos y las tablas.
    - Insertar datos de prueba para validar el correcto funcionamiento.
5. **Pruebas y Validación:**
    - Realizar consultas para verificar la consistencia e integridad de los datos.
    - Probar casos extremos (e.g., eliminación de registros relacionados).
## Conclusión Inicial

La elección de desarrollar una base de datos para inventarios no solo permite aplicar los conocimientos adquiridos en el módulo de DAM, sino también enfrentar retos prácticos del mundo real. Este proyecto tiene el potencial de ser una herramienta básica para empresas pequeñas o medianas, y sirve como base para integrar sistemas más complejos en el futuro.


>[!Check] Hecho

```dataviewjs

const pages = dv.pages('#tabla');


for (const page of pages) {
    // Comprobar si la nota tiene datos de tabla
    if (page.tabla && page.datos) {
        dv.header(2, `Tabla: ${page.tabla}`); 

        // Crear la tabla dinámicamente
        dv.table(
            page.campos, 
            page.datos  
        );
    }
}

```

```dataviewjs

const pages = dv.pages('#tabla');


for (const page of pages) {
 
    if (page.tabla && page.datos) {
        dv.header(2, `Tabla: ${page.tabla}`);

        // Crear la tabla dinámicamente
        dv.table(
            page.campos, // Usar los nombres de los campos como encabezado
            page.datos   // Mostrar cada registro como fila
        );
    }
}

```



