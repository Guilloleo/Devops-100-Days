# Day 2: Temporary User Setup with Expiry


### Temporary User Setup with Expiry

```
Para la creacion de un usuario temporal debemos hacer lo siguiente:

1. Conectarnos al servidor con el usuario: ssh banner
2. Con el comando hostname revisamos que estemos en el servidor correcto.
3. Usamos el comando useradd con la opción -e (formato YYYY-MM-DD):
4. sudo useradd -m -e 2026-10-31 Kareem
5. con el comando sudo chage -l Kareem
```
