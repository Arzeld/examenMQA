# Documentación Apache2 Web Server: Setup y configuración
## Starting Apache2 Service
### Comprobar el estado de Apache2 service:

```bash
systemctl status apache2
```

## Pasos
### 1. Crear y editar index.html

1. Crear un nuevo directorio para la web y otorgar permisos:

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
![Contenido indexhtml](https://github.com/Arzeld/examenMQA/blob/main/Virtualhost/Images/(3)%20contenido_index.png)

### 2. Configurar VirtualHost

1. Crear un archivo de configuración virtual host para la web:

```bash
nano /etc/apache2/sites-available/examenMQA.conf
```
![Creación archivo conf](https://github.com/Arzeld/examenMQA/blob/main/Virtualhost/Images/(4)%20creacion_examenMQA_conf.png)

2. Contenido del archivo conf:

```apacheconf
<VirtualHost *:80>
    ServerAdmin querolmanel@gmail.com
    DocumentRoot /var/www/examenMQA
    ServerName daw.ejercicio3.com
</VirtualHost>
```
![Contenido archivo conf](https://github.com/Arzeld/examenMQA/blob/main/Virtualhost/Images/(5)%20contenido_examenMQA_conf.png)

### 3. Editar /etc/hosts

1. Editar el archivo /etc/hosts para mapear el dominio a la IP local:

```bash
nano /etc/hosts
```
![Editar archivo hosts](https://github.com/Arzeld/examenMQA/blob/main/Virtualhost/Images/(6)%20edicion_etchosts.png)

```hosts
127.0.0.1 daw.ejercicio3.com
```
![Linia a añadir en hosts](https://github.com/Arzeld/examenMQA/blob/main/Virtualhost/Images/(7)%20contenido_etchosts.png)

### 4. Habilitar el sitio y recargar Apache2

1. Habilitar la nueva configuración del sitio:

```bash
a2ensite examenMQA.conf
systemctl reload apache2
```
![Habilitar y recargar apache](https://github.com/Arzeld/examenMQA/blob/main/Virtualhost/Images/(8)%20final_examenMQA.png)

### 5. Resultado

![Resultado final](https://github.com/Arzeld/examenMQA/blob/main/Virtualhost/Images/(9)%20resultado.png)
