# Java Swing Point of Sale and Inventory System

A desktop point-of-sale prototype developed with **Java Swing**. The application supports product registration, inventory tracking, product search, wholesale pricing, and sales-total calculation.

## Features

- Register products with:
  - ID and product code
  - Name and description
  - Available quantity
  - Unit and wholesale prices
  - Product image
- Validate required fields and duplicated products
- Import and export product information as TXT files
- Search products by name
- Add selected quantities to a sale
- Automatically reduce available inventory
- Apply wholesale pricing to purchases of 10 or more units
- Calculate subtotal and 16% VAT
- Customize interface text colors
- Navigate between catalog, search, and sales windows

## Technologies

- Java 18
- Java Swing
- NetBeans
- Apache Ant
- Object-oriented programming
- Java file handling

## Project Structure

```text
P3_PV_MCPB_312/
├── src/
│   ├── Modelos/
│   │   └── Producto.java
│   ├── Negocio/
│   │   └── NegocioProducto.java
│   └── p3_pv_mcpb_312/
│       ├── P3_PV_MCPB_312.java
│       ├── frmProducto.java
│       ├── frmListaBúsqueda.java
│       └── frmVentas.java
├── nbproject/
├── build.xml
└── manifest.mf
````

## Run the Project

### NetBeans

1. Open the project in Apache NetBeans.
2. Make sure JDK 18 or a compatible version is configured.
3. Run the project.

### Command Line

Build the project with Ant:

```bash
ant clean jar
```

Run the generated application:

```bash
java -jar dist/P3_PV_MCPB_312.jar
```

## Pricing Logic

* Quantities below 10 use the unit price.
* Quantities of 10 or more use the wholesale price.
* The total includes 16% VAT.

## Project Status

This is an academic desktop prototype. Product information is stored in memory during the current execution, and TXT import/export handles individual product records rather than a persistent inventory database.
