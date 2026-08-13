# Manual Técnico — Avance

## Instalación de Ubuntu y Comandos Iniciales

**Universidad de San Carlos de Guatemala**
**Ingeniería en Ciencias y Sistemas**
**Curso:** Prácticas Iniciales
**Estudiante:** Cristian Fuentes

---

# 1. Instalación de Ubuntu

Para esta práctica se utilizó **virtualización mediante Oracle VirtualBox**, manteniendo Windows como sistema operativo anfitrión y Ubuntu como sistema invitado.

La máquina virtual fue configurada con:

* **RAM:** 4096 MB
* **Procesadores:** 2
* **Disco virtual:** 40 GB
* **EFI:** Habilitado

El procedimiento general fue:

1. Instalar Oracle VirtualBox.
2. Descargar la imagen ISO de Ubuntu.
3. Crear una nueva máquina virtual.
4. Asignar memoria RAM, procesadores y almacenamiento.
5. Seleccionar la ISO de Ubuntu.
6. Iniciar la máquina virtual.
7. Completar la instalación de Ubuntu.
8. Reiniciar y comprobar que el sistema funcione correctamente.

> [![Captura-de-pantalla-2026-08-13-162539.png](https://i.postimg.cc/4xGbLmsw/Captura-de-pantalla-2026-08-13-162539.png)](https://postimg.cc/RNPHqC3n)

---

# 2. Comandos de navegación

## `pwd`

Muestra la ruta del directorio actual.

### Sintaxis

```bash
pwd
```

### Ejemplo

```bash
pwd
```

Resultado:

```text
/home/crismo
```

---

## `cd`

Permite cambiar de directorio.

### Sintaxis

```bash
cd directorio
```

### Ejemplos

Entrar a una carpeta:

```bash
cd Documentos
```

Regresar un nivel:

```bash
cd ..
```

Regresar al directorio personal:

```bash
cd ~
```

> [![Captura-de-pantalla-2026-08-13-163921.png](https://i.postimg.cc/sfcVQL1G/Captura-de-pantalla-2026-08-13-163921.png)](https://postimg.cc/JtswSPNR)

---

# 3. Listado y creación de directorios

## `ls`

Muestra los archivos y directorios existentes.

### Sintaxis

```bash
ls
```

### Variaciones

Listado detallado:

```bash
ls -l
```

Mostrar archivos ocultos:

```bash
ls -a
```

Combinar ambas opciones:

```bash
ls -la
```

> [![Captura-de-pantalla-2026-08-13-164417.png](https://i.postimg.cc/TPV88yD5/Captura-de-pantalla-2026-08-13-164417.png)](https://postimg.cc/3yxfmx93)

---

## `mkdir`

Permite crear directorios.

### Sintaxis

```bash
mkdir nombre
```

### Ejemplo

```bash
mkdir PracticaLinux
```

### Directorios anidados

```bash
mkdir -p PracticaLinux/documentos/copias
```

La opción `-p` permite crear varios niveles de directorios.

> [![Captura-de-pantalla-2026-08-13-164830.png](https://i.postimg.cc/J0yPLgFW/Captura-de-pantalla-2026-08-13-164830.png)](https://postimg.cc/m1sQ3dRd)

---

# 4. Manipulación de archivos

## `cp`

Permite copiar archivos.

### Sintaxis

```bash
cp origen destino
```

### Ejemplo

```bash
cp archivo.txt copia.txt
```

Para copiar carpetas completas:

```bash
cp -r carpeta carpeta_copia
```
> [![Captura-de-pantalla-2026-08-13-165751.png](https://i.postimg.cc/ydCZdGWz/Captura-de-pantalla-2026-08-13-165751.png)](https://postimg.cc/jWv53Zz8)
---

## `mv`

Permite mover o renombrar archivos.

### Sintaxis

```bash
mv origen destino
```

### Mover un archivo

```bash
mv archivo.txt Documentos/
```

### Renombrar un archivo

```bash
mv archivo.txt archivo_nuevo.txt
```

---

## `rm`

Permite eliminar archivos.

### Sintaxis

```bash
rm archivo
```

### Ejemplo

```bash
rm archivo.txt
```

Solicitar confirmación:

```bash
rm -i archivo.txt
```

Eliminar una carpeta y su contenido:

```bash
rm -r carpeta
```

> **Precaución:** Se debe verificar el nombre del archivo antes de utilizar `rm`.

---

## `rmdir`

Permite eliminar directorios vacíos.

### Sintaxis

```bash
rmdir directorio
```

### Ejemplo

```bash
mkdir Temporal
rmdir Temporal
```

> [![Captura-de-pantalla-2026-08-13-173049.png](https://i.postimg.cc/1XktCn69/Captura-de-pantalla-2026-08-13-173049.png)](https://postimg.cc/1VKs4zJT)

---

# 5. Ejemplo práctico

Para practicar los comandos anteriores se creó un directorio de prueba:

```bash
mkdir ManualLinux
cd ManualLinux
pwd
```

Posteriormente:

```bash
mkdir -p Practica/documentos
ls -la
```

Se creó un archivo de prueba:

```bash
echo "Archivo de prueba" > archivo.txt
```

Se realizó una copia:

```bash
cp archivo.txt copia.txt
```

Se renombró:

```bash
mv copia.txt archivo_nuevo.txt
```

Se eliminó el archivo original:

```bash
rm archivo.txt
```

Finalmente se creó y eliminó una carpeta vacía:

```bash
mkdir Temporal
rmdir Temporal
```

---

# 6. Conclusión

La virtualización mediante Oracle VirtualBox permitió utilizar Ubuntu sin eliminar Windows.

Los comandos `pwd`, `cd`, `ls`, `mkdir`, `cp`, `mv`, `rm` y `rmdir` permiten realizar operaciones básicas de navegación y administración de archivos y directorios desde la terminal de Linux.
