# Documentación SSH: Creación y Edición de Archivos

Este documento proporciona una guía paso a paso para conectarse a una máquina remota via SSH, crear un archivo de texto con el nombre del usuario, y luego agregar información sobre los usuarios conectados a la máquina.

## Pasos

### 1. Conexión SSH

```bash
ssh -p 22 usuario@192.168.0.148
```
![Login en escritorio remoto](https://github.com/Arzeld/examenMQA/blob/main/SSH%2BCommand%20line/login_en_escritorio_remoto.png)

### 2. Navegar al Escritorio

```bash
cd /Escritorio
```

### 3. Crear un Archivo de Texto

```bash
touch nombre.txt
```

### 4. Escribir el Nombre de Usuario en el Archivo

```bash
whoami > nombre.txt
```

### 5. Agregar Información de Usuarios Conectados

```bash
who >> nombre.txt
```
![creacion_archivotxt](https://github.com/Arzeld/examenMQA/blob/main/SSH%2BCommand%20line/creacion_manuelaicart.png)
