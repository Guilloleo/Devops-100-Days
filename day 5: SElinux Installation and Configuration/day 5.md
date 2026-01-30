# SElinux Installation and Configuration

```
Para realizar la instalacion de SElinux en el servidor hacemos los siguientes pasos:

1. ingresamos al servidor que nos indica el ejercicio en este caso Nautilus App02
2. Utilizamos el comando sudo yum install -y selinux-policy selinux-policy-targeted, para la instalacion de SElinux
3. En el ejercicio se nos pide deshabilitarlo y no reinciar el servico ya que ahi un servicio programado
4. Vamos a la siguiente ruta sudo vi /etc/selinux/config, y buscamos SELINUX=enforcing
5. Dejamos ese servicio en estado SELINUX=disabled, y revisar que no este comentada
6. Guardamos y salimos
7. Con el comando sestatus, podemo ver el estado desabilitado
```
