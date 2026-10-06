# ADBD-Práctica-2

## Descripción de cada una de las entidades definidas.
### Vivero
Localización de trabajo y tratado de plantas por parte de los trabajadores de la empresa Tajinaste S.A.
### Puesto
Puesto de trabajo de cada trabajador.
### Tareas
Tareas designadas a los trabajadores en sus respectivos puestos.
### Zonas
Divisiones internas de cada vivero.
### Productos
Inventario disponible a venta.
### Empleados
Trabajadores de la empresa Tajinaste S.A.
### Pedidos
Encargos de productos gestionados por los empleados para los clientes.
### Cliente Tajinaste Plus
Clientes fidelizados al programa de clientes de la empresa.
### Bonificación
Bonuses que obtienen los socios del programa de fidelización de la empresa.

## Descripción y ejemplos ilustrativos del dominio de cada uno de los atributos de las entidades y de las relaciones.
### Vivero
1. Id_Vivero: Número de identificación exclusivo de cada vivero.
2. Nombre: Nombre del vivero.
3. Longitud: Longitud de la ubicación del vivero.
4. Latitud: Latitud de la ubicación del vivero.
### Puesto:
1. Id_Puesto: Número identificativo del puesto.
2. Cargo: Designación del puesto.
3. Fecha_Inicio: Fecha de inicio del trabajo.
4. Fecha_Fin: Fecha de la conclusión del trabajo.
### Tareas:
1. Id_Tarea: Identificación de la tarea.
2. Tiempo_en_realizar: Tiempo estimado para completar la tarea.
3. Nombre_tarea: Nombre específico de la tarea a realizar.
4. Material_necesario: Recurso(s) necesario(s) para poder llevar a cabo la tarea.
### Zonas
1. Id_Zona: Número de identificación de la zona del vivero.
2. Nombre: Denominación específica de la zona.
3. Longitud: Longitud geográfica de la zona.
4. Latitud: Latitud geográfica de la zona.
### Productos
1. Id_producto: Número identificativo del producto.
2. Tipo: Categoría a la que pertenece el producto.
3. Nombre: Nombre del producto.
4. Precio: Precio de venta al público del producto.
### Empleados
1. DNI_empleado: DNI específico de cada empleado.
2. Nombre: Nombre completo de cada empleado.
3. Fecha_de_Nacimiento: Fecha de nacimiento de cada empleado.
4. Fecha_de_Contratación: Fecha de inicio del contrato de cada empleado.
### Pedidos:
1. Id_Pedidos: Identificador unitario del pedido.
2. Importe_total: Precio total del producto.
3. Número_de_producto: Cantidad de productos englobados dentro del pedido.
### Cliente Tajinaste Plus
1. DNI_cliente: DNI del cliente.
2. Nombre: Nombre completo del cliente.
3. Fecha_de_nacimiento: Fecha de nacimiento del cliente.
### Bonificación
1. Total_de_Bonificación_Dados: Porcentaje total de bonificación para futuras compras del socio. 
2. Año: Año en el que bono está activo.
3. Mes: Mes en el que el bono está activo.

## Descripción de cada una de las relaciones definidas. Describa con detalle la cardinalidad de cada relación.
