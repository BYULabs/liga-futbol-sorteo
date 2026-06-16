# LigaFootballSorteo

Proyecto simple en Java para realizar el sorteo de una etapa de una liga de fútbol (octavos, cuartos, semifinales). Permite ingresar los nombres de los equipos por consola y genera los emparejamientos aleatorios para la etapa seleccionada.

## Requisitos

- Java 8 o superior (recomendado Java 11+).
- No se usa un sistema de build (Maven/Gradle) en el repositorio; las instrucciones abajo usan javac/java.

## Estructura del proyecto

- LigaFootballSorteo/
  - src/com/liga/
    - Main.java       -> Programa principal (entrada por consola)
    - Equipo.java     -> Objeto que representa un equipo
    - Partido.java    -> Objeto que representa un partido entre dos equipos
    - Sorteo.java     -> Lógica para emparejar equipos aleatoriamente

## Compilar y ejecutar (línea de comandos)

Desde la raíz del repositorio, ejecuta:

1) Compilar todos los archivos Java y colocar las clases compiladas en el directorio `out`:

```bash
javac -d out LigaFootballSorteo/src/com/liga/*.java
```

2) Ejecutar la aplicación:

```bash
java -cp out com.liga.Main
```

La aplicación pedirá por consola la etapa ("octavos", "cuartos" o "semifinales") y luego los nombres de los equipos según la cantidad requerida. Finalmente imprimirá la lista de partidos generada aleatoriamente.

## Ejemplo de ejecución

- Entrada (ejemplo):
  - etapa: `octavos`
  - 16 nombres de equipos

- Salida (ejemplo):

```
Bienvenido al Sorteo de la Liga de Fútbol
Etapas disponibles: octavos, cuartos, semifinales
Ingrese la etapa: octavos
Ingrese el nombre del equipo 1: Equipo A
...

Partidos para la etapa de octavos:
Equipo A vs Equipo B
Equipo C vs Equipo D
...
```

## Notas y posibles mejoras

- Añadir un sistema de build (Maven o Gradle) para facilitar compilación, pruebas y empaquetado.
- Añadir validaciones de entrada (evitar nombres vacíos, validar número de equipos, evitar duplicados).
- Añadir pruebas unitarias para la lógica de sorteo.
- Mejorar la lógica de sorteo si se requieren restricciones (por ejemplo evitar enfrentamientos de la misma región o cabeza de serie).
- Considerar exponer la funcionalidad mediante una interfaz web o REST para uso más sencillo.

## Contribuciones

Las contribuciones son bienvenidas. Abre un issue o un pull request con tus propuestas.

## Licencia

No se ha especificado una licencia para este repositorio. Si deseas que el proyecto sea reutilizable públicamente, añade un archivo `LICENSE` con la licencia deseada (por ejemplo MIT, Apache-2.0, etc.).
