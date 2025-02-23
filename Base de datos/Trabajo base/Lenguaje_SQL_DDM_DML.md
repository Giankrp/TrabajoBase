---
created: 2025-02-23T01:05
updated: 2025-02-24T00:30
---

```SQL
-- Crear la tabla de Productos
CREATE TABLE Productos (
    id_producto INT AUTO_INCREMENT PRIMARY KEY,
    nombre VARCHAR(100) NOT NULL,
    precio DECIMAL(10, 2) NOT NULL,
    marca VARCHAR(50) NOT NULL,
    categoria VARCHAR(50) NOT NULL,
    stock INT NOT NULL,
    id_proveedor INT NOT NULL,
    especificaciones TEXT,
    FOREIGN KEY (id_proveedor) REFERENCES Proveedores(id_proveedor)
);

-- Crear la tabla de Proveedores
CREATE TABLE Proveedores (
    id_proveedor INT AUTO_INCREMENT PRIMARY KEY,
    nombre VARCHAR(100) NOT NULL,
    telefono VARCHAR(15),
    email VARCHAR(100),
    direccion VARCHAR(255)
);

-- Crear la tabla de Clientes
CREATE TABLE Clientes (
    id_cliente INT AUTO_INCREMENT PRIMARY KEY,
    nombre_completo VARCHAR(100) NOT NULL,
    telefono VARCHAR(15),
    email VARCHAR(100),
    DNI VARCHAR(20) NOT NULL,
    direccion VARCHAR(255)
);

-- Crear la tabla de Entradas
CREATE TABLE Entradas (
    id_entrada INT AUTO_INCREMENT PRIMARY KEY,
    fecha DATE NOT NULL,
    id_proveedor INT NOT NULL,
    FOREIGN KEY (id_proveedor) REFERENCES Proveedores(id_proveedor)
);

-- Crear la tabla de DetalleEntrada
CREATE TABLE DetalleEntrada (
    id_detalle INT AUTO_INCREMENT PRIMARY KEY,
    id_entrada INT NOT NULL,
    id_producto INT NOT NULL,
    cantidad INT NOT NULL,
    precio_unitario DECIMAL(10, 2) NOT NULL,
    FOREIGN KEY (id_entrada) REFERENCES Entradas(id_entrada),
    FOREIGN KEY (id_producto) REFERENCES Productos(id_producto)
);

-- Crear la tabla de Salidas
CREATE TABLE Salidas (
    id_salida INT AUTO_INCREMENT PRIMARY KEY,
    fecha DATE NOT NULL,
    id_cliente INT NOT NULL,
    motivo VARCHAR(255) NOT NULL,
    FOREIGN KEY (id_cliente) REFERENCES Clientes(id_cliente)
);

-- Crear la tabla de DetalleSalida
CREATE TABLE DetalleSalida (
    id_detalle INT AUTO_INCREMENT PRIMARY KEY,
    id_salida INT NOT NULL,
    id_producto INT NOT NULL,
    cantidad INT NOT NULL,
    precio_unitario DECIMAL(10, 2) NOT NULL,
    FOREIGN KEY (id_salida) REFERENCES Salidas(id_salida),
    FOREIGN KEY (id_producto) REFERENCES Productos(id_producto)
);
```