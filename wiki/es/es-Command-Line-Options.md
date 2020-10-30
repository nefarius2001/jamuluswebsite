---
layout: wiki
title: "Opciones de la Línea de Comandos"
lang: "es"
permalink: "/wiki/Command-Line-Options"
---

# Opciones de Línea de Comandos

Mientras que las funciones más comunes de Jamulus pueden configurarse usando la interfaz gráfica, Jamulus también puede ser controlado utilizando estas opciones en la línea de comandos. Exactamente cómo se hace dependerá de tu sistema operativo.

Por ejemplo, en Windows, para activar la grabación con la opción `-R`: haz clic derecho en el acceso directo de Jamulus y elige "Propiedades" > Destino. Añade los argumentos necesarios a Jamulus.exe:

```shell
"C:\Program Files (x86)\Jamulus\Jamulus.exe" -s -R "C:\path\to\your\Jam Recordings"
```

Para Macintosh, arranca una ventana de Terminal y ejecuta Jamulus con las opciones deseadas como sigue:

```shell
/Applications/Jamulus.app/Contents/MacOS/Jamulus -s -R "/path/to/your/jam recordings"
```

***

Puedes ver todas las opciones posibles soportadas por tu versión arrancando Jamulus con la opción `-h`.


| Corto | Nombre largo | `[...]` significa parámetro opcional | |
|-------|--------------|--------------------------------------|-|
|    `-c` |`--connect`        | Conectar con una dirección de servidor al arrancar, formato `dirección[:puerto]` | (solo cliente) |
|    `-d` |`--discononquit`   | Desconectar todos los clientes al salir | (solo servidor) |
|    `-e` |`--centralserver`  | Hace que el servidor sea público. |  (solo servidor) [Ver nota](Choosing-a-Server-Type#público). |
|    `-f` |`--listfilter`     | Lista blanca con IPs para registrarse en la lista de servidores de este servidor. | (solo servidor central) [Ver nota](Choosing-a-Server-Type#central). |
|    `-F` |`--fastupdate`     | Utiliza modo 64 muestras. Requiere un procesador potente para evitar cortes, y más ancho de banda si los clientes también se conectan con la opcion de "Activar Buffers Pequeños". | (Solo servidor) |
| `-h,-?` |`--help`           | Este texto de ayuda | (cliente y servidor) |
|    `-i` |`--inifile`        | Nombre de archivo de inicialización | (cliente y servidor) |
|    `-j` |`--nojackconnect`  | Deshabilitar conexiones automáticas de Jack | (solo cliente) |
|    `-l` |`--log`            | Habilitar registro, establece nombre del archivo | (solo servidor) |
|    `-m` |`--htmlstatus`     | Habilita un archivo de estado HTML, establece un nombre de archivo | (solo servidor) |
|    `-M` |`--mutestream`     | Arranca Jamulus en estado muteado | (solo cliente) |
|    `-n` |`--nogui`          | Deshabilitar interfaz gráfica  | (cliente y servidor) |
|    `-o` |`--serverinfo`     | Detalles de localización del servidor en el formato: <br/>`[nombre];[ciudad];[[valor locale]]; ...` <br/>`[dirección servidor1];[nombre servidor1];[ciudad servidor1];[país servidor1 como ID QLocale]; ...` <br/> `[dirección servidor2]; ...` | (primero para cualquier servidor; adicionales solo para el servidor central - [ver nota](Choosing-a-Server-Type#central).) |
|    `-p` |`--port`           | Número del puerto UDP local. Por defecto es 22124 | (solo servidor) |
|    `-R` |`--recording`      | Incluye una ruta editable donde se deben guardar los archivos (entrecomillado si es apropiado). | (solo servidor) Ver descripción en [Configuración del Servidor](Server--Windows-&-Mac#grabación). |
|       |`--norecord`       | Arranca la grabadora con la grabación desactivada| (solo servidor) |
|    `-s` |`--server`         | Arrancar en modo servidor | (solo servidor) [Ver nota](Choosing-a-Server-Type) |
|    `-t` |`--notranslation`  | Deshabilitar traducciones | (cliente y servidor) |
|    `-T` |`--multithreading` | Habilitar multithreading | (solo servidor) |
|    `-u` |`--numchannels`    | Número máximo de canales. Por defecto son 10, el máximo son 50 | (solo servidor) |
|    `-w` |`--welcomemessage` | Mensaje de bienvenida al conectarse. Soporta el formateo HTML y CSS (entre comillas), o establece ruta a un archivo de texto | (solo servidor) |
|    `-z` |`--startminimized` | Arranca minimizado | (solo servidor) |
|       |`--ctrlmidich`     | Canal para recibir mensajes de controlador MIDI | (solo cliente), ver [Consejos y Trucos](Tips,-Tricks-&-More#usar-la-opción---ctrlmidich-para-utilizar-un-controlador-midi) |
|       |`--clientname`     | Título de ventana y nombre de cliente en Jack | (solo cliente) | |