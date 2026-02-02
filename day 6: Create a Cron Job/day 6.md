
# Day 6: Create a Cron Job

En este ejercicio se debe crear una tarea programada con Cron job y vamos a seguir los siguientes pasos:


## Pasos Iniciales
Para hacer este ejercicio debemos crear el cron job en los 3 servidores de Nautilus como lo indica el enunciado (stapp01, stapp02, stapp03)


## Pasos

Nos conectamos al servidor que nos solicita el ejercicio 
ssh@<stapp0X>

1. Instala el servicio cron con (cronie)

```
sudo yum install -y cronie
```

2. Se debe iniciar y deja activo el servicio de cron

```
sudo systemctl start crond
sudo systemctl enable crond
```

  Verificamos que se encuentre activo el servicio 

```
systemctl status crond
```
  Debe mostrarnos el estado 

```
Active: active (running)
```
3. Crear el cron para el usuario root
```
sudo crontab -e
```

verifcamos con el comando 
```
sudo crontab -l
```
Se abre el editor Vim y agregamos la siguiente linea
```
*/5 * * * * echo hello > /tmp/cron_text
```
4. Este cron lo ejecutamos cuando la hora del sistema este en multiplos de 5
```
cat /tmp/cron_text
```
5. Cuando se ejecute nos debe mostrar el siguiente resultado
```
hello
```
