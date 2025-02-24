---
created: 2025-02-11T00:33
updated: 2025-02-24T01:01
tags:
  - Trabajobase
---
A continuación, se presentan los posibles casos de uso del sistema basado en la estructura de la base de datos. Estos casos describen las principales interacciones que los usuarios pueden realizar con el sistema.

---

## **1. Gestión de Productos**

### **1.1 Registrar un nuevo producto**

**Actor:** Administrador del inventario  
**Descripción:** Se agrega un nuevo producto con todos sus detalles, como nombre, marca, modelo, categoría, proveedor y precio.  
**Flujo principal:**

1. El usuario accede al módulo de productos.
2. Ingresa los datos del nuevo producto.
3. Se asocia el producto a una categoría y proveedor.
4. Se guarda el producto en la base de datos.

### **1.2 Actualizar información de un producto**

**Actor:** Administrador del inventario  
**Descripción:** Se editan datos de un producto, como precio, stock o proveedor.  
**Flujo principal:**

1. El usuario busca el producto en el inventario.
2. Modifica la información necesaria.
3. Guarda los cambios en la base de datos.

### **1.3 Eliminar un producto**

**Actor:** Administrador del inventario  
**Descripción:** Se elimina un producto del inventario si ya no se maneja en la tienda.  
**Flujo principal:**

4. El usuario selecciona el producto.
5. Confirma la eliminación.
6. Se elimina el producto de la base de datos (si no tiene registros en movimientos).

---

## **2. Gestión de Categorías**

### **2.1 Registrar una nueva categoría**

**Actor:** Administrador del inventario  
**Descripción:** Se define una nueva categoría de productos, como laptops, tarjetas gráficas, periféricos, etc.

### **2.2 Editar o eliminar una categoría**

**Actor:** Administrador del inventario  
**Descripción:** Se actualiza o elimina una categoría si ya no es necesaria.

---

## **3. Gestión de Proveedores**

### **3.1 Registrar un proveedor**

**Actor:** Administrador del inventario  
**Descripción:** Se ingresa la información de un nuevo proveedor.

### **3.2 Modificar o eliminar un proveedor**

**Actor:** Administrador del inventario  
**Descripción:** Se actualizan los datos de contacto de un proveedor o se elimina si ya no se trabaja con él.

---

## **4. Gestión de Entradas de Inventario**

### **4.1 Registrar una nueva entrada de productos**

**Actor:** Administrador del inventario  
**Descripción:** Se registra una nueva compra de productos a un proveedor.  
**Flujo principal:**

7. El usuario selecciona el proveedor.
8. Se añaden los productos comprados, sus cantidades y precios unitarios.
9. Se guarda la entrada y se actualiza el stock en la base de datos.

### **4.2 Consultar historial de entradas**

**Actor:** Administrador del inventario  
**Descripción:** Se revisan todas las entradas registradas en el sistema.

---

## **5. Gestión de Salidas de Inventario**

### **5.1 Registrar una salida de productos**

**Actor:** Administrador del inventario / Vendedor  
**Descripción:** Se registra la venta o retiro de productos del inventario.  
**Flujo principal:**

10. Se selecciona el cliente o motivo de la salida.
11. Se añaden los productos que se están vendiendo o retirando.
12. Se guarda la salida y se actualiza el stock.

### **5.2 Consultar historial de salidas**

**Actor:** Administrador del inventario  
**Descripción:** Se revisan todas las salidas registradas en el sistema.

---

## **6. Reportes y Análisis**

### **6.1 Generar reportes de inventario**

**Actor:** Administrador del inventario  
**Descripción:** Se generan informes sobre el estado actual del stock.

### **6.2 Generar reportes de entradas y salidas**

**Actor:** Administrador del inventario  
**Descripción:** Se generan informes detallados sobre compras y ventas realizadas.

---

### **Conclusión**

Este modelo de base de datos permite gestionar de manera eficiente el flujo de productos, garantizando el control de **entradas, salidas, proveedores y stock**. Además, proporciona herramientas para el análisis del inventario y facilita la toma de decisiones dentro de la empresa.

>[!Check] Hecho
