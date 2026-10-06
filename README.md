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
## Descripción de cada una de las relaciones definidas. Descripción con detalle de la cardinalidad de cada relación.
### Vivero
1. Id_Vivero: Número de identificación exclusivo de cada vivero.
2. Nombre: Nombre del vivero.
3. Longitud: Longitud de la ubicación del vivero.
4. Latitud: Latitud de la ubicación del vivero.
#### Relaciones Vivero
![Relaciones Viveros](https://github.com/FranciOrtiz/ADBD-Pr-ctica-2/blob/5b842e1ace295961b06975d4a91aa2a8fb5bc5ce/Im%C3%A1genes/Relaciones_Viveros.png)

#### Descripción de la relación y cardinalidad
A un Vivero se le ha destinado un Puesto de trabajo y está dividido en distintas zonas.
Puesto que un Vivero puede albergar múltiples puestos de trabajos, al igual que estar dividido en múltiples zonas, la relación de la tabla Vivero tiene una cardinalidad de Uno a Muchos (1:M) con las tablas de Puesto y Zonas.

### Puesto:
1. Id_Puesto: Número identificativo del puesto.
2. Cargo: Designación del puesto.
3. Fecha_Inicio: Fecha de inicio del trabajo.
4. Fecha_Fin: Fecha de la conclusión del trabajo.
#### Relaciones Puesto
![Relaciones Puesto](https://github.com/FranciOrtiz/ADBD-Pr-ctica-2/blob/5601e0936d59c1b1dc3d88b1c664120d8dd8674e/Im%C3%A1genes/Relaciones%20Puesto.png)

#### Descripción de la relación y cardinalidad
El Puesto con cargo específico y comprendido entre ambas fechas se le ha sido asignado un Empleado destinado al Vivero y que desempeña distintas Tareas.
Solo un Empleado puede ocupar un Puesto, lo que convierte la relación entre la tabla Puesto y Empleado de tipo Uno a Uno (1:1).
Un Empleado puede desempeñar múltiples Tareas, por lo que la relación entre estas tablas es de tipo Uno a Muchos (1:M).
Como se especificó antes, múltiples Empleados pueden ser asignados a un mismo Vivero, dejando una cardinalidad de Uno a Muchos (M:1).

### Tareas:
1. Id_Tarea: Identificación de la tarea.
2. Tiempo_en_realizar: Tiempo estimado para completar la tarea.
3. Nombre_tarea: Nombre específico de la tarea a realizar.
4. Material_necesario: Recurso(s) necesario(s) para poder llevar a cabo la tarea.
#### Relaciones Tareas
![Relaciones Tareas](https://github.com/FranciOrtiz/ADBD-Pr-ctica-2/blob/5601e0936d59c1b1dc3d88b1c664120d8dd8674e/Im%C3%A1genes/Relaciones%20Tareas.png)

#### Descripción de la relación y cardinalidad
Las Tareas se desempeñan en el Puesto de trabajo y se realizan en las distintas Zonas del Vivero en base a la Fecha de inicio y el Tiempo en llevarlas a cabo.
Igual que se especificó antes, un Empleado puede realizar múltiples Tareas, dejando una cardinalidad de Uno a Muchos(M:1).
Por otro lado, en base al Tiempo y la Fecha de las Tareas, se pueden tener múltiples Tareas en múltiples Zonas del Vivero, dejándonos una relación Muchos a Muchos(M:M).

### Zonas
1. Id_Zona: Número de identificación de la zona del vivero.
2. Nombre: Denominación específica de la zona.
3. Longitud: Longitud geográfica de la zona.
4. Latitud: Latitud geográfica de la zona.
#### Relaciones Zonas
![Relaciones Zonas](https://github.com/FranciOrtiz/ADBD-Pr-ctica-2/blob/5601e0936d59c1b1dc3d88b1c664120d8dd8674e/Im%C3%A1genes/Relaciones%20Zonas.png)

#### Descripción de la relación y cardinalidad
En la Zona perteneciente al Vivero, se realizan las Tareas y se tienen distintas cantidades de los Productos.
Como se especificó al principio, un Vivero está comprendido por multitud de Zonas, poniendo así una cardinalidad de Uno a Muchos(M:1).
Al igual que antes, múltiples Zonas pueden estar involucradas en múltiples Tareas, dejando así la cardinalidad de Muchos a Muchos(M:M).
Las distintas Zonas de un Vivero pueden tener muchos Productos y en distintas cantidades, de ahí que podamos considerarlo una cardinalidad de Muchos a Muchos(M:M).

### Productos
1. Id_producto: Número identificativo del producto.
2. Tipo: Categoría a la que pertenece el producto.
3. Nombre: Nombre del producto.
4. Precio: Precio de venta al público del producto.
#### Relaciones Productos
![Relaciones Productos](https://github.com/FranciOrtiz/ADBD-Pr-ctica-2/blob/5601e0936d59c1b1dc3d88b1c664120d8dd8674e/Im%C3%A1genes/Relaciones%20Producto.png)

#### Descripción de la relación y cardinalidad
Los distintos Productos se tienen en alguna de las Zonas del Vivero.
Dicho pues, la relación entre los Productos y las Zonas de un Vivero son de cardinalidad Muchos a Muchos(M:M).

### Empleados
1. DNI_empleado: DNI específico de cada empleado.
2. Nombre: Nombre completo de cada empleado.
3. Fecha_de_Nacimiento: Fecha de nacimiento de cada empleado.
4. Fecha_de_Contratación: Fecha de inicio del contrato de cada empleado.
#### Relaciones Empleados
![Relaciones Empleados](https://github.com/FranciOrtiz/ADBD-Pr-ctica-2/blob/5601e0936d59c1b1dc3d88b1c664120d8dd8674e/Im%C3%A1genes/Relaciones%20Empleados.png)

#### Descripción de la relación y cardinalidad
Los Empleados gestionan los pedidos y son asignados a los Puestos de trabajo.
Como ya se ha especificado, un Empleado solo puede ser asignado a un Puesto de trabajo, dandonos una cardinalidad de Uno a Uno(1:1).
Por otro lado, un sólo Empleado debería de ser capaz de realizar múltiples pedidos, obteniendo así una cardinalidad de Uno a Muchos(1:M).

### Pedidos:
1. Id_Pedidos: Identificador unitario del pedido.
2. Importe_total: Precio total del producto.
3. Número_de_producto: Cantidad de productos englobados dentro del pedido.
#### Relaciones Pedidos
![Relaciones Pedidos](https://github.com/FranciOrtiz/ADBD-Pr-ctica-2/blob/5601e0936d59c1b1dc3d88b1c664120d8dd8674e/Im%C3%A1genes/Relaciones%20Pedidos.png)

#### Descripción de la relación y cardinalidad
Los Pedidos son gestionados por los Empleados y los realizan los Clientes de Tajinaste Plus.
Cómo se estableció en el anterior apartado, un solo Empleado puede llevar a cabo múltiples Pedidos, por lo que podemos denominar esta cardinalidad de Uno a Muchos(M:1)
En cambio, un solo Cliente de Tajinaste Plus puede realizar múltiples Pedidos, obteniendo así también una cardinalidad de Uno a Muchos(M:1).

### Cliente Tajinaste Plus
1. DNI_cliente: DNI del cliente.
2. Nombre: Nombre completo del cliente.
3. Fecha_de_nacimiento: Fecha de nacimiento del cliente.
#### Relaciones Clientes Tajinaste Plus
![Relaciones Cliente Plus](https://github.com/FranciOrtiz/ADBD-Pr-ctica-2/blob/5601e0936d59c1b1dc3d88b1c664120d8dd8674e/Im%C3%A1genes/Relaciones%20Clientes%20Plus.png)

#### Descripción de la relación y cardinalidad
Un Cliente de Tajinaste Plus realiza los pedidos y recibe Bonificaciones por ello.
Dicho anteriormente, un solo Cliente Plus puede realizar múltiples Pedidos, generando la cardinalidad de Uno a Muchos(1:M).
Luego, un Cliente Plus obtendrá una Bonificación que le durará durante una franja de tiempo específica. De este modo determinamos que se trata de una relación Uno a Uno(1:1).

### Bonificación
1. Total_de_Bonificación_Dados: Porcentaje total de bonificación para futuras compras del socio. 
2. Año: Año en el que bono está activo.
3. Mes: Mes en el que el bono está activo.
#### Relaciones Bonificación
![Relaciones Bonificación](https://github.com/FranciOrtiz/ADBD-Pr-ctica-2/blob/5601e0936d59c1b1dc3d88b1c664120d8dd8674e/Im%C3%A1genes/Relaciones%20Bonificaci%C3%B3n.png)

#### Descripción de la relación y cardinalidad
Las Bonificaciones son obtenidas por los Clientes de Tajinaste Plus.
Un Cliente Plus solo obtendrá una Bonificación a la vez, generando la cardinalidad de Uno a Uno(1:1).
