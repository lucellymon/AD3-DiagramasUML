# AD3-DiagramasUML
Este proyecto corresponde a la Actividad 3 de la asignatura *Entornos de Desarrollo*.  
El objetivo principal es diseñar, mediante el lenguaje UML, un sistema para la gestión de jugadores y equipos dentro de un torneo.  

Para ello, se han elaborado diagramas de **casos de uso** y **clases**, que permiten representar tanto las funcionalidades del sistema como su estructura interna. El diseño incluye la intervención de distintos actores (administrador, usuario y sistema) y contempla procesos como el registro de equipos, la incorporación de jugadores y la consulta de información.
## 1. Diagrama de Casos de Uso

![Diagrama de Casos de Uso](useCaseDiagram1.png)
### Descripción de los casos de uso:

- **Registrar equipo**: El administrador introduce un nuevo equipo en el sistema.  
- **Añadir jugador**: El administrador añade un jugador a un equipo ya existente.  
- **Consultar jugadores**: El usuario consulta información sobre jugadores registrados.  
- **Consultar equipos**: El usuario accede a información de los equipos disponibles.  
- **Verificación del sistema**: El sistema comprueba si el equipo o jugador ya existen antes de registrar.
- ## 2. Diagrama de Clases UML

![Diagrama de Clases UML]()

### Explicación de la estructura:

El sistema está estructurado en torno a las siguientes clases:
-**Administrador**:
- **Gestores**: `GestorEquipos`, `GestorJugadores`. 
- **Entidades**: Clases `Equipo`, `Jugador`, `Usuario`,`consultas`.
- **Sistema**: Clase que orquesta el flujo entre gestores y operaciones.

Las relaciones incluyen:
- Asociación entre `Equipo` y `Jugador` (un equipo tiene muchos jugadores).
- Asociación entre `Usuario` y operaciones de consulta.
- Dependencias entre gestores y entidades.

---

## 3. Justificación del Diseño

Se eligió una arquitectura modular basada en gestores para separar responsabilidades. Esto mejora la escalabilidad, el mantenimiento y la legibilidad del código.
-**Administrador**:
- **Gestores**: Encapsulan la lógica de cada dominio (equipos, jugadores, etc.).
- **Validación**: La lógica del sistema valida previamente la existencia de entidades para evitar duplicados.
- **Consultas separadas**: Se ofrece al usuario acceso a información sin alterar los datos del sistema.

Esta organización favorece una separación clara entre el backend (gestores y validaciones) y las funcionalidades del usuario.

---

## 4. Conclusiones

Durante la realización de esta actividad:

- Aprendí a modelar un sistema con múltiples actores y responsabilidades claras.
- Comprendí la importancia de los diagramas UML para planificar antes de codificar.






