# Ventas Online

## Entidades

### CUSTOMERS (ED)
- id **(PK)**
- name
- phoneNumber **(UQ)**
- email **(UQ)**
- address 
- postalCode
- city
- countryId **(FK)**
  
### PRODUCTS (ED | EC)
- id **(PK)**
- name **(UQ)**
- description
- image
- price
- stock

### SALES (ED)
- id **(PK)**
- clienteId **(FK)**
- fecha
- monto

### COUNTRIES (EC)
- id **(PK)**
- nombre **(UQ)**
- moneda

### Tipo de Producto (EC)
### Metodo de Pago (EC)
### Promociones (EC)

### productos_por_venta (EP)
- id **(PK)**
- productId **(FK)**
- saleId **(FK)**
- amount

### Factura (EP)


## Relaciones
Un **cliente** pertenece **pais** (1 - 1)
Un **cliente** efectua **ventas** (1 - M)
Una **venta** posee **producto_por_venta** (1 - M)
Un **producto_por_venta** es **producto** (1 - 1)

## Modelo Relacional de la DB
![](Modelo_Relacional_DB.png)

## Reglas de Negocio