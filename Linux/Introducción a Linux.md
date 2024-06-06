## Comandos básicos

- Acercar ➜ `[CTRL] + [+]`
- Alejar ➜ `[CTRL] + [-]`
- Imprimir directorio de trabajo ➜ `pwd`
- Borrar el terminal ➜ `[CTRL] + [l]`o`clear`
- Asignar un alias ➜ `alias [alias-name]="[command-to-run]"`
- Obtener un archivo ➜ `source [name-of-the-file-to-read-and-execute]`

---
## Comandos de directorios (cd)

- Moverse a un directorio específico ➜ `cd [name-of-your-directory]`
- Moverse al directorio principal ➜ `cd ..`
- Ir al directorio de inicio ➜ `cd`o`cd ~`
- Moverse al último directorio en el que estaba ➜ `cd -`

---
## Comando de listas (ls)

- Enumerar todos los archivos y directorios visibles ➜ `ls`
- Enumerar todos los archivos y directorios (incluya archivos ocultos) ➜ `ls -a`
- Formato de lista larga ➜ `ls -l`
- Formato legible por humanos ➜ `ls -lh`
- Combinando argumentos: formato legible por humanos + archivos ocultos ➜ `ls -lah`
- Obtén más información sobre el comando ls ➜ `man ls`

---
## Comandos de Búsquedas

