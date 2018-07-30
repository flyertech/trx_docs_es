---
title: Modo desarrollo
sidebar: mydoc_sidebar
permalink: debugging.html
folder: mydoc
---

## Modo desarrollo

Es posible habilitar una salida de debug de los datos recibidos por nuestros servidores. Esto es útil durante el desarrollo para asegurar que los datos están siendo correctamente enviados por la Tag de integración.
Simplemente inserta este snippet antes del loader:

```
window._trx_debug = true;
```

Este modo ha sido testado con Google Chrome (o Chromium) y Mozilla Firefox. Cuando se habilita, es posible leer el texto, en la consola del buscador, el contenido de la carga hecha por el Tag.

Además, dentro del Transactionale user dashboard, en la sección  *My account -> Integration* es posible comprobar la propia transmisión de todos estos eventos.