# Inventory-system
![Imagen](./Inventory-system.webp)

Este es un sistema de gestión de inventarios para una tienda de belleza. Permite realizar el seguimiento de ventas, productos, proveedores y clientes, así como generar reportes y mantener la base de datos actualizada. Este sistema también incluye funcionalidades de facturación, gestión de stock, y alertas cuando los productos están por agotarse.

## Características

- **Gestión de Inventarios:** Registro y actualización de productos en inventario.
- **Ventas:** Realización de ventas y seguimiento del stock.
- **Facturación:** Generación de facturas en texto y en formato CSV.
- **Reportes:** Generación de reportes de ventas y productos.
- **Alertas de Stock:** Notificación cuando un producto está por agotarse.

## Librerías utilizadas

- `sqlite3`: Para la gestión de base de datos.
- `plotly`: Para la visualización de gráficos e informes en el dashboard.
- `matplotlib`: Para gráficos adicionales.
- `tkinter`: Para interfaces gráficas de usuario.

## Instalación

### En Windows

1. Clona este repositorio en tu máquina:
   ```bash
   git clone https://github.com/IngEliab/Inventory-system.git
   cd Inventory-system/

2. Crea un entorno virtual (opcional pero recomendado):

```python -m venv venv```


3. Activa el entorno virtual:

```.\venv\Scripts\activate```


4. Instala las dependencias:

```pip install -r requirements.txt```


5. Ejecuta el sistema:

```python inventario.py```



En Linux / Termux

1. Clona este repositorio en tu máquina:

```
git clone https://github.com/IngEliab/Inventory-system.git
cd Inventory-system/
```

2. Si no tienes un entorno virtual, instálalo:

```sudo apt install python3-venv```


3. Crea un entorno virtual:

```python3 -m venv venv```


4. Activa el entorno virtual:

```source venv/bin/activate```


5. Instala las dependencias:

```pip install -r requirements.txt```


6. Ejecuta el sistema:

```python3 inventario.py```



## Estructura de archivos

```
Inventory-system/
│
├── inventario.py     -->   # Archivo principal del sistema
├── factura.py        -->   # Gestión de facturación
├── dashboard.py      -->   # Visualización de ventas y productos
├── requirements.txt  -->   # Dependencias del proyecto
├── inventario.db     -->   # Base de datos
├── README.md         -->   # Este archivo
└── otros_archivos.py -->   # Otros archivos útiles
```

##Mejoras futuras

-**Generación de facturas en PDF: Añadir la capacidad de generar facturas en formato PDF para un formato más profesional.**

-**Integración de correo electrónico: Enviar automáticamente las facturas por correo electrónico a los clientes.**

-**Soporte para múltiples almacenes: Gestionar productos en diferentes ubicaciones.**

-**Historial de movimientos: Registrar los cambios de inventario y quién los realizó.**

-**Mejoras en la interfaz gráfica: Hacer la interfaz más interactiva y accesible.**

-**Análisis de ventas avanzado: Agregar filtros y más opciones de personalización en los reportes.**
---
## Configuración de la Base de Datos

El archivo `configurar_base_datos.py` es una herramienta para configurar la base de datos del sistema de inventario. Este script crea las tablas necesarias y permite al usuario ingresar datos esenciales para configurar el sistema antes de empezar a usarlo.

### ¿Cómo funciona?

1. **Estructura de la base de datos:**
   El script crea las siguientes tablas en una base de datos SQLite llamada `inventario.db`:
   - **productos**: Contiene información sobre los productos (nombre, descripción, precio, cantidad, etc.).
   - **sqlite_sequence**: Guarda la secuencia de incremento automático para las tablas.
   - **ventas**: Registra las ventas realizadas (fecha, total, cliente, etc.).
   - **proveedores**: Información sobre los proveedores.
   - **compras**: Registra las compras realizadas, junto con el proveedor y el producto.
   - **descuentos**: Descuentos aplicados a productos específicos.
   - **categorias**: Categorías de productos (Maquillaje, Cuidado Facial, etc.).
   - **clientes**: Información sobre los clientes.
   - **detalles_venta**: Detalles de cada venta (productos, cantidades y precios).

2. **Proceso de configuración:**
   - El script solicita al usuario ingresar el número de categorías que desea agregar.
   - Luego, se le pide al usuario ingresar el nombre de cada categoría.
   - Las categorías ingresadas son almacenadas en la tabla `categorias`.
   
3. **Instalación y Ejecución:**
   - **Paso 1:** Clona o descarga el repositorio.
   - **Paso 2:** Asegúrate de tener Python instalado y las bibliotecas necesarias (SQLite3 es parte de la biblioteca estándar de Python, por lo que no necesitas instalarla aparte).
   - **Paso 3:** Ejecuta el script `configurar_base_datos.py` con el siguiente comando:
   
     ```bash
     python3 configurar_base_datos.py
     ```

4. **Resultado:**
   - El script creará la base de datos `inventario.db` con las tablas necesarias.
   - Luego, te permitirá ingresar las categorías que deseas agregar a tu sistema.

### Ejemplo de Ejecución:

Supongamos que se ejecuta el script y el usuario desea ingresar 3 categorías. La salida del script podría ser la siguiente:

```bash
Ingrese el número de categorías que desea agregar: 3
Ingrese el nombre de la categoría 1: Maquillaje
Ingrese el nombre de la categoría 2: Cuidado Facial
Ingrese el nombre de la categoría 3: Cuidado Capilar
```
El proceso es interactivo y fácil de usar, lo que permite al usuario personalizar la base de datos de acuerdo a sus necesidades.
---
Contribuciones

Si deseas contribuir a este proyecto, puedes realizar un fork y hacer tus cambios. Luego, abre un pull request con tus mejoras o correcciones.


---
```
Este proyecto fue creado por IngEliab y está en constante desarrollo.

Este README.md cubre las principales características, librerías utilizadas,
instrucciones de instalación y mejoras futuras. Puedes agregar más detalles según lo necesites.
```
