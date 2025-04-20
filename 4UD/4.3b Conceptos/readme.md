# Sistema de Control de Versiones (SCV)
Un **Sistema de Control de Versiones (SCV)** es una herramienta que permite gestionar los cambios realizados en archivos o proyectos a lo largo del tiempo. Estas herramientas son fundamentales para el desarrollo de software, ya que facilitan la colaboración, la recuperación de versiones anteriores y el seguimiento de modificaciones.

## Tipos de Sistemas de Control de Versiones
1. **Sistemas de control de versiones locales**: Guardan versiones en el disco local. Ejemplo: RCS (Revision Control System).
2. **Sistemas de control de versiones centralizados (CVCS)**: Todos los desarrolladores trabajan desde un único repositorio central. Ejemplos: CVS, Subversion (SVN).
3. **Sistemas de control de versiones distribuidos (DVCS)**: Cada desarrollador tiene una copia completa del repositorio, incluyendo su historial. Ejemplos: Git, Mercurial.

## Orígenes de Git
Git fue creado en 2005 por **Linus Torvalds**, el creador de Linux. Surgió como respuesta a la necesidad de un sistema de control de versiones rápido, eficiente y distribuido, después de que el proyecto Linux dejara de usar BitKeeper.

## Características de Git
### 1. Guarda copias instantáneas, no diferencias
Git realiza un registro completo del estado de los archivos en cada confirmación (**commit**). A diferencia de otros sistemas, no almacena sólo las diferencias entre versiones, sino instantáneas completas.

### 2. Casi todas las operaciones son locales
La mayoría de las operaciones (como obtener historial, crear commits, comparar cambios) se ejecutan localmente, sin necesidad de conectarse al servidor remoto. Esto hace que Git sea extremadamente rápido.

### 3. Tiene integridad (Hash SHA-1)
Git utiliza un algoritmo de hashing, **SHA-1**, para garantizar la integridad de los datos. Cada archivo, commit o cambio se identifica mediante un hash único.

### 4. Generalmente sólo añade información
Git evita la pérdida de datos ya que casi siempre añade información en lugar de sobrescribirla. Esto hace que sea muy seguro para el historial de cambios.

## Tres Estados en Git
1. **Modificado (Modified)**: Archivos que han sido cambiados pero no están en el área de preparación (staging area).
2. **Preparado (Staged)**: Cambios que se han añadido al área de preparación y están listos para ser confirmados.
3. **Confirmado (Committed)**: Cambios almacenados de forma permanente en el repositorio local.

## Tres Secciones Principales de un Proyecto Git
1. **Directorio de trabajo (Working Directory)**: Donde los archivos son editados.
2. **Área de preparación (Staging Area)**: Área intermedia donde se añaden los cambios antes de confirmar un commit.
3. **Repositorio (Repository)**: Donde se almacenan las instantáneas confirmadas de manera permanente.

## Equivalente al Índex
El **índex** en Git es equivalente al **Área de preparación (Staging Area)**. Es el espacio donde se añaden los cambios antes de confirmarlos.

## Diferencia entre Archivos Rastreables y No Rastreables
- **Rastreables (Tracked)**: Archivos que Git ya está gestionando y que pueden estar en estados como "modificado", "preparado" o "confirmado".
- **No rastreables (Untracked)**: Archivos que no están siendo gestionados por Git y que no forman parte del repositorio hasta que son añadidos explícitamente.

## HEAD y su Relación con un Nuevo Commit
**HEAD** es un puntero que apunta al commit más reciente en la rama activa. Cuando se crea un nuevo commit:
1. Git guarda los cambios preparados en el repositorio como un nuevo commit.
2. HEAD se actualiza automáticamente para apuntar a este nuevo commit, convirtiéndolo en el estado actual del proyecto.