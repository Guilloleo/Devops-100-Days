# Day 3: Secure Root SSH Access

```
Deshabilitar el acceso SSH directo del usuario root en los servidores Linux para mejorar la seguridad.

Para deshabilitar el acceso ssh
1. ingresamos con el usuario SSH@hostname de los 3 servidores del ejercicio
2. se confirma el hostname
3. ingresamo en la ruta sudo vi /etc/ssh/sshd_config
4. en el asrchivo que se nos abre debemos buscar PermitRootLogin yes, y dejarlo en: no, guadamos y salimos
5. se aplican los cambios con el comando sudo systemctl restart sshd
6. verificamos con el comando sudo sshd -T | grep permitrootlogin
7. y nos tiene que mostrar lo siguiente: permitrootlogin no
