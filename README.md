
# InternetDealers

Repositorio dedicado a la configuracion y mantenimiendo de los scripts referidos al equipo de InternetDealers

## Pasos

- Es necesario instalar UBUNTU 20.04

 1) na vez hayas accedido con tus credenciales a la VPS ingresa    las siguientes líneas:
-  sudo apt-get update
- sudo apt-get upgrade
Este proceso actualiza la distribución de Linux y puede llevar varios minutos.

2) Instalar el MULTI SCRIPT (Elegir la version 8.6 de VPS-MX, es la unica probada de momento)

```bash
  rm -rf Install-Sin-Key.sh; apt update; apt upgrade -y; wget https://raw.githubusercontent.com/NetVPS/VPS-MX_Oficial/master/Instalador/Install-Sin-Key.sh; chmod 777 Install-Sin-Key.sh; ./Install-Sin-Key.sh --start
```
3) Script udp (Luego de ejecutar este script se reiniciara el servidor)
```bash
wget "https://raw.githubusercontent.com/info-devf5r/UDP-Custom-Installer-Manager/main/install.sh" -O install.sh && chmod +x install.sh && ./install.sh
```

Después del reinicio usar esta linea para establecer el rango del puerto:
```bash
sudo ufw allow 1:65535/udp
```

4) Script instalador de websocket y dropbear:
Ejecutar el script y asignar puerto 80 para python y 444 para dropbear (o cualquier otro que no sea los conocidos para evitar conflicto)
```bash
sudo wget https://raw.githubusercontent.com/rudi9999/Script/master/Proxy.sh; chmod +x Proxy.sh* && ./Proxy.sh
```




### Notas


Nota 1: CADA VEZ QUE REINICIES TENDRAS QUE EJECUTAR EL PASO 4 YA QUE EL PUERTO WEBSOCKET SE CIERRA.

Nota 2: En caso de que el puerto udp se cierre solo ejecutar "sudo udp" y seleccionar la opción 1, todo esto fuera del script VPS-MX.
## Author

- [@sebasValdez](https://sebasvaldez.github.io/sebasvaldez.io/)

