# Ventas Online

## Entidades

### clientes (ED)
- id **(PK)**
- name
- lastName
- **phoneNumber**
- email
- address
- postalCode
- city
- countryId **(FK)**
  
### proveedores (ED)

### productos (ED | EC)
- id **(PK)**
- name
- description
- image
- price
- stock
- model

### ventas (ED)
- id (PK)
- clienteId (FK)
- fecha
- monto
- productoPorVenta (FK)

### Paises (EC)
- id **(PK)**
- nombre
- moneda

### Tipo de Producto (EC)****
### Metodo de Pago (EC)
### Promociones (EC)

### productos_por_venta (EP)
- id **(PK)**
- productoId **(FK)**
- ventaId **(FK)**
- cantidadComprada

### Factura (EP)


## Relaciones
Un **Cliente** tiene **Pais** (1 - 1)
Un **Cliente** efectua **Ventas** (1 - M)