- Busque el binario de un programa ➜ `which [name-of-the-program]`
- Busque el manual binario, fuente y de usuario de un programa ➜ `whereis [name-of-the-program]
- Busque archivos y directorios por nombre ➜  `find [path-to-search] -iname [name-of-the-file-you-want-to-search]`
- Obtén más información sobre el comando de búsqueda ➜ `man find`
- Obtén una breve descripción de un comando ➜ `whatis [command-name]`

---
## Historial de Comandos

- Obtén comandos anteriores (uno por uno) ➜ Use `Up Arrow key`⬆️ para navegar por su historial
- Obtén comandos anteriores (lista completa) ➜ `history`.
- Repite los comandos del historial (comando bang) ➜ `history`➜`![number-of-the-command-to-repeat]`
- Repite el último comando (comando bang-bang) ➜ `!!`

---
## Comandos para Trabajar con Archivos y Directorios

- Crear un nuevo archivo (sin abrirlo) ➜ `touch [name-of-your-file]`
- Crear un nuevo archivo usando un editor de texto ➜ `vim [name-of-your-file]`o`nano [name-of-your-file]`
- Copiar un archivo ➜ `cp [source-path-of-your-file] [destination-path-for-your-file]`
- Crear un nuevo directorio ➜ `mkdir [new-directory-name]`
- Eliminar un directorio vacío ➜ `rmdir [name-of-the-directory-you-want-to-remove]`
- Comando de eliminar (rm)
    - Eliminar un archivo ➜ `rm [name-of-your-file]`
    - Eliminar un directorio de forma recursiva (usar con precaución) ➜ `rm -rf [name-of-your-directory]`
- Comando de concatenar (cat)
    - Ver un solo archivo ➜ `cat [name-of-your-file]`
    - Ver un solo archivo que incluye los números de línea ➜ `cat -n [name-of-your-file]`
    - Copiar el contenido de un archivo a otro archivo ➜ `cat [filename-whose-contents-is-to-be-copied] > [destination-filename]`
    - Más información sobre el comando cat ➜ `man cat`
- Comando de mover (mv)
    - Mover un archivo ➜ `mv [source-path-of-your-file] [destination-path-for-your-file]`
    - Cambiar el nombre de un archivo ➜ `mv [name-of-your-file] [new name-of-your-file]`

---
## Buscar con Grep

- Buscar una cadena dentro de un archivo ➜ `grep [term-to-search] [source-file-to-search]`
- Búsqueda que no distingue entre mayúsculas y minúsculas dentro de un archivo ➜ `grep -i [term-to-search] [source-file-to-search]`
- Buscar líneas que no coincidan dentro de un archivo ➜ `grep -v [term-to-search] [source-file-to-search]`
- Búsqueda recursiva dentro de un directorio ➜ `grep -r [term-to-search] [path-to-directory-to-search]`
- Varias búsquedas dentro de un archivo ➜ `grep -E "[first-term-to-search|second-term-to-search]" [source-file-to-search]`
- Contar los resultados de la búsqueda ➜ `grep -c [term-to-search] [source-file-to-search]`
- Mostrar el nombre de los archivos coincidentes ➜ `grep -l [term-to-search] [matching-files-to-search]`
- Más información sobre grep ➜ `man grep`

---
## Pipelines o Tuberías

- Comandos en tuberías ➜ `[command 1] | [command 2] | [command n]`
- Canalización de resultados de búsqueda filtrados en un nuevo archivo ➜ `ls | grep [term-to-filter] | cat > [path-to-new-file]/[name-for-new-file]`
- Buscar en el historial de comandos ➜ `history | grep "[term-to-search]"`

---
## Permisos: Cambiar el comando de bits del modo de archivo (chmod)

- Agregar permiso de ejecución a todos ➜ `chmod a+x [name-of-the-file]`o`chmod +x [name-of-the-file]`
- Quitar el permiso de ejecución a todos ➜ `chmod a-x [name-of-the-file]`o`chmod -x [name-of-the-file]`
- Agregar permiso de ejecución al propietario ➜ `chmod u+x [name-of-the-file]`
- Eliminar el permiso de escritura a otros usuarios ➜ `chmod o-w [name-of-the-file]`
- Agregar permiso de lectura al grupo ➜ `chmod g+r [name-of-the-file]`
- Quitar el permiso de escritura y lectura a todos ➜ `chmod a-wr [name-of-the-file]`
- Quitar el permiso de escritura y lectura a todos para todos los archivos en el directorio actual ➜ `chmod a-wr *.*`

---
## Comandos para trabajar con grupos

- Enumerar todos los grupos disponibles ➜ `getent group`
- Enumerar todos los grupos a los que está asignada mi cuenta ➜ `groups`
- Buscar un grupo específico (usando tuberías) ➜ `getent group | grep [group-name-to-search]`
- Crear un nuevo grupo ➜ `sudo groupadd [name-for-the-new-group]`
- Agregar un usuario existente a un grupo secundario ➜ `usermod -a -G [group-you-want-to-add-the-user-to] [user-name-to-add]`

---
## Propiedades: Cambiar el propietario y el grupo del archivo (chown)

- Cambiar la propiedad del usuario para un archivo ➜ `sudo chown [new-owner-name] [file-to-change-ownership]`
- Cambiar la propiedad del usuario para varios archivos ➜ `sudo chown [new-owner-name] [file-1-to-change-ownership] [file-n-to-change-ownership]`
- Cambiar la propiedad del usuario para un directorio ➜ `sudo chown [new-owner-name] [directory-to-change-ownership]`
- Cambiar recursivamente la propiedad del usuario para un directorio y todos sus archivos ➜ `sudo chown -R [new-owner-name] [directory-to-change-ownership]`
- Cambiar la propiedad del grupo para un archivo ➜ `sudo chown :[new-group-name] [file-to-change-ownership]`
- Cambiar la propiedad de usuario y grupo de un archivo ➜ `sudo chown [new-owner-name]:[new-group-name] [file-to-change-ownership]`

---
## Atajos de Teclado

- Buscar en tu historial de búsqueda ➜ `[CTRL] + r`. Luego escriba algunos caracteres para encontrar su comando
- Pegar líneas anteriores ➜ `[CTRL] + p`
- Mover el cursor al principio de la línea. ➜`[CTRL] + a`
- Mover el cursor al final de la línea. ➜`[CTRL] + e`
- Mover el cursor un carácter hacia adelante. ➜`[CTRL] + f`
- Mover el cursor un carácter hacia atrás. ➜`[CTRL] + b`
- Borrar la línea completa. ➜`[CTRL] + u`
- Borrar la última palabra escrita. ➜`[CTRL] + w`

---
## Comandos para trabajar con archivos largos

- Imprimir las últimas líneas de un archivo ➜ `tail [name-of-the-file]`
- Imprimir las últimas n líneas para un archivo ➜ `tail -n [number-of-lines] [name-of-the-file]`
- Imprimir las primeras líneas de un archivo ➜ `head [name-of-the-file]`
- Imprimir las primeras n líneas de un archivo ➜ `head -n [number-of-lines] [name-of-the-file]`
- Ojear un archivo ➜ `less [name-of-the-file]`

---
## Control de logs

` journalctl | grep TEXTO_A_BUSCAR_PARA_FILTRAR `

---
## **Para Contar el Numero de Procesos:**

 ` ps -Af | grep mysql | grep -v "grep" | wc -l `