# Propuesta TP DSW

## Grupo
### Integrantes
* 54617 - Marino, Eduardo
* 55197 - Requelme, Candela M
* 54720 - Lucca, Liam Santiago

### Repositorios
* [diseño](https://app.diagrams.net/#G1eFO_b5KQ9T8M1xZn47CeNbCgubCR8u94)
* [frontend app](https://github.com/liamlucca/cineweb-frontend)
* [backend app](https://github.com/EduardoMarino73/TP-BackEnd)
*Nota*: si utiliza un monorepo indicar un solo link con fullstack app.

### Pull requests
* Frontend: https://github.com/liamlucca/cineweb-frontend/pull/2
* Backend: https://github.com/EduardoMarino73/TP-BackEnd/pull/7

## Tema
### Descripción
Sistema de gestión de series y películas, donde el usuario pueda subir y eliminar audiovisuales de su autoría, mirarlos, valorarlos con "Me gusta" / "No me gusta" y guardarlos para "Ver más tarde". Además, un usuario puede denunciar un audiovisual seleccionando un motivo de un catálogo; cuando un audiovisual acumula 3 denuncias se abre un caso, que el dueño del contenido puede apelar. Luego, un administrador se encarga de revisar la apelación: si la rechaza, el contenido queda suspendido.

### Modelo
https://drive.google.com/file/d/16af4iugaq9fV1vGB6cZFufNQbk7T6Gk6/view?usp=sharing

## Alcance Funcional 

### Alcance Mínimo

Regularidad:
|Req|Detalle|
|:-|:-|
|CRUD simple|1. CRUD Audiovisual: películas y series (con temporadas y episodios); alta con video, miniatura y duración, consulta, edición y borrado lógico, solo por quien lo subió<br>2. CRUD Tipo Reporte: catálogo de motivos de denuncia administrado por los administradores<br>3. CRUD Denuncia: alta por el espectador (un motivo del catálogo + detalle opcional, obligatorio para "Otro"); consulta, filtro y cambio de estado por el administrador a través de la apelación<br>4. CRUD Usuario: registro, ingreso, consulta y edición del perfil, activación y desactivación de cuentas|
|CRUD dependiente|1. CRUD Administrador {depende de} CRUD Usuario<br>2. CRUD Espectador {depende de} CRUD Usuario<br>3. CRUD Apelación {depende de} CRUD Denuncia: alta y retiro por el dueño del contenido, consulta y resolución (aceptar / rechazar) por el administrador|
|Listado<br>+<br>detalle| 1. Listado de contenidos audiovisuales filtrado por categoría, tipo (película / serie) y coincidencia parcial del título => detalle del audiovisual con el usuario que lo subió y sus valoraciones<br> 2. Listado de denuncias (casos de moderación) filtrado por número de caso, estado y motivo; muestra el nombre del usuario denunciado, el nombre del audiovisual y los motivos agrupados => detalle muestra cada denuncia con su motivo y detalle, y la apelación|
|CUU/Epic|1. Agregar a "Ver Más Tarde" un Audiovisual<br>2. Buscar los datos de una Denuncia<br>3. Hacer valoración "Me gusta" "No Me gusta"|


Adicionales para Aprobación<br>

|Req|Detalle|
|:-|:-|
|CRUD |1. CRUD Audiovisual<br>2. CRUD Tipo Reporte<br>3. CRUD Denuncia<br>4. CRUD Usuario<br>5. CRUD Administrador<br>6. CRUD Espectador<br>7. CRUD Apelación<br>8. CRUD VER MAS TARDE<br>9. CRUD Reseña|
|CUU/Epic|1. Agregar a “Ver Más Tarde” un Audiovisual<br>2. Buscar los datos de una Denuncia<br>3. Hacer valoración “Me gusta” “No Me gusta”|


### Alcance Adicional Voluntario

*Nota*: El Alcance Adicional Voluntario es opcional, pero ayuda a que la funcionalidad del sistema esté completa y será considerado en la nota en función de su complejidad y esfuerzo.

|Req|Detalle|
|:-|:-|
|Listados |1. "Denuncias sobre mi contenido": el espectador ve los casos abiertos sobre los audiovisuales que subió, con su estado y el de su apelación|
|CUU/Epic|1. Retirar una apelación que todavía no fue revisada (el caso vuelve a quedar abierto para apelar)|
|Otros|1. Miniatura y duración de cada video obtenidas en el navegador al subirlo; portada opcional para las series<br>2. Borrado lógico de películas, series, temporadas y episodios|

### Notas técnicas
* La persistencia del backend usa el patrón Repository con `mysql2` y SQL, en lugar de un ORM (decisión del equipo).
