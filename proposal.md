# Propuesta TP DSW

## Grupo
### Integrantes
* 54617 - Marino, Eduardo
* 55197 - Requelme, Candela M
* 54720 - Lucca, Liam Santiago

### Repositorios
* [frontend app](http://hyperlinkToGihubOrGitlab)
* [backend app](http://hyperlinkToGihubOrGitlab)
*Nota*: si utiliza un monorepo indicar un solo link con fullstack app.

## Tema
### Descripción
Sistema de gestión de series y peliculas, donde el usuario pueda subir y eliminar audio-visuales de su autoría. Además, un usuario podría denunciar a otro seleccionando un motivo. Luego, un administrador se encargará de validar esa denuncia. 

### Modelo
https://drive.google.com/file/d/16af4iugaq9fV1vGB6cZFufNQbk7T6Gk6/view?ts=69d6d6cd

## Alcance Funcional 

### Alcance Mínimo

*Nota*: el siguiente es un ejemplo para un grupo de 3 integrantes para un sistema de hotel. El 

Regularidad:
|Req|Detalle|
|:-|:-|
|CRUD simple|1. CRUD Audiovisual<br>2. CRUD Tipo Reporte<br>3. CRUD Denuncia<br>4. CRUD Usuario|
|CRUD dependiente|1. CRUD Administrador {depende de} CRUD Usuario<br>2. CRUD Espectador {depende de} CRUD Usuario<br>3. CRUD Apelación {depende de} CRUD Denuncia|
|Listado<br>+<br>detalle| 1.Listado de contenidos Audiovisuales que tengan cierta categoría deseada o que coincidan parcialmente en nombre con el elemento buscado<br> 2. Listado de datos filtrados por id de denuncia, muestra nombre del usuario reportado, nombre del Audiovisual y los motivos de la misma = > detalle muestra datos denuncia|
|CUU/Epic|1. Agregar a “Ver Más Tarde” un Audiovisual<br>2. Buscar los datos de una Denuncia<br>3. Hacer valoración “Me gusta” “No Me gusta”|


Adicionales para Aprobación
|Req|Detalle|
|:-|:-|
|CRUD |1. CRUD Tipo Habitacion<br>2. CRUD Servicio<br>3. CRUD Localidad<br>4. CRUD Provincia<br>5. CRUD Habitación<br>6. CRUD Empleado<br>7. CRUD Cliente|
|CUU/Epic|1. Reservar una habitación para la estadía<br>2. Realizar el check-in de una reserva<br>3. Realizar el check-out y facturación de estadía y servicios|


### Alcance Adicional Voluntario

*Nota*: El Alcance Adicional Voluntario es opcional, pero ayuda a que la funcionalidad del sistema esté completa y será considerado en la nota en función de su complejidad y esfuerzo.

|Req|Detalle|
|:-|:-|
|Listados |1. Estadía del día filtrado por fecha muestra, cliente, habitaciones y estado <br>2. Reservas filtradas por cliente muestra datos del cliente y de cada reserve fechas, estado cantidad de habitaciones y huespedes|
|CUU/Epic|1. Consumir servicios<br>2. Cancelación de reserva|
|Otros|1. Envío de recordatorio de reserva por email|

