# Documentación Apache2 Web Server: Setup y configuración

# Starting Apache2 Service

### Comprobar el estado de Apache2 service:

```bash
systemctl status apache2
```

## Pasos

### 1. Crear y editar index.html

1. Creando un nuevo directorio para la web y otorgar permisos:

```bash
mkdir /var/www/examenMQA
chmod 777 /var/www/examenMQA
```

![Creación nuevo directorio](https://github.com/Arzeld/examenMQA/blob/main/Virtualhost/Images/(1)%20inicio_apache2.png)

![Permisos al nuevo directorio y creción indexhtml](https://github.com/Arzeld/examenMQA/blob/main/Virtualhost/Images/(2)%20creacion_index_html.png)

2. Usar el editor nano para crear y editar el archivo index.html:

```bash
nano /var/www/examenMQA/index.html
```

![Contenido indexhtml](https://github.com/Arzeld/examenMQA/blob/main/Virtualhost/Images/(3)%20contenido_index.png)

```html
<!DOCTYPE html>
<html>
  <head>
      <title>ExamenDAW!</title>
  </head>
  <body>
      <h1>Manuel Querol Aicart</h1>
  </body>
</html>
```

### 2. Configurar VirtualHost

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
![creacion_archivotxt](https://github.com/Arzeld/examenMQA/blob/main/SSH%2BCommand%20line/Images/creacion_manuelaicart.png)
