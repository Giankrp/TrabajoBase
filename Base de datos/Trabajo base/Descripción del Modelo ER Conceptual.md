---
created: 2025-02-15T20:25
updated: 2025-02-23T23:50
---

Este modelo representa la estructura de una base de datos diseñada para gestionar el inventario de productos informáticos. Incluye entidades principales, sus atributos y las relaciones entre ellas para controlar el flujo de entrada y salida de productos.

### **Entidades y sus Atributos:**

1. **Productos:**  
    Representa los productos informáticos en el inventario. Cada producto tiene:
    
    - `id_producto`: Identificador único del producto.
    - `nombre`: Nombre del producto.
    - `precio`: Precio del producto.
    - `marca`: Marca del producto (ej. ASUS, Dell, HP).
    - `categoria`: Tipo de producto (ej. laptop, monitor, periférico).
    - `stock`: Cantidad disponible en el inventario.
    - `precio`: Precio unitario del producto.
    - `id_proveedor`: Relaciona el producto con su proveedor.
    - `especificaciones`: Descripción técnica del producto.
    
2. **Proveedores:**  
    Contiene la información de los proveedores que suministran productos. Sus atributos incluyen:
    
    - `id_proveedor`: Identificador único del proveedor.
    - `nombre`: Nombre del proveedor.
    - `telefono`: Número de contacto.
    - `email`: Correo electrónico del proveedor.
    - `direccion`: Ubicación del proveedor.
3. **Clientes:**
	Contiene la información de los clientes que han comprado un producto o productos. Sus atributos incluyes
	- `id_cliente`: Identificador único del cliente.
	- `nombre_completo`: Nombre del cliente que desglosa su nombre y apellido.
	- `telefono`: Teléfono del cliente.
	- `email`: Email del cliente para poder suministrar información adicional como estado de  pedidos, promociones y pagos.
	- `DNI`: Numero de identidad del cliente
	- `direccion`: Dirección del cliente necesarios en caso de pedidos
4. **Entradas:**  
    Registra las compras o ingresos de productos al inventario. Sus atributos son:
    
    - `id_entrada`: Identificador único de la entrada.
    - `fecha`: Fecha en que se registró la entrada.
    - `id_proveedor`: Proveedor que suministró los productos.
5. **DetalleEntrada:**  
    Desglosa los productos incluidos en cada entrada. Sus atributos incluyen:
    
    - `id_detalle`: Identificador del detalle.
    - `id_entrada`: Relación con la entrada correspondiente.
    - `id_producto`: Producto incluido en la entrada.
    - `cantidad`: Cantidad de unidades recibidas.
    - `precio_unitario`: Precio por unidad del producto en la entrada.
6. **Salidas:**  
    Registra la salida de productos del inventario, ya sea por venta o uso interno. Sus atributos son:
    
    - `id_salida`: Identificador único de la salida.
    - `fecha`: Fecha de la salida.
    - `cliente`: Persona o empresa que recibe el producto.
    - `motivo`: Razón de la salida (ej. venta, reposición, devolución).
7. **DetalleSalida:**  
    Detalla los productos incluidos en cada salida. Sus atributos son:
    
    - `id_detalle`: Identificador del detalle.
    - `id_salida`: Relación con la salida correspondiente.
    - `id_producto`: Producto que se está retirando.
    - `cantidad`: Cantidad de unidades retiradas.
    - `precio_unitario`: Precio por unidad en la salida.

---

### **Relaciones entre Entidades:**

- **Varios productos pueden ser comprados por uno o mas clientes** (`Productos }|--||Clientes`).
- **Varios productos son suministrados por varios proveedores** (`Productos }o--|{ Proveedores`).
-  **Varios productos pueden ser comprados por varios clientes **  (`Productos }o--|{ Clientes`)
- **Una entrada de productos está vinculada a un proveedor** (`Entradas ||--|| Proveedores`).
- **Una entrada puede contener varios productos** (`Entradas ||--o{ DetalleEntrada`).
- **Cada producto en una entrada se detalla en DetalleEntrada** (`DetalleEntrada ||--|| Productos`).
- **Una salida de productos puede contener varios productos** (`Salidas ||--o{ DetalleSalida`).
- **Cada producto en una salida se detalla en DetalleSalida** (`DetalleSalida ||--|| Productos`).

---

## **Conclusión:**

Este modelo ER conceptual organiza eficientemente la información relacionada con el **gestor de inventario** de productos informáticos. Permite un control estructurado sobre los productos, proveedores y movimientos de stock, garantizando una gestión clara de las **entradas y salidas** de los productos en el sistema.

>[!Tip] Haciendo